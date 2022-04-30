//** HTML Tables **//

HTML tables allow web developers to arrange data into rows and columns.

-- Define an HTML Table --

The `<table>` tag defines an HTML table.

Each table row is defined with a `<tr>` tag. Each table header is defined witha `<th>` tag. Each table data/cell is defined with a `<td>` tag.

By default, the text in `<th>` elements are bold and centered.

By default, the text in `<td>` elements are regular and left-aligned.

-- HTML Table - Collapsed Borders --

To let the borders collapse into one border, add the CSS `border-collapse` property.

Example:

`table, th, td { border: 1px solid black; border-collapse: collapse;}`

-- HTML Table - Add Cell Padding --

Cell padding specifies the space between the cell content and its borders.

If you do not specify a padding, the table cells will be displayed without padding.

To set the padding, use the CSS `padding` property.

example:

`th, td { padding: 15px;}`

-- HTML Table - Left-align Headings --

By default, table headings are bold and centered.

To left-align the table headings, use the CSS `text-align` property.

-- HTML Table - Add a Caption --

To add a caption to a table, use the `<caption>` tag.

-- A Special Style for One Table --

To define a special style for one particular table, add an `id` attribute to the table.