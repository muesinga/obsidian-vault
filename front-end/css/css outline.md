//** CSS Outline **//

An outline is a line that is drawn around elements, OUTSIDE the borders, to make the element "stand out".

![[Screen Shot 2022-03-16 at 8.23.21 AM.png]]

CSS has the following outline properties:

• `outline-style`
• `outline-color`
• `outline-width`
• `outline-offset`
• `ouline`

NOTE: Outline differs from borders! Unlike border, the outline is drawn outside the element's border, and may overlap other content. Also, the outline is NOT a part of the element's dimenions; the element's total wifth and height is not affected by the width of the outline.

//** CSS Outline Style **//

The `outline-style` property specifies the style of the outline, and can have one of the following values:

• `dotted` -- Defines a dotted outline
• `dashed` -- Defines a dashed outline
• `solid` -- Defines a solid outline
• `double` -- Defines a double outline
• `groove` -- Defines a 3D grooved outline
• `ridge` -- Defines a 3D inset outline
• `inset` -- Defines a 3D outset outline
• `none` -- Defines no outline
• `hidden` -- Defines a hidden outline

NOTE: None of the other outline properties will have ANY effect unless the `outline-style` property is set!

//** Ooutline Width **//

The `outline-width` property specifies the width of the outine, and can have one of the following values:

•   thin (typically 1px)
•  medium (typically 3px)
•  thick (typically 5px)
•  A specific size (in px, pt, cm, em, etc)

//** Outline Color **//

The `outline-color` property is used to set the color of the outline.

The color can be set by:

• name -- specify a color name, like "red"
• HEX -- specify a hex value, like "#ff0000"
• RGB -- specify a RGB value, like "rgb(255,0,0)"
• HSL -- specify a HSL value, like "hsl(0, 100%, 50%)"
• invert -- performs a color inverstion (which ensures that the outline is visible, regardless of color background)

//** Outline Shorthand **//

The `outline` property is a shorthand property for setting the following individual outine properties:

• `outline-width`
• `outline-style` (required)
• `outline-color`

The `outline` property is specified as one, two, or three values from the list above. The order of the values does not matter.

//** Outline Offset **//

The `outline-offest` property adds space between an outline and the edge/border of an element. The space between an element and its outline is transparent. 

-- All CSS Outline Properties --

`outline` -- A shorthand property for setting outline-width, outline-style, and outline-color in one declaration
`outline-color` -- Sets the color of an outline
`outline-offset` -- Specifies the space between an outline and the edge or border of an element
`outline-style` -- Sets the style of an outline
`outline-width` -- Sets the width of an outline