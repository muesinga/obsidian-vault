//** HTML Classes **//

The HTML `class` attribute is used to specify a class for an HTML element.

Multiple HTML elements can share the same class.

-- Using The class Attribute --

The `<class>` attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.

In the following example we have three `<div>` elements with a `class` attribute with the value of "city". All of the three `<div>` elements will be styled equally according to the `.city` style definition in the head section.

-- The Syntax for Class --

To create a class; write a period (.) character, followed by a class name. Then, define the CSS properties within the curly braces {}:

-- Multiple Classes --

HTML elements can belong to more than one class.

To define multiple classes, separate the class names with a space, e.g. `<div class="city main">`. The element will be styled according to all the classes specified.

In the following example, the first `<h2>` element belongs to both the `city` class and also to the `main` class, and will get the CSS styles from both of the classes.

-- Different Elements Can Share Same Class --

Different HTML elements can point to the same class name.

In the following example, both `<h2>` and `<p>` points to the "city" class and will share the same style.

-- Use of The class Attribute in JavaScript --

The class name can also be used by JavaScript to perform certain tasks for specific elements.

JavaScript cna access elements with a specific class name with `getElementsByClassName()` method.

--Summary --

• The HTML `class` attribute specifies one or more class names for an element
• Classes are used by CSS and JavaScript to select and access specific elements
• The `class` attribute can be used on any HTML element
• The class name is case sensitive
• Different HTML elements can point to the same class name
• JavaScript can access elements with a specific class name with the `getElementsByClassName()` method