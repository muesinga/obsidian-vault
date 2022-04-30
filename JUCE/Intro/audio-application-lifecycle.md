//** Audio Application Lifecycle **//

The AudioAppComponent class is an abstract base class, it has three pure virtual functions that represent the lifecycle of our audio application that we must implement in our derived class:

	• AudioAppComponent::prepareToPlay(): This is called just before audio processing starts.
	
	• AudioAppComponent::releaseResources(): This is called when audio processing has finished.
	
	• AudioAppComponent::getNextAudioBlock(): This is called each time the audio hardware needs a new block of audio data.
	
of these three, the most important is perhaps `AudioAppComponent::getNextAudioBlock()`, since this is where you will either generate or process audio in your JUCE audio application. To understand how this workds, we need to know a little about how modern computers generate audio. The audio hardware needs to generate a certain number of samples per channel for each second of audio. The CD-quality sample rate is 44.1kHz, which means there needs to be 44100 samples per second per channel sent to the audio hardware for playback. Rather than being passed to the audio hardware a single sample at a time, the samples are passed in buffers -- or blocks -- containing a certain number of samples. For example, at 44.1kHz and a block size of 441 our `AudioAppComponent::getNextAudioBlock()` function would be called 100 times per second.

	Note: The buffer size of 441 samples, above, is used to keep the arithmetic simple for the purposes of explanation. In practice, a buffer size of 441 would be unusual. Hardware buffer sizes would almost certainly be a even number and would tend to be power-of-two (256, 512, 1024, and so on). It is important that you application is prepared to deal with any buffer size.

Essentially, our AudioAppComponent::getNextAudioBlock() is servicing the audio callbacl of the audio hardware. It is importnat to note that this function will be called from another thread (the audio thread in most cases).

For our JUCE audio application to work correctly, there are two more important functions. This time we need to call them, rather than implement them:

	• AudioAppComponent::setAudioChannels(): We must call this to register the number of input and output channels we need. Typically, we do this in our constructor. In turn, this function triggers the start of audio processing in our application.
	
	• AudioAppComponent::shutdownAudio(): We must call this to shutdown the audio system. Typically, we do this in our destructor. 
	
//** Initalising the audio application **//

The constructor needs to set up the size of the Component object. We also need to initalise at least one audio output:

	`MainContentComponent()
		{
			setSize (800, 600);
			setAudioChannels (0, 2); // no inputs, two outputs
		}`

The call to the `AudioAppComponent::setAudioChannels()` function triggers the audio system to start up. In particular, it will call the prepareToPlay() function:

	`void prepareToPlay (int samplesPerBlockExpected, double sampleRate) override
		{
			juce::String message;
			message << "Preparing to play audio...\n";
			message << "samplesPerBlockExpected = " << samplesPerBlockExpected << "\n";
			message << " sampleRate = " << sampleRate;
			juce::Logger::getCurrentLogger()->writeToLog(message);
		}`
		
In this case we don't really need to do anything here, but as it is a pure virtual function we must implement at least an empty function. Here we log some useful information that we can gain about the audio system on the target device at this point. The samplesPerBlockExpected arguement, as its name suggests, is the size (in samples) of the buffers of audio that we can expect to be asked for each time a buffer of audio is requested in our getNextAudioBlock() function. This buffer size might vary between callbacks, but it is a good indication. The sampleRate argument tells us the current sample rate of the hardware. We would need this if we were doing something that is frequencey-dependent, such as synthesising tones or using equalisation. We would also need to know the sample rate if we were using delay effects. We don't need this information to generate noise.

//** Generating Audio Data **//

Soon after this call to our prepareToPlay() function the audio thread will begin requesting blocks of audio via the `AudioAppComponent::getNextAudioBlock()` function. This function is passed a single `bufferToFill` argument that is an AudioSourceChannelInfo struct. The AudioSourceChannlInfo struct contains a multichannel buffer of audio samples. It also contains two integer values that specify which regions of this buffer should be processed on this call. In more detail, the `AudioSourceChannelInfo` contains the following members:

	• `AudioSampleBuffer* buffer:` An `AudioSampleBuffer`object is a multichannel buffer of audio data that is essentially a multidimensional array of float values. When our getNextAudioBlock() function is called, this buffer contains any audio data from the target device's audio input (if we requested audio input). When our getNextAudioBlock() function returns, we must have filled the relevant section of the buffer with audio that we want to play.
	
	•int startSample: This is the sample index within the buffer where our getNextAudioBlock() function should start reading or writing audio.
	
	•int numSamples: This is the number of samples in the buffer that should be read or written.

Audio data stored as floating point values is very straightforward. Each sample of the audio signal is stored as a value that is normally in the range ±1.0.

![[Screen Shot 2021-12-12 at 7.47.26 AM.png]]

At a peak level of ±1.0 like this the output level will be very loud. In fact, this is the loudest the audio system will be able to generate without clipping. Typically, we will need to output audio that doesn't exceed this ±1.0 limit (allthough it is fine for intermeiate stages of processing to go beyond this limit, as long as the final output is lower.)

//** The AudioSampleBuffer Class **//

While the AudioSampleBufffer class is (as a very basic level) just a multichannel array of float values, it provides a useful set of functions for dealing with audio data:

	• `AudioSampleBuffer::getNuChannels()`: This returns the number of audio channels stored in the buffer. In this case the value should match the number of output channels we requested in our call to the `AudioAppComponent::setAudioChannels()` function earlier. (This value will always be maximum of the number of input and output channels.)
	
	• `AudioSampleBuffer::getWritePointer()`: This returns a pointer to the buffer of float vlaues at a specific sample offset.