//** HTML Formatting Elements **//

-   `<b>` - Bold text
-   `<strong>` - Important text
-   `<i>` - Italic text
-   `<em>` - Emphasized text
-   `<mark>` - Marked text
-   `<small>` - Smaller text
-   `<del>` - Deleted text
-   `<ins>` - Inserted text
-   `<sub>` - Subscript text
-   `<sup>` - Superscript text

//** HTML Quotation and Citation Elements **//

- `<abbr>` - Defines an abbreviation or acronym
- `<address>` - Defines contact information for the author/owner of a document
- `<bdo>` - Bi-Directional Override. Defines a section that is quoted from another source
- `<blockquote>` - Defines a section that is quoted from another source-- cite=""
- `<cite>` - Defines the title of a work
- `<q>` - Defines a short inline quotation

//** HTML Comments **//

<!-- Write you comments here -->

//** HTML Colors **//

HTML colors are specified with predefined color names, or with RGB, HEX, HSL, or HSLA values.

Background Color:

You can set the background color for HTML elements:
`<h1 style="background-color:DodgerBlue;">Hello World</h1>`

An RGB color value represents RED, GREEN, and BLUE light sources.

An RGBA color value is an extension of RGB with an Alpha channel (opacity).

--COLOR VALUES:

In HTML, a color can be specified as an RGB value, using this formula:

rgb(red, green, blue)

Each parameter (red, green, and blue) defines the intensity of the coor with a value between 0 and 255. 

This means that there are 256 x 256 x 256 = 16777216 possible colors!

For example, rgb(255, 0, 0) is displayed as red, because red is set to its highest value (255), and the other two (green and blue) are set to 0.

Another example, rgb(0, 255, 0) is displayed as green, because green is set to its highest value (255), and the other two (red and blue) are set to 0.

To display black, set all color parameters to 0, like this: rgb(0, 0, 0).

To display white, set all color parameters to 255, like this: rgb (255, 255, 255).

--SHADES OF GREY:

Shades of gray are often defined using equal values for all three paramenters.

--RGBA Color Values

RGBA color values are an extension of RGB values with an Alpha channel - which specifies the opacity of a color.

An RGBA color value is specified with:

rgba(red, green, blue, alpha)

The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all).

//** Hex Colors **//

In HTML, a color can be specified using a hexadecimal valye in the form:

#rrggbb

Where rr (red), gg (green) and bb (blue) are hexadecimal values between 00 and ff (same as decimal 0-255).

For example, #ff0000 is displayed as green, because green is set to its highest value (ff), and the other two (red and blue) are set to 00.

Another example, #00ff00 is displayed as green, because green is set to its highest value (ff), and the other two (red and blue) are set to 00.

To display black, set all color parameters to 00, like this: #000000

To display white, set all color parameters to ff, like this: #ffffff

//** HSL Colors **//

In HTML, a color can be specified using hue, saturation, and lightness (HSL) in the form:

-- hsl(hue, saturation, lightness)

Hue is a degree on the color whell from 0 to 360. 0 is red, 120 is green, and 240 is blue.

Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.

Lightness is also a percentage value, 0% is black, and 100% is white.

-- Saturation

Saturation can be described as the intensity of a color.

100% is pure color, no shades of gray

50% is 50% gray, but you can still see the color

0% is completely gray, you can no longer see the color

-- Lightness

The lightness of a color can be described as how much light you want to give the color, where 0% means no light (black), 50% means 50% light (neither dark nor light) 100% means full lightness (white).

-- Shades of Gray

Shades of gray are often defined by setting the hue and saturation to 0, and adjust the lightness from 0% to 100% to get darker/lighter shades

-- HSLA Color Values

HSLA color values are an extension of HSL color values with an Alpha channel - which specifies the opacity for a color.

An HSLA color value is specified with:

hsla(hue, saturation, lightness, alpha)

The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all):

//** HTML CSS **//

CSS Stands for Cascading Style Sheets.

CSS saves a lot of work. It can control the layout of multiple web pages all at once.

With CSS, you can control the color, font, the size of text, the spacing between elements, how elements are positioned and laid out, what background images or background colors are to be used, different displays for different devices and screen sizes, and much more!

Tip: The word cascading means that a sytle applied to a parent element will also apply to all children elements within the parent. So, if you set the color of the body text to 'blue', all headings, paragraphs, and other text elements within the body will also get the same color (unless you specify something else!)

-- Using CSS

CSS can be added to HTML documents in 3 ways:

• Inline - by using the `style` attribute inside HTML elements
• Internal - by using a `<style>` element in the `<head>` section
• External - by using a `<link>` element to link to an external CSS file

The most common way to add CSS, is to keep the styles in external CSS files.

-- Inline CSS

An inline CSS is used to apply a unique style to a single HTML element.

An inline CSS uses the `style` attribute of an HTML element.

The following example sets the text color of the `<h1>` element to blue, and the text color of the `<p>` element to red.

-- Internal CSS

An internal CSS is used to define a style for a single HTML page.

An internal CSS is defined in the `<head>` section of an HTML page, within a `<style>` element.

-- External CSS

An external style sheet is used to define the style for many HTML pages.

To use an external style sheet, add a link to it in the `<head>` section of each HTML page.

The external style sheet can be written in any text editor. The file must not contain any HTML code, and must be save with a .css extension.

-- CSS Colors, Fonts and Sizes

The CSS `color` property defines the text color to be used.

The CSS `font-family` property defines the font to be used.

The CSS `font-size` property defines the text size to be used.

-- CSS Border

The CSS `border` property defines a border around an HTML element.

-- CSS Padding

The CSS `padding` property defines a padding (space) between the text and the border.

-- CSS Margin

The CSS `margin` property defines a margin (space) outside the border.

-- Link to External CSS

External style sheets can be referenceed with a full URL or with a path relative to the current web page.