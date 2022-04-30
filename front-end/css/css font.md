//** CSS Font **//

-- Font Selection is Important  --

Choosing the right font has a huge impact on ho the readers experience a website.

The right font can create a strong identity for your brand. 

Using a font that is easy to read are important. The font adds value to your text. It is also important to choose the correct color and text size for the font.

-- Generic Font Families --

In CSS there are five generic font families:

1) Serif fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.
2) Sans-serif fonts have clean lines (no small strokes attached). They create a modern and minimilistic look.
3) Monospace fonts - here all the letters have the same fixed width. They create a mechanical look.
4) Cursive fonts imitate human handwriting.
5) Fantasy fonts are decorative/playful fonts.

All the different font names belong to one of the generic font families.

-- The CSS font-family Property --

In CSS, we use the `font-family` property to specify the font of a text.

The `font-family` property should hold several font names as a "fallback" system, to ensure maximum compatibility between browsers/operating systems. Start with the font you want, and end with a generic family (to let the browser pick a similar font in the generic family, if no other fonts are available). The font names should be separated with comma.

//** Font Web Safe **//

Web safe fonts are fonts that are universally installed across all browsers and devices.

-- Fallback Fonts --

However, there are no 100% completetly web safe fonts. There is always a chance that a font is not found or is not installed properly.

Therefore, it is very important to always use fallback fonts.

This means that you should add a list of similar "backup fonts" in the `font-family` property. If the first font does not work, the browser will try the next one, and the next one, and so on. Always end the list with a generic font family name.

EXAMPLE -- Here, there are three font types: Tahoma, Verdana, and sans-serif. The second and third fonts are backups, in case the first one is not found.

`p {font-family: Tahoma, Verdana, sans-serif;}`

-- Arial (sans-serif) --

Arial is the most widely used font for both online and printed media. Arial is also the default font in Google Docs.

Arial is one of the safest web fonts, and it is available on all major operating systems.

-- Verdana (sans-serif) --

Verdanais a very popular font. Verdana is easily readable even for small font sizes.

-- Helvetica (sans-serif) --

The Helvetica font is loved by designers. It is suitable for many types of business.

-- Tahoma (sans-serif) --

The Tahoma font has less space between the characters.

-- Trebuchet MS (sans-serif) --

Trebuchet MS was designed by Microsoft in 1996. Use this font carefully. Not supported by all mobile operating systems.

-- Times New Roman (serif) --

Times New Roman is one of the most recognizable fonts in the world. It looks professional and is used in many newspapers and "news" websites. It is also the primary font for Windows devices and applications.

-- Georgia --

Georgia is an elegant serif font. It is very readable at different font sizes, os it is a good candidate for mobile-responsive design.

-- Garamons (serif) --

Garamond is a classical font used for many printed books. It has a timeless look and good readability.

-- Courier New (monospace) --

Courier New is the most widely used monospace serif font. Courier New is often used with coding displays, and many email providers use it as their default font. Courier New is also the standard font for movie screenplays.

-- Brush Script MT (cursive) --

The Brush Script MT font was designed to mimic handwriting. It is elegant and sophisticated, but can be hard to read. Use it carefully.

//** Font Style **//

The `font-style` property is mostly used to specify italic text.

This property has three values:

• normal - The text is shown normally
• italic - The text is shown in italics
• oblique - The text is "leaning" (oblique is very similar to italic, but less supported)

-- Font Weight --

The `font-weight` property specifies the weight of a font.

-- Font Variant -- 

The `font-variant` property specifies whether or not a text should be displayed in a small-caps font.

In a small-caps font, all lowercase letters are converted to uppercase letters. However, the converted uppercase letters appears in a smaller font size than the original uppercase letters in the text.

-- Font Size --

The `font-size` property sets the size of the text.

Being able to manage the text size is important in web design. However, you should not use font size adjustments to make paragraphs looks like headings, or headings look like paragraphs.

Always use the proper HTML tags, like `<h1> - <6>` for headings and `<p>` for paragraphs.

The font-size value can be absolute, or relative size.

Absolute size:

• Sets the text to a specified size
• Does not allow a user to change the text size in all browsers (bad or accesibility reasons)
• Absolute size is useful when the physical size of the output in known

NOTE: If you do not specify a font size, the defauly size for normal text, like paragraphs, is 16px (16px=1em).

-- Set Font Size With Pixels --

Setting the text size with pixels gives you full control over the text size.

-- Set Font Size With Em --

To allow users to resize the text (in the browser menu), many developers use em instead of pixels.

