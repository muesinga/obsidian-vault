//** CSS Max-Width **//

A block-level element always takes up the full width available (stretches out to the left and rigth as far as it can).

Setting the `width` of a block-level element will prevent it from stretching out to the edges of its container. Then, you can set the margins to auto, to horizontally center the element within its container. The element wil take up the specified width, and the remaining space will be split equally between the two margins:

NOTE: The problem with the `<div>` above occurs when the browser window is smaller than the width of the element. The browser adds a horizontal scrollbar to the page.

Using `max-width` instead, in this situation, will improve the browser's handling of small windows. This is important when making a site usable on small devices.

TIP: Resize the browser window to less than 500px wide, to see the difference between the two divs!

//** CSS Position **//

The `position` property specifices the type of positioning method used for an element (static, relative, fixed, absolute or sticky).

-- The position Property --

The `position` property specifies the type of positioning method used for an element.

There are five different position values:

• `static`
• `relative`
• `fixed`
• `absolute`
• `sticky`

Elements are then positioned using the top, bottom, left, and right properties. However, these properties will not work unless the `position` property is set first. They also work differently depending on the position value.

-- postion: static; --

HTML elements are positioned static by default.

Static positioned elements are not affected by the top, bottom, left and right properties.

An element with `position: static;` is not positioned in any special way; it is always positioned according to the normal flow of the page.

```
div.static { position: static;  
  border: 3px solid #73AD21;}
```

-- position: relative; --

An element with `position: relative;` is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element. 

This `<div>` element has position: relative;

```
div.relative { position: relative;  
  left: 30px;  
  border: 3px solid #73AD21;}
```

-- position: fixed; --

An element with `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the pageis scrolled. The top, right, bottom, and left properties are uesed to position the element.

A fixed element does not leave a gap in the page where it would normally have been located.

Notice the fixed element in the lower-right corner of the page. Here is the CSS that is used:

```
div.fixed { position: fixed;  
  bottom: 0;  
  right: 0;  
  width: 300px;  
  border: 3px solid #73AD21;}
```

-- position: absolute; --

An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element had no positioned ancestors it uses the document body, and moves along with page scrolling.

NOTE: A "positioned" element is one whose position is anything except `static`

A simple example:

```
div.relative { position: relative;  
  width: 400px;  
  height: 200px;  
  border: 3px solid #73AD21;}  
  
div.absolute { position: absolute;  
  top: 80px;  
  right: 0;  
  width: 200px;  
  height: 100px;  
  border: 3px solid #73AD21;}
```

-- position: sticky; --

An element with `position: sticky;` is positioned based on the user's scroll position.

A sticky element toggles between `relative` and `fixed`, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).

In this example, the sticky element sticks to the top of the page (`top: 0`), when you reach its scroll position.

-- Overlapping Elements --

When elements are positioned, they can overlap other elements.

The `z-index` property specifies the stack order of an element (which element should be place in front of, or behind, the others).

An element can have a positive or negative stack order:

```
img { position: absolute;  
  left: 0px;  
  top: 0px;  
  z-index: -1;}
```

-- All CSS Positioning Properties --

• `bottom` -- Sets the bottom margin edge for a positioned box
• `clip` -- Clips an absolutely positioned element
• `left` -- Sets the left margin edge for a positioned box
• `position` -- Specifies the type of positioning for an element
• `right` -- Sets the right margin edge for a positioned box
• `top` -- Sets the top margin edge for a positioned box
• `z-index` -- Sets the stack order of an element
