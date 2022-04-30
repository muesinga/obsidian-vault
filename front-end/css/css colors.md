//** CSS Colors **//

Colors are specified using predefined color names, or RGB, HEX, HSL, RGBA, HSLA values.

You can set the background, text, and border color of HTML elements.

//** RGB **//

In CSS, a color can be specified as an RGB value, using this formula: 

rgb(red, green, blue)

Each parameter (red, green, and blue) defines the intensity of the color between 0 and 255.

For example, rgb(255, 0, 0) is displayed as red, because red is set to its highest value (255) and the others are set to 0.

To display black, set all color parameters to 0, like this: rgb(0, 0, 0).

To display white, set all color parameters to 255, like this: rgb(255, 255, 255).

//** RGBA Value **//

RGBA color values are an extension of RGB color values with an alpha channel - which specifies the opacity for a color.

An RGBA color value is specified with:

rgba(red, green, blue, alpha)

The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all).

//** Hex **//

A color can be specified using a hexadecimal value in the form:

#rrggbb 

Where rr (red), gg (green) and bb (blue) are hexadecimal values between 00 and ff (same as decimal 0-255).

For example, #ff0000 is displayed as red, because red is set to its highest value (ff) and the others are set to the lowest value (00).

Shades of gray are often defined using equal values for all the 3 light sources:

Examples:

#000000

#3c3c3c

#787878

#b4b4b4

#f0f0f0

#ffffff

//** HSL **//

form: hsl(hue, saturation, lightness) Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.

hsl (hue, saturation, lightness)

Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.

Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.

Lightness is also a percentage, 0% is black, 50% is neither light or dark, 100% is white.

-- Saturation --

Saturation can be described as the intensity of a color.

100% is pure color, no shades of gray.

50% is 50% gray, but you can still see the color.

0% is completely gray, you can no longer see the color.

-- Lightness --

The lightness of a color can be described as how much light you want to give the color, where 0% means no light (black), 50% means 50% light (neither dark nor light) 100% means full lightness (white).

Shades of gray are often defined by setting the hue and saturation to 0, and adjust the lightness from 0% to 100% to get darker/lighter shades.

-- HSLA Value --

HSLA color values are an extension of HSL color values with an alpha channel - which specifies the opacity for a color.

An HSLA color value is specified with:

hsla(hue, saturation, lightness, alpha)

The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all).

