//** CSS Margins **//

-- CSS Margins --

The CSS `margin` properties are used to create space around elements, outside of any defined borders.

With CSS, you have full control over the margins. There are properties for setting the margin for each side of a element (top, right, bottom, and left).

-- Margin - Individual Sides --

CSS has properties for specifying the margin for each side of an element:

• `margin-top`
• `margin-right`
• `margin-bottom`
• `margin-left`

All the margin properties can have the following values:

• auto - the browser calculates the margin
• length - specifies a margin in px, pt, cm, etc.
• % - specifies a margin in % of the width of the containing element
• inherit - specifies that the margin should be inherited from the parent element

TIP: Negative values are allowed/

Example:

```
p { margin-top: 100px;  
  margin-bottom: 100px;  
  margin-right: 150px;  
  margin-left: 80px;}
```

-- Margin - Shorthand Property --

To shorten the code, it is possible to specify all the margin properties in one property.

The `margin` property is a shorthand property for the following indiviual margin properties:

• `margin-top`
• `margin-right`
• `margin-bottom`
•`margin-left`

Here is how it works:

If the `margin` property has four values, use the short hand:

`p { margin: 25px 50px 75px 100px;}`
 (Top, Right, Bottom, and Left)
 
 If the `margin` property has two values:
 
 `p { margin: 25px 50px;}`
 
 If the `margin` property has one value:
 
 `p { margin: 25px;}`
 
 -- The auto Value --
 
 You can set the margin property to `auto` to horizontally center the element within its container.
 
 The element will then take up the specified width, and the remaining space will be split equally between the left and right margins.
 
 ```
 div { width: 300px;  
  margin: auto;  
  border: 1px solid red;}
 ```
 
 -- The inherit Value --
 
 This example lets the left margin of the `<p class="ex1">` element be inherited from the parent element (`<div>`):
 
 ```
 div { border: 1px solid red;  
  margin-left: 100px;}  
  
p.ex1 { margin-left: inherit;}
 ```
 
-- Margin Collapse --

Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins.

This does not happen on left and right margins! Only top and bottom margins!

-- CSS Padding --

The CSS `padding` properties are used to generate space around an element's content, inside of any defined borders.

With CSS, you have full control over the padding. There are properties for setting the padding for each side of an element (top, right, bottom, and left).

-- Padding - Individual Sides --

CSS has properties for specifying the padding for each side of an element:

• `padding-top`
• `padding-right`
• `padding-bottom`
• `padding-left`

All the padding properties can have the following values:

• length - specifies a padding in px, pt, cm, etc.
• % - specifies a padding in % of the width of the containing element
• inherit - specifies that the padding should be inherited from the parent element

NOTE: Negative values are not allowed. 

Example:

Set different padding for all four sides of a `<div>` element:

```
div { padding-top: 50px;  
  padding-right: 30px;  
  padding-bottom: 50px;  
  padding-left: 80px;}
```

-- Padding - Shorthand Property --

To shorten the code, it is possible to specify all the padding in one property.

Thr `padding` property is a shorthand property for the following individual padding properties:

• `padding-top`
• `padding-right
• `padding-bottom
• `padding-left`

Example:

`div { padding: 25px 50px 75px 100px;}`
(Top, Right, Bottom, Left)

If the `padding` property had three values:

`div { padding: 25px 50px 75px;}`
(top, right/left, bottom)

If the `padding` property has two values:

`div { padding: 25px 50px;}`
(top/bottom, left/right)

If the `padding` property has one value:

`div { padding: 25px;}`
(all four sides)

-- Padding and Element Width --

The CSS `width` property specifies the width of the element's content area. The content area is the portion inside the padding, border, and margin of an element.

So, if an element has a specified width, the padding added to that element will be added to the total width of the element. This is often an undersirable result.

To keep the width no matter the amount of padding, you can use the `box-sizing` property. This causes the element to maintain its width; if you increase the padding, the available content space will decrease.

//** CSS Height/Width **//

-- CSS Setting height and width --

The `height`and `width` properties are used to set the height and width of an element.

The height and width properties do not include padding, borders, or margins. It sets the height/width of the area iside the padding, border, and margin of the element.

-- CSS height and width Values --

The `height` and `width` properties may have the following values:

• `auto` -- This is default. The browser calculates the height and width
• `length` -- Defines the height/width in px, cm etc.
• `%` -- Defines the height/width in percent of the containing block
• `initial` -- Sets the height/width to its default value
• `inherit` -- The height/width will be inherited from its parent value

-- Setting max-width --

The `max-width` property is used to set the maximum width of an element.

The `max-width` can be specified in length values, like px, cm, etc., or in percent (%) of the containing block, or set to none (this is default. Means that there is no maximum width).

The problem with the `<div>` above occurs when the browser window is smaller than the width of the lement (500px). The browser then adds a horizontal scrollbar to the page.

Using `max-width` instead, in this situation, will improve the browser's handling of small windows.

//** All CSS Dimension Properties **//

• height -- Sets the height of an element
• max-height -- Sets the maximum height of an element
• max-width -- Sets the maximum width of an element
• min-height -- Sets the minimum height of an element
ª min-width -- Sets the minimum width of an element
• width -- Sets the width of an element