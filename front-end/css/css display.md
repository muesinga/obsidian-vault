//** CSS Display **//

The `display` property is th emost important CSS property for controlling layout.

-- The display Property --

The `display` property specifies if/how an element is displayed.

Every HTML element has a sdefualt display value depending on what type of element it is. The default display value for most elements is `block` or `inline`.

-- Block-Level Elements --

A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can)

Examples of block-level elements:

• `<div>`
• `<h1> - <h6>`
• `<p>`
• `<form>`
• `<header>`
• `<footer>`
• `<section>`

-- Inline Elements --

An inlilne element does not start on a new line and only takes up as much width as necessary.

Examples of inline elements:

• `<span>`
• `<a>`
• `<img>`

-- Display: none; --

`display: none;` is commonly used with JavaScript to hide and show elements without deleting and recreating them. 

The `<script>` element uses `display: none;` as default.

-- Override The Default Display Value --

As mentioned, every element has a default display value. However, you can override this. 

Changing an inline element to a block element, or vice versa, can be useful for making the page look a specific way, and stil follow the web standards.

A common example is making inline `<li>` elements for horizontal menus.

Example:

`li { display: inline; }`

NOTE: Setting the display property of an element only changes how the element is displayed, NOT what kind of element it is. So, an inline element with `display: block;` is not allowed to have other block elements inside it.

-- Hide an Element - display:none or visibility:hidden? --

Hiding an element can be done by setting the `display` property to `none`. The element will be hidden, and the page will be diplayed as if the element is not there:

`h1.hidden { display: none;}`

`visibility:hidden;` also hides an element.

-- CSS Display/Visibility Properties --

`display` -- Specifies how an element should be displayed
`visibility` -- Specifies whether of not an element should be visible