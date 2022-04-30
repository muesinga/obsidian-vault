![[Screen Shot 2021-11-18 at 7.44.07 AM.png]]

//** GUI Projects **//

GUI project templates provide a source files to start the development process. Since the application will display a graphical user interface, the template provides you with a Main.cpp file in which a class derived from a JUCEApplication will have been created.  

The JUCEApplication class is an abstract base class that provides startup and shutdown functionalities for your application. The Main.cpp file also creates the application window in which you GUI will reside.

//** The GUI Application **//

The GUI Application project is the most generic of all GUI projects and in addition to the Main.cpp file, it also creates a MainComponent class derived from the Component class.

The Component class is a base class for all user-interface objects in JUCE. All your GUI elements should be defined and placed in the MainComponent class.

![[Screen Shot 2021-11-20 at 8.08.11 AM.png]]

When a GUI Application project is created you will find the following files in the source folder:

	• Main.cpp: Derived from the JUCEApplication class, it provides initialisation code for you application and window.
	
	• MainComponent.h: Header file for the MainComponent derived from the Component class.
	
	• MainComponent.cpp: Implementation file for the MainComponent derived from the Component class.
	
Use this project type when you know you will need a GUI in your application but are unsure of need flexibility as to the features of your application.

//** The Audio Application **//

The Audio Application is similar to the GUI Application but instead of the MainComponent deriving for the Component class, it derives from the AudioAppComponent class.

The AudioAppComponent class is an abstract base class that combines the functionalitites of a Component with an AudioSource to provide a convienient starting point to handle audio input/output.

![[Screen Shot 2021-11-20 at 8.12.47 AM.png]]

When an Audio Application project is created you will find the following files in the source folder:

	• Main.cpp: Derived from the JUCEApplication class, it provides initialisation code for your application and window.
	
	• MainComponent.cpp: Header and implementation file for the MainComponent derived from the AudioAppComponent class.
	
//** The Audio Plugin **//

The Audio Plugin project has an all around different project structure compared to other template projects offered by the Projucer and creates and `AudioProcessor` and an `AudioProcessorEditor`.

The `AudioProcessor` class is an abstract base class that handles tha audio processing of your audio plugin. It represents an instance of a loaded plugin and is wrapped by the different plugin formats such as VST, AU, RTAS, and AAX.

The `AudioProcessorEditor` class is a base class derived from the `Component` class and holds the GUI funtionalities of your audio plugin.

![[Screen Shot 2021-11-20 at 8.25.23 AM.png]]

When an Audio Plugin project is created you will find the following files in the source folder:

	• PluginProcessor.h: Header file for the PluginProcessor derived from the `AudioProcessor` class.
	
	• PluginProcessor.cpp: Implementation file for the PluginProcessor derived from the AudioProcessor class.
	
	• PluginEditor.h: Header file for the PluginEditor derived from the AudioProcessorEditor class.
	
	• PluginEditor.cpp: Implementation file for the PluginEditor derived from the AudioProcessorEditor class.
	
	