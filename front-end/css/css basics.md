//** CSS Syntax **//

A CSS rule-set consists of a selector and a declaration block:

The selector points to the HTML element you want to style/

The declatation block conations one or more declarations separated by semicolons.

Each declaration incldues a CSS property name and a value, separated by a colon.

Multiple CSS declatations are separated with semicolons, and declaration blocks are surrounded by curly braces.

//** CSS Selectors **//

CSS selectors are used to "find" (or select) the HTML elements you want to style.

We can divide CSS selectors into five catagories:

• Simple selectors (select elements based on name, id, class)
• Combinator selectors (select elements based on a specific relationship between them)
• Pseudo-class selectors (select elements based on a certain state)
• Pseudo-elements selectors (select and style a part of an element)
• Attribute selectors (select elements based on attribute or attribute value)

-- The CSS element Selector --

The element selector selects HTML elements based on the element name.

-- The CSS id Selector --

The id selector uses the id attribute of an HTML element to select a specific element.

The id of an element is unique within a page, so the id selector is used to select one unqiue element!

To seleect an element with a specific id, write a hash (#) character, followed by the id of the element.

-- The CSS class Selector --

The class selector selects HTML elements with a specific class attribute.

To select elements with a specific class, write a period (.) character, followed by the class name.

You can also specify that only specific HTML elements should be affected by a class.

In this example only `<p>` elements with class="center" will be red and center-aligned.

```
p.center { text-align: center;  
  color: red;}
```

HTML elements can also refer to more than one class.

In this example the `<p>` element will be styled according to class="center" and to class="large"

-- The CSS Universal Selector --

The universal selector (*) selects all HTML elements on the page.

-- The CSS Grouping Selector --

The grouping selector selects all the HTML elements with the same style definitions.

Look at the following CSS code (the h1, h2, and p elements have the same style definitionsl)

```
h1, h2, p { text-align: center;  
  color: red;}
```

-- All CSS Simple Seletors --

#id -- selects the element with id=""
.class -- selects all elements with class="intro"
p.intro -- selects only `<p>` elements with class="intro"
* -- selects all elements
element -- selects all of an HTML element
element, element

//** How to Add CSS **//

When a browser reads a style sheet, it will format the HTML document according to the infomation in the style sheet.

-- Three Ways to Insert CSS --

There are three ways of inserting a style sheet:

• External CSS
• Internal CSS
• Inline CSS

-- External CSS --

With an external style sheet, you can change the look of an entire website by changing just one file!

Each HTML page must include a reference to the external style sheet file incside the `<link>` element, inside the head section.

An external style sheet can be written in any text editor, and must be saved with a .css extension.

The external .css file should not contain any HTML tags.

-- Internal CSS --

An internal style sheet may be used if one HTML page has a unique style.

The internal style is defined inside the `<style>` element, inside the head section.

-- Multiple Style Sheets --

If some properties have been defined for the same selector (element) in different style sheets, the value from the last read style sheet will be used.

-- Cascading Order --

What style will be used when there is more than one style specified for an HTML element?

All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

• Inline style (inside an HTML element)
• External and internal style sheets (in the head section)
• Browser default

So, an inline style has the highest priority, and will override external and internal styles and browser defaults.

-- CSS Comments --

Comments are ued to explain the code, and may help when you edit the source code at a later date.

Comments are ignored by browsers.

A CSS comment is placed inside the `<style>` element and starts with `/*` and ends with `*/`

You can add comments wherever you want in the code.

Comments can also span multiple lines

//** HTML and CSS Comments **//

From the HTML tutuorial, you learned that you can add comments to your HTML source by using the `<!--...-->` syntax.
