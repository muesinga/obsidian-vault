//** CSS Units **//

CSS has several different units for expressing a length.

Many CSS properties take "length" values, such as `width`, `margin`, `padding`, `font-size`, etc.

Length is a number followed by a length unit, such as `10px`, `2em`, etc.

Example:

Set different length values, using px (pixels):

```
h1 {  font-size: 60px;}  
  
p {  font-size: 25px;  
  line-height: 50px;}
```

Note: A whitespace cannot appear between the number and the unit. However, if the value is `0`, the unit can be omitted.

For some CSS properties, negative lengths are allowed.

There are two types of length units: absolute and relative.

//** Absolute Lengths **//

The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.

Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output 
medium is known, such as for print layout.

• cm -- centimeters
• mm -- millimeters
• in -- inches (1in = 96px = 2.54cm)
• px --  pixels (1px = 1/96th of 1in)
• pt -- points (1pt = 1/72 of 1in)
• pc -- picas (1pc = 12pt)

//** Relative Lengths **//

Relative lengths units specify a length relative to another length property. Relative length units scales better between different rendering mediums.

• em -- relative to the font-size of the element (2em means 2 times the size of the current font)
• ex -- relative to the x-height of the current font (rarely used)
• ch -- relative to width of the "0" (zero)
• rem -- relative to font-size of the root element
• vw -- relative to 1% of the height of the viewport
• vmin -- relative to 1% of viewport's smaller dimension
• vmax -- relative to 1% of viewport's larger dimension
• % -- relative to the parent element

Tip: The em and rem units are practical in creating perfectly scalable layout!

Viewport = the browser size. If the viewport is 50cm wide, 1vw = 0.5cm.