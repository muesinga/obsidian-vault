//** The AudioSource Class **//

We can generate audio sample-by-sample in the `getNextAudioBlock()` function of the Audio Application template, however there are built-in tools for generating and processing audio. These allow us to link together high-level building blocks to form powerful audio applications without having to process each and every sample of audio within our application code (JUCE does this on our behalf). These building blocks are based on the `AudioSource` class. 

The `AudioAppComponent` class itself inherits from the AudioSource class and, importabtly, contains an `AudioSourcePlayer` object that streams the audio between the `AudioAppComponent` and the audio hardware device. We can simply generate the audio samples directly in the `getNextAudioBlock()` function but we can instead chain a number of `AudioSource` objects together to form a series of processes.

Once the is loaded we can consider these four possible states:

	• Stopped: Audio playback is stopped and ready to be started
	• Starting: Audio playback hasn't yet started but it has been told to start
	• Playing: Audio is playing
	• Stopping: Audio is playing but playback has been told to stop, after this it will return to the "stopped" state.