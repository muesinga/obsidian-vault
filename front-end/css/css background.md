//** CSS Background **//

The CSS background properties are used to add background effects for elements.

-- CSS background-color --

The `background-color` property specifies the background color of an element.

With CSS, a color is most specified by:

• a valid color name - like "red"
• a HEX value - like "#ff0000"
• an RGB value - like "rgb(255, 0, 0 )"

You can set the background color for any HTML element.

-- Opacity / Transparency --

The `opacity` property specifies the opacity/tranparency of an element. It can take a value from 0.0 - 1.0. The lower value, the more transparent.

Note: When using the `opacity` propoerty to add transparency to the background of an element, all of its child elements inherit the same transparency. This can make the text inside a fully transparent element hard to read.

-- Transparency using RGBA --

If you do not want to apply opacity to child elements, like in our example above, use RGBA color values. The following example sets the opacity for the background color and not the text.

You learned from our CSS Color Chapter, that you can use RGB as a color value. In addition to RGB, you can use an RGB color value with an alpha channel (RGBA) - which specifies the opacity for a color.

An RGBA color value is specified with: rgba(red, green, blue, alpha). The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

Example:


`div { background: rgba(0, 128, 0, 0.3) /* Green background with 30% opacity */}`

//** Background Image **//

The `background-image` property specifies an image to use as the background of an element.

By default, the image is repeated so it covers the entire element.

Set the background image for a page:

`body { background-image: url("paper.gif");}`

Note: When using a background image, use an image that does not disturb the text.

The background image can also be set for specific elements, like the `<p>` element:

`p { background-image: url("paper.gif");}`

//** Background Repeat **//

By default, the `background-image` property repeats an image both horizontally and vertically.

Some images should be repeated only horizontally or vertically, or the will look strange. 

-- CSS background-repeat:: no-repeat --

Showing the background image only once is also specified by the `background-repeat`  property::

Example:

```
body { background-image: url("img_tree.png");  
  background-repeat: no-repeat;}
```

In the example above, the background image is placed in the same place as the text. We want to change the position of the image, so that it does not disturb the text too much.

-- CSS background-position --

The `background-position` property is usaed to specify the position of the background image.

```
body { background-image: url("img_tree.png");  
  background-repeat: no-repeat;  
  background-position: right top;}
```

-- Background Attachment --

The `background-attachment` property specifies whether the background image should scroll or be fixed (will not scroll with the rest of the page):

```
body { background-image: url("img_tree.png");  
  background-repeat: no-repeat;  
  background-position: right top;  
  background-attachment: fixed;}
```

-- Background Shorthand --

To shorten the code, it is also possible to specify all the background properties in one single property. This is called a shorthad property.

Instead of writing:

```
body { background-color: #ffffff;  
  background-image: url("img_tree.png");  
  background-repeat: no-repeat;  
  background-position: right top;}
```

You can use the shorthand property `background`:

Example:

```
body { background: #ffffff url("img_tree.png") no-repeat right top;}
```

When using the shorthand property the order of the property values is:

• `background-color`
• `background-image`
• `background-repeat`
• `background-attachment`
• `background-position`

It does not matter if one of the property values is mising , as long as the other ones are in this order. Note that we do not use the background-attachment property in the examples above, as it does not have a value.

//** All CSS Background Properties **//

•`background` -- Sets all the background properties in one declarations
• `background-attachment` -- Sets whether a background image is fixed or scrolls with the rest of the page
• `background-clip` -- Specifies the painting area of the background
• `background-color` -- Sets the background color of an element
• `background-image` -- Sets the background image for an element
• `background-origin` -- Specifies where the background image(s) is/are positioned
• `background-position` - Sets how a background image will be repeated
• `background-size` - Specifies the size of the background image(s)