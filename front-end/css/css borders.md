//** CSS Borders **//

The CSS `border` properties allow you to specify the sytle, width, and color of an element's border.

-- CSS Border Sytle --

The `border-style` property specifies what kind of border to display.

The following values are allowed:

• `dotted` -- Defines a dotted border
• `dashed` -- Defines a dashed border
• `solid` -- Defines a solid border
• `double` -- Defines a double border
• `groove` -- Defines a 3D grooved border. The effect depends on the border-color value
• `ridge` -- Defines a 3D ridged border. The effect depends on the border-color value
• `inset` -- Defines a 3D inset border. The effect depends on the border-color value
• `outset` -- Defines a 3D outset border. The effect depends on the border-color value
• `none` -- Defines no border
• `hidden` -- Defines a hidden border

The `border-style` property can have from one to four values (for the top border, right border, bottom border, and left border).

NOTE: None of the OTHER CSS border properties will have ANY effect unless the `border-style` property is set!

//** Border Width **//

The `border-width` property specifies the width of the four borders.

The width can be set as a specific size (in px, pt, cm, em, etc) or by using one of the three pre-defined values: thin, medium, or thick.

//** Specific Side Widths **//

The `border-width` property can have from on to four values (for the top border, right border, bottom border, and the left border)

//** Border Color **//

The `border-color` property is used to set the color of the four borders.

The color can be set by:

• name - specify a color name, like "'red'"
• HEX - specify a HEX value, like "#ff0000"
• RGB - specify a RGB value, like "rgb(255,0,0)"
• HSL - specify a HSL value, like "hsl(0, 100%, 50%)"
• transparent

NOTE: If `border-color` is not set, it inherits the color of the element.

-- Specific Side Colors --

The `border-color` property can have from one to four values(for the top border, right border, bottom border, and the left border).

-- HEX, RGB, HSL Values --

The color of the border can also be specified using a hexadecimal value (HEX), as well as RBG and HSL values.

//** Border Sides **//

From the examples on the previous pages, you have seen that it is possible to specify a different border for each side.

In CSS, there are also properties for specifying each of the borders (top, right, bottom, and left)

Example:

```
p { border-top-style: dotted;  
  border-right-style: solid;  
  border-bottom-style: dotted;  
  border-left-style: solid;}
```

The example above gives the same result as this:

```
p { border-style: dotted solid;}
```

So, here is how it works:

If the `border-style` property has four values:
	• border-style: dotted solid double dashed;
		- top border is dotted
		- right border is solid
		- bottom border is double
		- left border is dashed

If the `border-style` property has three values:
	• border-style: dotted solid double;
		- top border is dotted
		- right and left borders are solid
		- bottom border is double
		
If the `border-style` property has two values:
	• border-style: dotted solid;
		- top and bottom borders are dotted
		- right and left borders are solid
		
If the `border-style` property has one value:
	• border-style: dotted;
		- all four border are dotted
		
```
/* Four values */  
p { border-style: dotted solid double dashed;}  
  
/* Three values */  
p { border-style: dotted solid double;}  
  
/* Two values */  
p { border-style: dotted solid;}  
  
/* One value */  
p { border-style: dotted;}
```

The `border-style` property is used in the example above. However, it also works with `border-width` and `border-color`.

//** Border Shorthand **//

Like you saw in the previous page, there are many properties to consider when dealing with borders.

To shorted the code, it is also possible to specify all the individual border properties in one property.

The `border` property is a shorthand property for the following individual border properties:

• `border-width`
• `border-style`
• `border-color`

Example:

```
p { border: 5px solid red;}
```

You can also specify all the individual border properties for just one side:

```
p { border-left: 6px solid red;  
  background-color: lightgrey;}
```

-- Bottom Border --

```
p { border-bottom: 6px solid red;  
  background-color: lightgrey;}
```

