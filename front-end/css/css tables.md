//** CSS Tables **//

-- Table Borders --

To specify table borders in CSS, use the `border` property.

The example below specifies a black border for `<table>`, `<th>`,  and `<td>` elements.

Example:

`table, th, td { border: 1px solid black;}`

-- Full-Wdith Table --

The table above might seems small in some cases. f you need a table that should span the entire screen (full-width), add `width:100%` to the `<table>` element.

EXAMPLE:

`table { width: 100%;}`

DOUBLE BORDERS--

Notice that the table in the examples above have double borers. This is because both the table and the `<th>` and `<td>` elements have separate borders.

-- Collapse Table Borders --

The `border-colapse` property sets whether the table borders should be collapsed into a single border.

`table { border-collapse: collapse;}`

//** Table Size **//

The width and height of a table are defined by the `width` and `height` properties.

This example sets the width of the table to 100%, and the height of the `<th>` elements to 70px:

```
table { width: 100%;}  
  
th { height: 70px;}
```

//** Table Alignment **//

--Horizontal Alignment--

The `text-align` property sets the horizontal alignment (like left, right, or center) of the content in the `<th>` or `<td>`.

By default, the content of `<th>` elements are center-aligned and the content of `<td>` elements are left-aligned.

To center-align the content of `<td>` elements as well, use `text-align:center`

To left-align the content, force the alignment of `<th>` elements to be left-aligned, with the `text-align: left` property.

```
th { text-align: left;}
```

--Vertical Alignment--

The `vertical-align` property sets the vertical alignment (like top, bottom, or middle) of the content in `<th>` or `<td>`.

By default, the vertical alignment of the content in a table is middle (for both `<th>` and `<td>` elements).

//** Table Responsive **//

A responsive table will display a horizontal scroll bar if the screen is too small to display the full content.

Add a container element with `overflow-x:auto` around the `<table>` element to make it responsive:

```
<div style="overflow-x:auto;">  
  
<table>  
... table content ...  
</table>  
  
</div>
```

NOTE : ON Mac, scroll bars are hidden by default and only shown when being used

//** CSS Table Properties **//

• `border` - Sets all the border properties in one direction
• `border-collapse` - Specifies whether or not table borders should be collapsed
• `border-spacing` - Specifies the distance between the borders of adjacent cells
• `caption-side` - Specifies the placement of a table caption
• `empty-cells` - Specifies whether or not to display borders and background on empty cells in a table
• `table-layout` - Sets the layour algorithm to be used for a table

