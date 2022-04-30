//** CSS Pseudo-Elements **//

A CSS pseudo-element is used to style specified parts of an element.

For example, it can be used to:

• Style the first letter, or line, of an element
• Insert content before, or after, the content of an element

-- The ::first-line Pseudo-element --

The `::first-line` pseudo-element is used to add a special style to the first line of a text.

The following example formats the first line of the text in all `<p>` elements:

```
p::first-line { color: #ff0000;  
  font-variant: small-caps;}
```

Note: The `::first-line` pseduo-element can only be applied to block-level elements.

The following properties apply to the `::first-line` pseudo-element:

• font properties
• color properties
• background properties
• word-spacing
• letter-spacing
• text-decoration
• vertical-align
• text-transform
• line-height
• clear

Notice the double colon notation - `::first-line` versus `:first-line`

The double colon replaces the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C is distinguish between pseudo-classes and pseduo-elements.

The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1.

For backwards compatibility, the single-colon syntax is acceptable for CSS2 and CSS1 pseudo-elements.

-- The ::first-letter Pseudo-element --

The `::first-letter` pseudo-element is used to add a special style to the first letter of a text.

The following example formats the first letter of the text in all `<p>` elements:

```
p::first-letter { color: #ff0000;  
  font-size: xx-large;}
```

Note: The `::first-letter` pseudo-element can only be applied to block-level elements.

The following properties apply to the ::first-letter pseudo-element:

• font properties
• color properties
• background properties
• margin properties
• padding properties
• border properties
• text-decoration
• vertical-align (only if "float" is "none")
• text-transform
• line-height
• float
• clear

-- Pseudo-elements and CSS Classes --

Pseudo-elements can be combined with CSS classes:

```
p.intro::first-letter { color: #ff0000;  
  font-size: 200%;}
```

The example above will display the first letter of paragraphs with class="intro", in red an in a larger size.

-- Multiple Pseudo-elements --

Several pseudo-elements can also be combined.

In the following example, the first letter of a paragraph will be red, in an xx-large font size. The rest of the first line will be blue, and in small-caps. The rest of the paragraph will be the default font size and color:

```
p::first-letter { color: #ff0000;  
  font-size: xx-large;}  
  
p::first-line { color: #0000ff;  
  font-variant: small-caps;}
```

-- CSS - The ::before Pseudo-element --

The `::before` pseudo-element can be used to insert some content before the content of an element.

The following example inserts an image before the content of each `<h1>` element:

`h1::before { content: url(smiley.gif);}`

-- CSS - The ::after Pseudo-element --

The `::after` pseudo-element can be used to insert some content after the content of an element.

The following example inserts an image after the content of each `<h1>` element:

`h1::after { content: url(smiley.gif);}`

-- CSS - The ::selection Pseudo-element --

The `::selection` pseudo-element matches the portion of an element that is selected by a user.

The followng CSS properties can be applied to `::seleciton`: `color`, `background`, `cursor`, and `outline`.

The following example makes the selected text red on a yellow background:

```
::selection { color: red;  
  background: yellow;}
```