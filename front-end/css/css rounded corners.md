//** CSS Rounded Corners **//

With the CSS `border-radius` property, you can give any element "rounded corners".

-- CSS border-radius Property --

The CSS `border-radius` property defines the radius of an element's corners.

Tip: This property allows you to add rounded corners to elements!

Tip: The `border-radius` property is actually a shorthand property for the `border-top-left-radius`, `border-top-right-radius`, `border-bottom-right-radius` and `border-bottom-left-radius` properties.

-- CSS border-radius - Specify Each Corner --

The `border-radius` property can have one to four values. Here are the rules:

Four values - border-radius: 15px 50px 30px 5px; (first value applies to top-left corner, second value applies to top-right corner, third value applies to bottom-right corner, and fourth value applies to bottom-left corner)

Three values - border-radius: 15px 50px 30p; (first value applies to top-left corner, second value applies to top-right and bottom-left corners, and third value applies to bottom-right corner)

Two values - border-radius: 15px 50px; (first value applies to top-left and bottom-right corners, and the second value applies to top-right and bottom-left corners)

One value - border-radius: 15px; (the value applies to all four corners, which are rounded equally)

You can also create elliptical corners:

```
#rcorners1 {  border-radius: 50px / 15px;  
  background: #73AD21;  
  padding: 20px;  
  width: 200px;  
  height: 150px;}  
  
#rcorners2 {  border-radius: 15px / 50px;  
  background: #73AD21;  
  padding: 20px;  
  width: 200px;  
  height: 150px;}  
  
#rcorners3 {  border-radius: 50%;  
  background: #73AD21;  
  padding: 20px;  
  width: 200px;  
  height: 150px;}

[Try it Yourself »Links to an external site.](https://www.w3schools.com/css/tryit.asp?filename=trycss3_border-radius3)
```