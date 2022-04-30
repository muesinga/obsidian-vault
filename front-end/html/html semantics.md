//** HTML Semantics **//

Semantic elements = elements with a meaning.

-- What are Semantic Elements? --

A semantic element clearly describes its meaning to both the browser and the developer.

Examples of non-semantic ekenents `<div>` and `<span>` - Tells nothing about its content.

Examples of semantic elements: `<form>` , `<table>`, and `<article>` - Clearly defines its content.

-- Semantic Elements in HTML --

Many web sites contain HTML code like: `<div id="nav"><div class="header"><div id="footer>"` to indicate navigation, header, and footer.

In HTML there are some semantic elements that can be used to define different parts of a web page:

• `<articl>`
• `<aside>`
• `<details>`
• `<figcaption>`
• `<figure>`
• `<footer>`
• `<header>`
• `<main>`
• `<nav>`
•`<section>`
• `<summary>`
• `<time>`

-- HTML `<section>` Element --

The `<section>` element defines a section in a document.

A section is a thematic grouping of content, typicaly with a heading.

A web page could normally be split into sections for introduction, content, and contact information.

-- HTML `<article>` Element --

The `<article>` element specifies independent, self-contained content.

An artice should make sense on its own, and it should be possible to distribute it independently from the rest of the web site.

Examples of where an `<articl>` element can be used:

• Forum post
• Blog post
• Newspaper article

-- Nest `<article>` in `<section>` or Vice Versa? --

The `<article>` element specifies independent, self-containted conent.

The `<section>` element defines section in a document.

Can we use the definitions to decide how to nest those elements? No, we cannot!

So, you wil find HTML pages with `<section>` elements containing `<article>` elements, and `<article>` elements containing `<section>` elements.

//** HTML `<header>` Element **//

The `<header>` element represents a container for introoductory content or a set of navigational links.

A `<header>` element typically contains:

• one or more heading elements
• logo or icon
• authorship information

Note: You can have several `<header>` elements in one HTML document. However, `<header>` cannot be placed within a `<footer>`, `<address>` or another `<header>` element.

//** HTML `<footer>` Element **//

The `<footer>` element defines a footer for a document or section.

A `<footer>` element typicatlly contains:

• authorship information
• copyright information
• contact information
• sitemap
• back to top links
• related documents

You can have several `<footer>` elements in one document. 

//** HTML `<nav>` Element **//

The `<nav>` element defines a set of navigation links.

Notice that NOT all links of a document should be inside a `<nav>` element. The `<nav>` element is intended only for major block of navigation lnks.

Browsers, such as screen readers for disabled users, can use this element to determine whether to omit the initial rendering of this content.

//** HTML `<aside>` Element **//

The `<aside>` element defines some content aside from the content it is placed in (like a sidebar).

The `<aside>` content should be indirctly related to the surrounding content.

//** HTML `<figure>` and `<figcaption>` Elements **//

The `<figure>` tag specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.

The `<figcaption>` tag defines a caption for a `<figure>` element. The `<figcaption>` element can be placed as the first or as the last child of a `<figure>` element.

The `<img>` element defines the actual image/illustration.

//** Semantic Elements in HTML **//

`<article>` -- Defines independent, self-contained content
`<aside>` -- Defines content aside from the page content
`<details>` -- Defines additional details that the user can view or hide
`<figcaption>` -- Defines a caption for a `<figure>` element
`<figure>` -- Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
`<footer>` -- Defines a footer for a document or section
`<header>` - Specifies a header for a document or section
`<main>` -- Specifies the main content for a document
`<mark>` -- Defines marked/highlighted text
`<nav>` -- Defines naviagtion links
`<section>` -- Defines a section in a document
`<summary>` -- Defines a visible heading for a `<details>` element
`<time>` -- Defines a date/time