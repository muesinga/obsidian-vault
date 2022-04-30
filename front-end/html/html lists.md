//** HTML Lists **//

HTML lists allow web developers to group a set of related items in lists.

--  Unordered HTML List --

An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag.

-- Ordered HTML List --

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.

-- HTML Description Lists --

HTML also supports description lists.

A description list is a list of terms, with a description of each term.

The `<dl>` tag defines the description list, the `<dt>` taf defines the term (name), and the `<dd>` tag describes each term.

Example:

```
<dl>
	<dt>Coffee</dt>
	<dd>- black hot drink</dd>
	<dt>Milk</dt>
	<dd>- white cold drink</dd>
</dl>
```

-- HTML List Tags --

`<ul>` -- defines an unordered list
`<ol>` -- defines an ordered list
`<li>` -- defines a list item
`<dl>` -- defines a description list
`<dt>` -- defines a term in a description list
`<dd>` -- describes the term in a description list

//** Unordered Lists **//

The HTML `<ul>` tag defines an unordered (bulleted) list.

-- Unordered HTML List

An unordered lists starts with the `<ul>` tag. Each list item starts with the `<li>` tag.

Example:

```
<ul>
	<li>coffee</li>
	<li>tea</li>
	<li>milk</li>
</ul>
```

-- Unordered HTML List - Choose List Item Marker

The CSS `list-style-type` property is used to define the style of the list item marker. It can have one of the following values:

• disc -- sets the list item marker to a bullet (default)
• circle -- sets the list item marker to a circle
• square -- sets the list item marker to a square
• none -- the list items will not be marked

Example:

```
<ul style="list-style-type:disc;">
	<li>Coffee</li>
	<li>Tea</li>
	<li>Milk</li>
</ul>
```

//** Nested HTML Lists **//

```
<ul>  
 <li>Coffee</li>  
 <li>Tea  
	 <ul>  
		 <li>Black tea</li>  
		 <li>Green tea</li>  
	 </ul>  
 </li>  
 <li>Milk</li>  
</ul>
```

//** Horizontal List with CSS

HTML lists can be styled in many different ways with CSS.

One popular way is to style a list horizontally, to create a navigation menu

//** HTML List Tags **//

`<ul>` -- defines an unordered list
`<ol>` -- defines an ordered list
`<li>` -- defines a list item
`<dl>` -- defines a description list
`<dt>` -- defines a term in a description list
`<dd>` -- describes a term in a descritption list

//** Ordered LIsts **//

The HTML `<ol>` tag defines an ordered list. An ordered list can be numberical or alphabetical.

-- Ordered HTML List --

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.

The list items will be marked with numbers by default:

```
<ol>  
 <li>Coffee</li>  
 <li>Tea</li>  
 <li>Milk</li>  
</ol>
```

-- Ordered HTML List - The Type Attribute --

• type="1" -- The list items will be numbered with numbers (default)
• type="A" -- The list items will be numbered with uppercase letters
• type="a" -- The list items will be numbered with lowercase letters
• type="l" -- The list items will be numbered with uppercase roman numbers
• type="i" -- The list items willbe numbered with lowercase roman numbers

-- Control List Counting --

By default, an ordered list will start counting from 1. If you want to start counting from a specified number, you can use the `start` attribute.

```
<ol start="50">
	<li>Coffee</li>
	<li>Tea</li>
	<li>Milk</li>
</ol>
```

-- Nested HTML Lists --

Lists can be nested

```
<ol>
	<li>Coffee</li>
	<li>tea</li>
		<ol>
			<li>Black tea</li>
			<li>Green tea</li>
		</ol>
	</li>
	<li>Milk<li>
</ol>
```

-- HTML List Tags --

`<ul>` - Defines an unordered list
`<ol>` - Defindes an ordered list
`<li>` - Defines a list item
`<dl>` - Defines a description list
`<dt>` - Defines a term in a description list
`<dd>` - Describes the term in a description list

-- Other List --

HTML Description LIsts

A description list is a list of terms, with a description of each term.

The `<dl>` tag defines the description list, the `<dt>` tag defines the term (name), and the `<dd>` tag describes each term:

```
<dl>
	<dt>Coffee</dt>
	<dd>- black hot drink</dd>
	<dt>Milk</dt>
	<dd>- white cold drink</dd>
</dl>
```

-- HTML List Tags --

`<ul>` -- Defines an unordered list
`<ol>` -- Defines an ordered list
`<li>` -- Defines a list item
`<dl>` -- Defines a description list
`<dt>` -- Defines a term in a description list
`<dd>` -- Describes the term in a description list