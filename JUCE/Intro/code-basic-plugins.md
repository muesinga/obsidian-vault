//** Orientation **//

Create a new audio plug-in with the name `TutorialPlugin`. 

A newly-created audio plug-in project contains two classes: `PluginProcessor` handles the audio and MIDI IO and processing logic, and `PluginEditor` handles any on screen GUI controls or visualisations.

When passing information between these two it is best to consider the processor as the parent of the editor. There is only one plug-in processor whereas you can create multiple editors. Each editor has a reference to the processor such that it can edit or access information and parameters from the audio thread. It is the editor's job to set and get information on this processir thread and not the other way around.

The main function we will be editing in the `PluginProcessor.cpp` file is the `processBlock()` method. This receives and produces both audio and MIDI data to the plug-in output. The main funtion we will change in the `PluginEditor.cpp` is the constructor, where we initialise and set up our window and GUI objects, and also the paint() method where we can draw extra controls and custom GUI components.m


