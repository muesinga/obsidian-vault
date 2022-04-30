//** Radial Gradients **//

A radial gradient is defined by its center.

To create a radial gradient you must also define at least two color stops.

-- Syntax --

`background-image: radial-gradient(_shape size_ at _position, start-color, ..., last-color_);`

By default, shape is elllipse, size is farthest-corner, and position is center.

Raidal Gradient - Evenly Spaced Color Stops (this is default)

The following example shows a radial gradient with evenly spaced color stops:

`#grad {  background-image: radial-gradient(red, yellow, green);}`

Radial Gradient - Differently Spaced Color Stops

The following example shows a radial gradient with differently spaced color stops:

`#grad {  background-image: radial-gradient(red 5%, yellow 15%, green 60%);}`

-- Set Shape --

The shape parameter defines the shape. It can take the value circle or ellipse. The defualt value is ellipse.

The following example shows a radial gradient with the shape of a circle:

`#grad {  background-image: radial-gradient(circle, red, yellow, green);}`

-- Use of Different Size Keywords --

The size parameter defines the size of the gradient. It can take four values:

• closest-side
• farthest-side
• closest-corner
• farthest-corner

Example:

A radial gradient with different size keywords:

```
#grad1 {  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);}  
  
#grad2 {  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);}
```

-- Repeating a radial-gradient --

The repeating-radial-gradient() function is used to repeat radial gradients:

Example

A repeating radial gradient:

`#grad {  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);}`

