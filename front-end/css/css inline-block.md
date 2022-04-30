//** CSS Inline-block **//

Compared to `display: inline`, the major difference is that `display: inline-block` allows to set a width and height on the element.

Also, with `display: inline-block`, the top and bottom margins/paddings are respected, but with `display: inline` they are not.

Compared to `display: block`, the major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements.

The following example shows the different behavior of `display: inline`, `display: inline-block` and `display: block`

-- Using inline-block to Create Navigation Links --

One common use for `display: inline-block` is to display list items horizontally instead of vertically. The following example creates horizontal navigation links:

```
.nav { background-color: yellow;  
  list-style-type: none;  
  text-align: center;   
  padding: 0;  
  margin: 0;}  
  
.nav li { display: inline-block;  
  font-size: 20px;  
  padding: 20px;}
```