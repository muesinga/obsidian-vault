//** HTML File Paths **//

A file path describes the location of a file in a web site's folder structure.

File paths are used when linking to external files, like:

• Web pages
• Images
• Style sheets
• JavaScript

-- Absolute File Paths --

Example:

`<img src="https://www.w3schools.com/images/picture.jpg" alt="Mountain">`

-- Relative File Paths --

A relative file path points to a file relative to the current page.

In the following example, the file path points to a file in the images folder located at the root of the current web:

`<img src="/images/picture.jpg" alt="Mountain">`

In the following example, the file path points to a file in the images folder located in the folder one level up from the current folder:

`<img src="../images/picture.jpg" alt="Mountain">`

-- Best Practice --

It is best practice to use relative file paths (if possible).

When using relative file paths, your web pages will not be bounf to your current base URL. All links will work on your own computer (localhost) as well as on your current public domain and your future public domains.
