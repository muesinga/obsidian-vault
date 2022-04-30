//** CSS Text **//

-- Text Color --

The `color` property is used to set the color of the text. The color is specified by:

• a color name - like "red"
• a HEX value - like "#ff0000"
• an RGB value - like "rgb(255,0,0)"

-- Text Alignment --

The `text-align` property is used to set the horizontal alignment of a text.

A text can be left or right aligned, centered, or justified.

The following example shows center aligned, and left and right aligned text (left alignmnet is default if text direction is left-to-right, and right alignment is default if text direction is right-to-left):

```
h1 { text-align: center;}  
  
h2 { text-align: left;}  
  
h3 { text-align: right;}
```

When the `text-align` property is set to "justify", each line is stretched so that every line has equal width, and the left and right margins are straight (like in magazines and newspapers):

`div { text-align: justify;}`

-- Text Direction --

The `direction` and `unicode-bidi` properties can be used to change the text direction of an element:

```
p { direction: rtl;  
  unicode-bidi: bidi-override;}
```

-- Vertical Alignment --

The `vertical-align` property sets the vertical alignment of an element.

This example demonstrates how to set the vertical alignment of an image in a text:

```
img.top { vertical-align: top;}  
  
img.middle { vertical-align: middle;}  
  
img.bottom { vertical-align: bottom;}
```

//** Text Decoration **//

The `text-decoration` property is used to set or remove decorations from text.

The value `text-decoration: none;` is often used to remove underlines from links:

`a { text-decoration: none;}`

//** Text Transformaiton **//

The `text-transform` property is used to specify uppercase and lowercase letters in a text.

It can be useed to turn everything into uppercase or lowercase letters, or capiltalize the first letter of each word:

Example:

```
p.uppercase { text-transform: uppercase;}  
  
p.lowercase { text-transform: lowercase;}  
  
p.capitalize { text-transform: capitalize;}
```

//** Text Spacing **//

-- Text Indentation --

The `text-indent` property is used to specify the indentation of the first line of a text:

`p { text-indent: 50px;}`

-- Letter Spacing --

The `letter-spacing` property is used to specify the space between the characters in a text.

The following example demonstrates how to increase or decrease the space between characters:

```
h1 { letter-spacing: 5px;}  
  
h2 { letter-spacing: -2px;}
```

-- Line Height --

The `line-height` property is used to specify the space between lines:

```
p.small { line-height: 0.8;}  
  
p.big { line-height: 1.8;}
```

-- Word Spacing --

The `word-spacing` property is used to specify the space between the words in a text.

The following example demonstrates how to increase or decrease the space between words:

```
h1 { word-spacing: 10px;}  
  
h2 { word-spacing: -2px;}
```

-- White Space --

The `white-soace` property specifies how white-space inside an element is handled.

The example demonstrates how to disable text wrapping inside an element:

`p { white-space: nowrap;}`

-- Text Shadow --

The `text-shadow` property adds shadow to text.

In its simplest use, you only specify the horizontal shadow (2px) and the vertical shadow (2px):

`h1 { text-shadow: 2px 2px;}`

Next, add a color (red) to the shadow:

`h1 { text-shadow: 2px 2px red;}`

Then, add a blur effect (5px) to the shadow:

`h1 { text-shadow: 2px 2px 5px red;}`

-- All CSS Properties --

• `color` -- Sets the color of text
• `direction` -- Specifies the text direction/writing direction
• `letter-spacing` -- Increase or decrease the space between characters in a text
• `line-height` -- Sets the line height
• `text-align` -- Specifies the horizontal alignment of text
• `text-decoration` -- Specifies the decoration added to text
• `text-indent` -- Specifes the indentation of the first line in a text-block
• `text-shadow` -- Specifies the shadow effect added to text
• `text-transform` -- Controls the capitalization of text
• `text-overflow` -- Specifies how overflowed content that is not displayed should be signaled to the user
• `unicode-bidi` -- Used together with the direction property to set or return whether the text should be overridden to support multiple languages in the same document
• `vertical-align` -- Sets the vertical alignment of an element
• `white-space` -- Specifies how white-space inside an element in handled
• `word-spacing` -- Increases or decreases the space between words in a text