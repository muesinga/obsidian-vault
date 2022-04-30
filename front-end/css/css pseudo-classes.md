//** CSS Pseudo-Classes **//

A pseudo-class is used to define a special state of an element.

For example, it can be used to:

• Style an element when a user mouses over it
• Style visited and unvisited links differently
• Style an element when it gets focus

-- Anchor Pseudo-classes --

Links can be displayed in different ways:

```
/* unvisited link */  
a:link { color: #FF0000;}  
  
/* visited link */  
a:visited { color: #00FF00;}  
  
/* mouse over link */  
a:hover { color: #FF00FF;}  
  
/* selected link */  
a:active { color: #0000FF;}
```

NOTE: `a:hover` MUST come after `a:link` and `a:visited` in the CSS definition in order to be effective! `a:active` MUST come after `a:hover` in the CSS definition in order to be effective! Pseudo-class names are not case-sensitive.

-- Pseudo-classes and CSS Classes --

Pseudo-classes can be combined with CSS classes.

When you hover over the link in the example, it will change color:

`a.highlight:hover { color: #ff0000;}`

-- Hover on `<div>` --

An example of using the `:hover` psuedo-class on a `<div>` element:

`div:hover { background-color: blue;}`

-- Simple Tooltip Hover --

Hover a `<div>` element to show a `<p>` element (like a tooltip):

```
p { display: none;  
  background-color: yellow;  
  padding: 20px;}  
  
div:hover p { display: block;}
```

-- CSS - The :first-child Pseudo-class --

The `:first-child` pseudo-class matches a specified element that is the first child of another element.

-- Match the first `<p>` element --

The the following example, the selector matches any `<p>` element that is the first child of any element:

`p:first-child { color: blue;}`

-- Match the first `<i>` element in all `<p>` elements --

In the following example, the selector matches the first `<i>` element in all `<p>` elements:

`p i:first-child { color: blue;}`

-- Match all `<i>` elements in all first child `<p>` elements --

In the following example, the selector matches all `<i>` elements in `<p>` elements that are the first child of another element:

`p:first-child i { color: blue;}`

-- CSS - The :lang Pseudo-class --

The `:lang` pseudo-class allows you to define special rules for different languages.

In the example below, `:lang` defines the quotation marks for `<q>` elements with lang="no":

```
<html>  
<head>  
<style>  
q:lang(no) { quotes: "~" "~";}  
</style>  
</head>  
<body>  
  
<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>  
  
</body>  
</html>
```