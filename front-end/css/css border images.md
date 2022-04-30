//** CSS Border Images **//

With the CSS `border-image` property, you can set an image to be used as the border around an element.

-- CSS border-image Property --

The CSS `border-image` property allows you to specify an image to be used insetead of the normal border around an element.

The property has three parts:

1. The image to use as the border
2. Where to slice the image
3. Define whether the middle sections should be repeated or stretched

The `border-image` property takes the image and slices it into nine sections, like a tic-tac-toe board. It then places the corners at the corners, and the middle sections are repeated or stretched as you specify.

Note: For `border-image` to work, the element also needs the `border` property set!

Example:

```
#borderimg {  border: 10px solid transparent;  
  padding: 15px;  
  border-image: url(border.png) 30 round;}
```

Tip: The `border-image` property is actually a shorthand property for the `border-image-source`, `border-image-slice`, `border-image-width`, `border-image-outset` and `border-image-repeart` properties.

-- CSS border-image - Different Slice Values --

Different slice values completely changes the look of the border.

Example:

```
#borderimg1 {  border: 10px solid transparent;  
  padding: 15px;  
  border-image: url(border.png) 50 round;}  
  
#borderimg2 {  border: 10px solid transparent;  
  padding: 15px;  
  border-image: url(border.png) 20% round;}  
  
#borderimg3 {  border: 10px solid transparent;  
  padding: 15px;  
  border-image: url(border.png) 30% round;}
```

-- CSS Border Image Properties --

• `border-image` -- A shorthand property for setting all the border-image-properties
• `border-image-source` -- Specifies the path to the image to be used as a border
• `border-image-slice` -- Specifies how to slice the border image
• `border-image-width` -- Specifies the widths of the border image
• `border-image-outset` -- Specifies the amount by which the border image area extends beyond the border box
• `border-image-repeat` -- Specifies whether the border image should be repeated, rounded or stretched