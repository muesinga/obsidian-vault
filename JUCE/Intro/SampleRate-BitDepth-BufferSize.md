//** Sample Rate **//

Sample Rate is the number of times the audio is captured per second. This is analogous with the FPS (Frames Per Second) of video.

Sample Rate values are typically written in kHz (kiloHertz).

Sample Rates come in 'bands' and common examples include:

	• Single Band - 44.1kHz & 48kHz
	
	• Dual Band - 88.2kHz & 96kHz
	
	• Quad Band - 176.4kHz & 192kHz
	
For example, when recording using a sample rate of 48kHz, 48,000 samples are being captured each second by your audio recording device.

As you increase the sample rate, you capture more samples on the incoming audio signal each second.

The maximum frequency that can be captured correctly by a recording device is limited by the sample rate the device is set to.

There is a simple rule for determining the maximum frequency given a sample rate (Nyquist Theorem):

`Sample rate/2 = maximum frequency that can be correctly captured`

This means, when using a sample rate of 48kHz, we can capture audio frequencies up to 24kHz.

The range of human hearing is from around 20Hz to 20kHz so sample rates of 44.1 & 28kHz are commonly used because they are more than capable of capturing the full range of the human audible spectrum.

//** Bit Depth **//

Bit Depth is the number of "bits" captured in each sample per second.

As bit depth changes, so does the dynamic range. As bit depth increases, the threshold of what can be heard and recorded by your recording software. The maximum range of human hearing typically does not exceed 120dB.

//** Buffer Size **//

Buffer Size is the amount of time allowed for your computer to process the audio of your sound card or audio interface.

This applies when experiencing latency, which is a delay in processing audio in real-time. You can reduce your buffer size to reduce latency but this can result in a higher burden on your computer that can cause glitchy audio or drop-outs.

When introducing more audio tracks to your session, you may need a larger buffer size to accurately record the signal with no distortion and limited latency. Increasing the buffer size will allow more time for the audio to be captured without distortion.

It is important to find the right buffer size for your session as this can vary depending on the number of tracks, plug-ins, audio files ets. We do not recommend a specific setting because it will depend on your specific project.

When Recording:

	• Set the buffer size as low as you can to reduce latency. If you start hearing clicks ad pops or your DAW gives you an error message, either raise the buffer size or reduce the number of effects plug-ins/audio tracks in your project.
	
When Mixing:

	• As latency is not really a factor when mixing, you can afford to put the buffer size at its highest setting. This will reduce the chances of any clicks and pops being heard when you add effects plug-ins.
	
General Music/Audio:

	• Latency is not a factor when just listening to music outside of a DAW so the buffer size can be set to its highest setting. 