//** CSS Gradients **//

CSS gradients let you display smooth transitions between two or more specified colors.

CSS defines two types of gradients:

• Linear Gradients (goes down/up/left/right/diagonally)
• Radial Gradients (defined by their center)

-- CSS Linear Gradients --

To create a linear gradient you must define at lesat two color stops. Color stops are the colors you want to render smooth transitions among. YOu can also set a starting point and a direction (or an angle) along with the gradient effect.

Syntax:

```
background-image: linear-gradient(_direction_, _color-stop1_, _color-stop2, ..._);
```

Direction - Top to Bottom (this is default)

The following example shows a linear gradient that starts at the top. It starts red, transitioning to yellow:

```
#grad {  background-image: linear-gradient(red, yellow);}
```

Direction - Left to Right

The following example shows a linear gradient that starts from the left. It starts red, transitioning to yellow:

```
#grad {  background-image: linear-gradient(to right, red , yellow);}
```

Direction - Diagonal

You can make a gradient diagonally by specifying both the horizontal and vertical starting positions.

The following example shows a linear gradient that starts at top left (and goes to bottom right). It starts red, transitioning to yellow:

`#grad {  background-image: linear-gradient(to bottom right, red, yellow);}`

-- Using Angles --

If you want more control over the direction of the gradient, you can define an angle, instead of the predefined directions (to bottom, to top, to right, to left, to bottom right, etc.). A value of 0deg is equivalent to "to top". A value of 90deg is equivalent to "to right". A value of 180deg is equivalent to "to bottom".

`#grad {  background-image: linear-gradient(180deg, red, yellow);}`

-- Using Multiple Color Stops --

The following example shows a linear gradient (from top to bottom) with multiple color stops:

`#grad {  background-image: linear-gradient(red, yellow, green);}`

The following example shows how to create a linear gradient (from left to right) with the color of the rainbow and some text:

`#grad {  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);}`

-- Using Transparency --

CSS gradients also support transparency, which can be used to create fading effects.

To add transparency, we use the rgba() function to define the color stops. The last parameter in the rgba() function can be a value from 0 to 1, and it defines the transparency of the color: 0 indicates full transparency, 1 indicates full color (no transparency).

The following example shows a linear gradient that starts from the left. It starts fully transparent, transitioning to full color red:

`#grad {  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));}`

-- Repearting a linear-gradient --

The repeating-linear-gradient() function is used to repeat linear gradients:

`#grad {  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);}`