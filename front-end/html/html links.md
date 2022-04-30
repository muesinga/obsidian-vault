//** HTML Links **//

HTML Links - Hyperlinks

HTML links are hyperlinks.

The HTML `<a>` tag defines a hyperlink. It has the following syntax:
	
	`<a href="url">link text</a>`
	
The most important attribute of the `<a>` element is the href attribute, which indicates the link's destination.

-- TARGET ATTRIBUTE

The `target` attribute specifies where to open the linked document.

The `target` attribute can have one of the following values:

1) `_self` - Default. Opens the document in the same window/tab as it was clicked
2) `_blank`- Opens the document in the parent frame
3) `_top` - Opens the document in the full body of the window

-- ABSOLUTE URLS vs. RELATIVE URLS

A local link (a link to a page within the same website) is specified with a relative URL (without the "https://www" part).

//** HTML Link Colors **//

By default:

	• An unvisited link is underlined and blue
	• A visted link is underlined and purple
	• An active link is underlined and red
	
You can change the link state colors, by using CSS.

//** Link Bookmarks **//

HTML links can be used to create bookmarks, so that readers can jump to specidic parts of a web page.

-- Create a Bookmark in HTML

Bookmarks can be useful if a web page is very long

To create a bookmark - first create the bookmark, then add a link to it.

When the link is clicked, the page wills croll down or up to the location with the bookmark.

Example

First, use the `id` attribute to create a bookmark

`<h2 id="C4">Chapter 4</h2>`

Then, add a link to the bookmark ("Jump to Chapter 4")

`<a href="#C4">Jump to Chapter 4</a>`