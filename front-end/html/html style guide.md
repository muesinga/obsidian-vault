//** HTML Sytle Guide **//

A consistent, clean, and tidy HTML code makes it esier for others to read and understand your code.

Here are some guidelines and tips for creating good HTML code.

-- Always Declare Document Type --

Always delcare the document type as the first line in your document.

The correct document type for HTML is:

`<!DOCTYPE html>`

-- Use Lowercase Element Names --


HTML allows mixing uppercase and lowercase letters in element names.

However, we recommend using lowercase element names, because:

• Mixing uppercase and lowercase names look bad
• Developers normakky use lowercase names
• Lowercase looks cleaner
• Lowercase is easier to write

-- Close All HTML Elements --

In HTML, you do not have to close all elements (for example the `<p>` element).

However, we strongly recommend closing all HTML elements.

-- Use Lowercase Attribute Names --

HTML allows mixing uppercase and lowercase letters in attribute names.

However, we recommend using lowercase attribute names, because:

• Mixing uppercase and lowercase names looks bad
• Developers normally use lowercase names
• Lowercase look cleaner
• Lowercase are easier to write

-- Always Quote Attribute Values --

HTML allows attribute values without quotes.

However, we recommend quoting attribute values, because:

• Developers normally quote attribute values
• Quoted values are easier to read
• You MUST use quotes if the value contains spaces

-- Always Specify alt, width, and height for Images --

Always specify the `alt` attribute for images. This attribute is important if for some reason the image cannot be displayed.

Also, always define the `width` and `height` of images. The reduces flickering, because the browser can reserve space for the image before loading. 

-- Spaces and Equal Signs --

HTML allows space around equal signs. But space-less is eaiser to read and groups entities better together.

-- Avoid Long Code Lines --

When using an HTML editor, it is NOT convenient to scroll right and left to read the HTML code.

Try to avoid too long code lines.

-- Blank Lines and Indentation --

Do not add blank lines, spaces, or indentations without a reason.

For readability, add blank lines to separate large or logical code blocks.

For readability, add two spaces of indentation. Do not use the tab key.

-- Never Skip the `<title>` Element --

The `<title>` element is required in HTML.

The contents of a page title is very important for a search engine optimization (SEO)! The page title is used by search engine algorithms to decide the order when listing pages in search results.

The `<title>` element:

• defines a title in the browser toolbar
• provides a title for the page when it is added to favorites
• displays a title for the page in search-engine results

-- Omitting `<html>` and `<body>`? --

An HTML page is validate without the `<html>` and `<body>` tags.

However, we strongly recommend to always add the `<html>` and `<body>` tags!

Omitting `<body>` can produce errors in older browsers.

Omitting `<html>` and `<body>` can also crash DOM and XML software.

-- Omitting `<head>`? --

The HTML `<head>` tag can also be omitted.

Browsers will add all elements before `<body>`, to a default `<head>` element.

However, we recommend using the `<head>` tag.

-- Close Empty HTML Elements? --

In HTML, it is optional to close empty elements.

If you expect XML/XHTML software to access your page, keep the closing slash (/), because it is required in XML and XHTML.

-- Add the lang Attribute --

You should always include the `lang` attribute inside the `<html>` tag, to declare the language of the Web page. This is meant to assist search engines and browsers.

-- Meta Data --

To ensure proper interpretation and correct search engine indexing, both the language and the character encoding `<meta charset="charset">` should be defines as early as possible in an HTML document.

-- Setting The Viewport --

The viewport is the user's visible area of a web page. It varies with the device - it will be smaller on a mobile phone than on a computer screen.

You should include the following `<meta>`h element in all your web pages:

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`

This gives the browser instructions on how to control the page's dimensions and scaling.

The `width=device-width` part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).

The `initial-scale=1.0` part sets the initial zoom level when the page is first loaded by the browser.

-- HTML Comments --

Short comments should be written on one line, like this:

`<!-- This is a comment -->`

Comments that spans more than one line, should be written like this:

```
<!--
  This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example.
 -->
 ```
 
 Long comments are easier to observe if they are indented with two spaces.
 
 -- Using Style Sheets --
 
 Use simple syntax for linking to style sheets (the `<type>` attribute is not necessary):
 
 `<link rel="stylesheet" href="styles.css">`
 
 Short CSS can be written compressed, like this:
 
 `p.intro {font-family:Verdana;font-size:16em;}`
 
 Long CSS rules should be written over multiple lines:
 
 ```
 body {
   background-color: lightgrey;
   font-family: "Arial Black", Helvetica, sans-serif;
   font-size: 16em;
   color: black;
 }
 ```
 
 • Place the opening bracket on the same line as the selector
 • Use one space before the opening bracket
 • Use two spaces of indentation
 • Use semicolon after each property-value pair, including the last
 • Only use quotes around values if the value contains spaces
 • Place the closing bracket on a new line, without leading spaces
 
 -- Loading JavaScript in HTML --
 
 Use simple syntax for loading external scripts (the `type` attribute is not necessary):
 
 `<script src="myscript.js">`
 