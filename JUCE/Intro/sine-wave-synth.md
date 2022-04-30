//** std::sin() **//

It is possible to use the standard library function `std::sin()`. In order to use this we need to maintain a state for our sine wave generation by storing the current phase angle and the amount by which the phase angle needs to increment for each output sample. This size of this change per sample ("delta") is dependent on the sample rate of the output and the frequency of the sine wave we want to generate.

//** Maintaing our State **//

In our MainContentComponent class we stored three double members:

`double currentSampleRate = 0.0, currentAngle = 0.0, angleDelta = 0.0;`

We have a simple function that updates the angleDelta member:

`void updateAngleDelta()
{
	auto cyclesPerSample =
	frequencySlider.getValue() / currentSampleRate;
	angleDelta = cyclesPerSample * 2.0 *
	juce::MathConstants<double>::pi;
}`

Before this function can work correctly we need to know the output sample rate. This is because we need to know how frequently the samples are being generated, this is in order to know the amount of change that is needed per sample. We are passed the sample rate by the `AudioAppComponent::prepareToPlay()`callback function:

`void prepareToPlay (int, double sampleRate) override
{
	currentSampleRate = sampleRate;
	updateAngleDelta();
}`

Here we store a copy of the sample rate value and call our updateAngleDelta() function initially.

//** Using the slider value **//

When the slider is moved while the app is running, we need to update the angleDelta member again:

`frequencySlider.onValueChange = [this]
{
	if (currentSampleRate > 0.0)
	updateAngleDelta();
}`

Here we check that the sample rate is valid before calling the updateAngleDelta() function again.

//** Outputting the audio **//

During the `getNextAudioBlock()` callback we need to generate the actual sine wave and write it to the output:

`void getNextAudioBlock (const juce::AudioSourceChannelInfo& bufferToFill) override
{
	auto level = 0.125f;
	auto* leftBuffer = bufferToFill.buffer->getWritePointer (0, bufferToFill.startSample);
	auto* rightBuffer = bufferToFill.buffer->getWritePointer (1, bufferToFill.startSample);
	
	for (auto sample = 0; sample < bufferToFill.numSamples; ++sample)
		{
			auto currentSample = (float) std::sin (currentAngle);
			currentAngle += angleDelta;
			leftBuffer[sample] = currentSample * level;
			rightBuffer[sample] = currentSample * [level];
		}
}`

For each output sample we calculate the sine function for the current angle, then increment the angle for the next sample. Notice that we bring the level down to 0.125 as a full scale sine wave will be very loud! We could (and perhaps should) wrap the current angle value back to zero when it reaches 2pi. Since larger values still return a valid value we can actually avoid this calculation. We get something like that shown in the following image:

![[Screen Shot 2021-12-13 at 9.43.36 AM.png]]

//** The slider configuration **//

You may have noticed that the slider value changes non-linearly (if not you should try this out now). These changes are, in fact, logarithmc. This give us higher resolution for smaller values and lower resolution for larger values. When controlling a frequency value this is often appropriate (as musically, we hear equal changes in ratios between frequences rather than equal linear changes). This is configured by using the Slider::setSkewFactorFromMidPoint() function. Our slider range is set to 50..5000 therefire setting the centre of the slider track to represent 500 would mean there is an equal musical interval between the slider minimum and the centre, and the centre and the slider maximum:

`MainContentComponent()
{
	addAndMakeVisible (frequencySlider);
	frequencySlider.setRange (50.0, 500.0);
	frequencySlider.setSkewFactorFromMidPoint (500.0);`
	
//** Smoothing frequency changes **//

You may notice -- especially in the higher frequencies -- that there are audible, and probably unwanted, artefacts produced as the slider is moved. This is because the slider is actually changing in discrete steps, and when the slider is moved quickly then these steps are quite large. In addition to this the slider frequency is only updated for each audio block, therefore the precise effect of these changes will be dependent on the hardward block size.

//** State members for smoothing **//

Let's add two members to our class, one to store the current frequency being used for synthesis, and another target frequency that the user has requested by moving the slider. Then we can more slowly ramp between these values to remove the artefacts:

`double currentFrequency = 500.0, targetFrequency = 500.0;`

We initalise these values at the same time. We can also initalise the slider to the same value:

`MainContentComponent()
{
	addAndMakeVisible (frequencySlider);
	frequencySlider.setRange (50.0, 5000.0);
	frequencySlider.setSkewFactorFromMidPoint (500.0);
	frequencySlider.setValue (currentFrequency,
	juce::dontSendNotification);`
	
//** Updating the synthesis code **//

The key to the way this algorithm works is to check whether the current and target values are the same or different. If they are the same, then we can simpy use our original code as the `angleDelta` member doesn't need to change. If the current and target values are different, then we need to update the `angleDelta` member for each sample as we gradually move the current value closer to the target.

` void getNextAudioBlock (const juce::AudioSourceChannelInfo& bufferToFill) override
{
	auto levle = 0.125f;
	auto* leftBuffer = bufferToFill.buffer->getWritePointer (0, bufferToFill.startSample);
	auto* rightBuffer = bufferToFill.buffer->getWritePointer (1, bufferToFill.startSample);
	
	auto localTargetFrequency = targetFrequency;
	
	if (localTargetFrequency != currentFrequency)
	{
			auto frequencyIncrement = 
		(localTargetFrequency - currentFrequncy - currentFrequency) / bufferToFill.numSamples;
		
			for (auto sample = 0; sample bufferToFill.numSamples; ++sample)
				{
					auto currentSample = 
					(float) std::sin (currentAngle);
						currentFrequency += frequencyIncrement;
							updateAngleDelta();
							currentnAngle += angleDelta;
							leftBuffer[sample] = 
							currentSample * level;
							rightBuffer[sample] = 
							currentSample * level;
							}
							currentFrequency = localTargetFrequency;
						}
						else
						{
							for (auto sample = 0; sample < bufferToFill.numSamples;; ++sample)
								{
									auto currentSample = (float) std::sin (currentAngle);
									currentAngle += angleDelta;
									leftBuffer[sample] = 
									currentSample * level;
									rightBuffer[sample] =
									currentSample * level;
								}
						}
				}
`

The format of this code uses a typical pattern for DSP code. We avoid conditional statements in the inner `for()` loop, if possible. Instead, having the condition tested outside the loop, and we two different, but quite similar loops depending upon whether the paramenter is changing. 