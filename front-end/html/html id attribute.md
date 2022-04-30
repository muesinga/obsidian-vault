//** HTML Id Attribute **//

The HTML `id` attribute is used to specify a unique id for an HTML element.

You cannot have more than one element with the same id in an HTML document.

-- Using The id Attribute --

The `id` attribute specifies a unique id for an HTML element. The value of the `id` attribute must be unique within the HTML document.

The `id` attribute is used to point to a specific style declaration in a style sheet. It is also used by JavaScript to access and manipulate the element with the specific id.

The syntax for id is: write a hash character (#), followed by an id name. Then, define the CSS properties within curly braces {}.

In the following example we have an `<h1>` element that points to the id name "myHeader". This `<h1>` element will be styled according to the `#myHeader` style definition in the head section.

-- Difference Between Class and ID --

A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page.

-- HTML Bookmarks with ID and Links --

HTML bookmarks are used to allow readers to jump to specific parts of a webpage.

Bookmarks can be useful if your page is very long.

To use a bookmark, you must first create it, and then add a link to it.

Then, when the link is clicked, the page will scroll to the location with the bookmark.

-- Example --

First, create a bookmark with the `id` attribute:

`<h2 id="C4">Chapter 4</h2>`

Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:

`<a href="#C4">Jumpt to Chapter 4</a>`

Or, add a link to the bookmark ("Jump to Chapter 4"), from another page:

`<a href="html_demo.html#C4">Jump to Chapter 4</a>`

-- Using The id attribute in JavaScript --

The `id` attribute can also be used by JavaScript to perform some tasks for that specific element.

JavaScript can access an element with a specific id with `getElementbyId()` method:

```
<script>
function displayResults() {
	document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
</script>
```

-- Chapter Summary --

• The `id` attribute is used to specify a unique if for an HTML element
• The value of the `id` attribute must be unique within the HTML document
• The `id` attribute is used by CSS and JavaScript to style/select a specific element
• The value of the `id` attribute is also used to create HTML bookmarks
• JavaScript can access an element with a specific id with the `getElementById()` method