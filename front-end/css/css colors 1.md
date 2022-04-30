//** CSS Colors **//

CSS supports 140+ color names, HEX values, RGB values, RGBA values, HSL values, HSLA values, and opacity

-- RGBA Colors --

RGBA color values are an extension of RBG color values with an alpha channel - which specifies the opacity for a color. 

An RGBA color value is specified with rgba(redm green, blue, alpha). The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

The following example defines different RGBA colors:

```
#p1 {background-color: rgba(255, 0, 0, 0.3);}  /* red with opacity */  
#p2 {background-color: rgba(0, 255, 0, 0.3);}  /* green with opacity */  
#p3 {background-color: rgba(0, 0, 255, 0.3);}  /* blue with opacity */
```

-- HSL Colors --

HSL stands for Hue, Saturation, and Lightness.

An HSL color value is specified with: hsl(hue, saturation, lightness).

1, Hue is a degree on the color wheel (from 0 to 360):
	• 0 (or 360) is red
	• 120 is green
	• 240 is blue
2, Saturation is a percentage value: 100% is the full color.
3, Lightness is also a percentage; 0% is dark (black) and 100% is white.

The following example defines different HSL colors:

```
#p1 {background-color: hsl(120, 100%, 50%);}  /* green */  
#p2 {background-color: hsl(120, 100%, 75%);}  /* light green */  
#p3 {background-color: hsl(120, 100%, 25%);}  /* dark green */  
#p4 {background-color: hsl(120, 60%, 70%);}   /* pastel green */
```

-- HSLA Colors --

HSLA color values are an extensio of HSL color values with an alpha channel - which specifies the opacuty for a color.

An HSLA color value is specified with: hsla(hue, saturation, lightness, alpha), where the alpha parameter defines the opacity. The alpha paramenter is a numbner 0.0 (fully transparent) and 1.0 (fully opaque).

The following example defines different HSLA colors:

```
#p1 {background-color: hsla(120, 100%, 50%, 0.3);}  /* green with opacity */  
#p2 {background-color: hsla(120, 100%, 75%, 0.3);}  /* light green with opacity */  
#p3 {background-color: hsla(120, 100%, 25%, 0.3);}  /* dark green with opacity */  
#p4 {background-color: hsla(120, 60%, 70%, 0.3);}   /* pastel green with opacity */
```

-- Opacity --

The CSS `opacity` property sets the opacity for whole element (both background color and text will be opaque/transparent).

The `opacity` property value must be a number between 0.0 (fully transparent) and 1.0 (fully opaque).

The following example shows different elements with opacity:

```
#p1 {background-color:rgb(255,0,0);opacity:0.6;}  /* red with opacity */  
#p2 {background-color:rgb(0,255,0);opacity:0.6;}  /* green with opacity */  
#p3 {background-color:rgb(0,0,255);opacity:0.6;}  /* blue with opacity */
```