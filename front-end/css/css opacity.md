//** CSS Opacity **//

The `opacity` property specifies the opacity/transparency of an element.

-- Transparent Image --

The `opacity` property can take a value from 0.0 - 1.0. "The lower value, the more transparent.

Example:

`img { opacity: 0.5;}`

-- Transparent Hover Effect --

The `opacity` property is often used together with the `:hover` selector to change the opacity on mouse-over.

Example:

```
img { opacity: 0.5;}  
  
img:hover { opacity: 1.0;}
```

Example explained:

The first Css block is similar to the code in Example 1. In addition, we have added what should happen when a user hovers over one of the images. In this case we want the image to NOT be transparent when the user hovers over it. The CSS for this is `opacity:1;`.

When the mouse pointer moves away from tthe image, the image iwll be transparent again.

`img:hover { opacity: 0.5;}`

-- Transparent Box --

When using the `opacity` property to add transparency to the background of an element, all of its child elements inherit the same transparency. This can make the text inside a fully transparent element hard to read.

-- Transparency using RGBA --

If you do not want to apply opacity to child elements, like in our example above, use RGBA color values. The following example sets the opacity for the background color and not the text.

You learned from our CSS Colors Chapter, that you can use RGB as a color value. In addition to RGB, you can use an RGB color value with an alpha channel (RBGA) - which specifies the opacity for a color.

An RGBA color value is specified with: rgba (red, green, blue, alpha). The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

`div { background: rgba(76, 175, 80, 0.3) /* Green background with 30% opacity */}`

-- Text in Transparent Box --

```
<html>  
<head>  
<style>  
div.background { background: url(klematis.jpg) repeat;  
  border: 2px solid black;}  
  
div.transbox { margin: 30px;  
  background-color: #ffffff;  
  border: 1px solid black;  
  opacity: 0.6;}  
  
div.transbox p { margin: 5%;  
  font-weight: bold;  
  color: #000000;}  
</style>  
</head>  
<body>  
  
<div class="background">  
  <div class="transbox">  
  <p>This is some text that is placed in the transparent box.</p>  
  </div>  
</div>  
  
</body>  
</html>
```

-- Example explained --

First, we create a `<div>` element (class="background") with a background image, and a border.

Then we create another `<div>` (class="transbox") inside the first `<div>`.

The `<div class="transbox">` have a background color, and a border - the div is transparent.

Inside the transparent `<div>`, we add some text inside a `<p>` element.