1em is equal to the current font size. The default text size in browsers is 16px. So, the default size of 1em is 16px.

The size can be calculated from pixels to em using the formula: pixels/16=em

In the example above, the text size in em is the same as the previous example in pixels. However, with the em size, it is possible to adjust the text size of all browsers.

Unfortunately, there is still a problem with older versions of Internet Explorer. The text becomes larger than it should when made larger, and smaler than it should when made smaller.

-- Use a Combination of Percent and Em --

The solution that workds in all browsers, is to set a default font-size in percent for the `<body>` element:

```
body { font-size: 100%;}  
  
h1 { font-size: 2.5em;}  
  
h2 { font-size: 1.875em;}  
  
p { font-size: 0.875em;}
```

This will allow the same text size in all browsers, and allow all browsers to zoom or resize the text.

-- Responsive Font Size --

The text size can be set with a `vw` unit, which means the "viewport width". 

Example:

`<h1 style="**font-size:10vw**">Hello World</h1>

NOTE: Viewport is the browser window size. 1vw = 1% of viewport width. If the viewport is 50cm wide, 1vw is 0.5cm.

//** Font Google **//

If you do not wnat to use any of the standard fonts in HTML, you can use Google Fonts.

Google Fonts are free to use, and have more than 1000 fonts to choose from.

-- How To Use Google Fonts --

Just add a special style sheet link in the `<head>` sectino and then refer to the font in the CSS.

Example:

```
<head>  
**<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">**  
<style>  
body { font-family: "Sofia", sans-serif;}  
</style>  
</head>
```

NOTE: When specifying a font in CSS, always list at minimum one fallback font (to avoid unexpected behaviors).

-- Use Multiple Google Fonts --

To use multiple Google fonts, just separate the font names with a pipe character (|).

Example:

```
<head>  
**<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide|Sofia|Trirong">**  
<style>  
h1.a {font-family: "Audiowide", sans-serif;}  
h1.b {font-family: "Sofia", sans-serif;}  
h1.c {font-family: "Trirong", serif;}  
</style>  
</head>
```

NOTE: Requesting multiple fonts may slow down your web pages! So be careful about that.

-- Styling Google Fonts --

You can style Google Fonts as you like, with CSS

Google have also enabled different font effects that you can use.

First add `effect=*effectname*` to the Google API, then add a special class name to the element that is going to use the special effect. The class name always starts with `font-effect-` and ends with the `*effectname*`

Example:

Add the fire effect to the "Sofia" font:

```
<head>  
**<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia&effect=fire">**  
<style>  
body { font-family: "Sofia", sans-serif;  
  font-size: 30px;}  
</style>  
</head>  
<body>  
  
<h1 class="font-effect-fire">Sofia on Fire</h1>  
  
</body>
```

You can use a pipe (|) character to request multiple effects.

//** Font Pairings **//

-- Font Pairing Rules --

1) Compliment
		-- It is always safe to find font pairings that complement on another.
			A great font combination should harmonize, without beeing too similar or too different.
			
2) Use Font Superfamilies
		-- A font superfamily is a set of fonts designed to work well together. So, using different fonts within the same superfamily is safe.

3) Contrast is King
		-- Two fonts that are too similar will often conflict. However, contrasts, done the rightw ay, brings out the best in each font.
		Combining serif and sans serif is a well known combination.
		A strong superfamily includes both serif and sans serif variations of the same font.
		
4) Choose Only One Boss
		One font should be the boss. This establishes a hierarchy for the fonts on your page.  This can be achieved by varying the size, weight and color.
		
Example:

Here "Georgia" is the boss:

```
body { background-color: black;  
  font-family: Verdana, sans-serif;  
  font-size: 16px;  
  color: gray;}  
  
h1 { font-family: Georgia, serif;  
  font-size: 60px;  
  color: white;}
```

-- Popular Font Pairings --

Georgian and Verdana

Helvetica and Garamond

(Google Fonts)

Merriweather and Open Sans

Ubuntu and Lora

Abril Fatface and Poppins

Cinzel and Fauna One

Fjalla One and Libre Baskerville

Space Mono and Multi

Spectral and Rubik

Oswald and Noto Sans

//** Font Shorthand **//

To shorten the code, it is also possible to specify all the individual font properties in one property.

The `font` property is a shorthand property for:

• `font-style`
• `font-variant`
•`font-weight`
•`font-size/line-height`
•`font-family` 

NOTE: The `font-size` and `font-family` values are required. If one of the other values is missing, their defaulr value are used.