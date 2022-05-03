//** CSS 2D Transforms **//

CSS transforms allow you to move, rotate, scale, and skew elements.

With CSS `transform` property you can use the following 2D transformation methods:

`translate()`
`rotate()`
`scalex()`
`scaley()`
`scale()`
`skewX()`
`skewY()`
`skew()`
`matrix()`

-- The translate() Method --

The `translate()` method moves an element from its current position (according to the parametes given for the x-axis and the y-axis).

The following example moves the `<div>` elemetn 50 pixels to the right, and 100 pixels down from its current position.

Example:

```
div {
  transform: translate(50px, 100px);
}
```

-- The rotate() Method --

The `rotate()` method rotates an element clockwise or counter-clockwise according to a given degree.

The following example rotates the `<div>` element clockwise 20 degrees:

```
div {
  transform: rotate(20deg);
}
```

Using negative values will rotate the element counter-clockwise.

The following example rotates the `<div>` element counter-clockwise with 20 degrees.

```
div {
  transform: rotate(-20deg);
}
```

-- The scale() Method --

The `scale()` method increases or decreases the size of an element (according to the parameters given for the width and height).

The following example increases the `<div>` element to be two times of its original width, and three times of its original height:

```
div {
  transform: scale(2, 3);
}
```

The following example decreases the `<div>` element to be half of its original width and height:

```
div {
  transform: scale(0.5, 0.5);
}
```

-- The scaleX() Method --

The `scaleX()` method increases or decreases the width of an element.

The following example increases the `<div>` element to be two times of its original width:

```
div {
  transform: scaleX(2);
}
```
The following example decreases the `<div>` element to be half of its original width:

```
div {
  transform: scaleX(0.5);
}
```

-- The scaleY() Method --
The `scaleY()` method increases or decreases the height of an element.

The following example increases the `<div>` element to be three times of its original height:

```
div {
  transform: scaleY(3);
}
```

The following example decreases the `<div>` element to be half of its original height:

```
div {
  transform: scaleY(0.5);
}
```

-- The skewX() Method --

The `skewX()` method skews an element along the X-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the X-axis:

```
div {
  transform: skewX(20deg);
}
```

-- The skewY() Method --

The `skewY()` method skews an element along the Y-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the Y-axis:

```
div {
  transform: skewY(20deg);
}
```

-- The skew() Method --

The `skew()` method skews an element along the X and Y-axis by the given angles.

The following example skews the `<div>` element 20 degrees along the X-axis, and 10 degrees along the Y-axis.

Example:

```
div {
  transform: skew(20deg, 10deg);
}
```
If the second parameter is not specified, it has a zero value. So, the following example skews the `<div>` element 20 degrees along the X-axis:

```
div {
  transform: skew(20deg);
}
```

-- The matrix() Method --

The `matrix()` method combines all the 2D transform methods into one.

The matrix() method take six parameters, containing mathematic functions, which allows you to rotate, scale, move (translate), and skew elements.

The parameters are as follow: matrix(scaleX(),skewY(),scaleY(),translateX(),translateY())

Example:

```
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}

-- CSS 2D Transform Methods --

matrix(n,n,n,n,n,n) -- Defines a 2D transformation, using a matrix of six values
translate(x,y) -- Defines a 2D translation, moving the element along the X- and the Y-axis
translateX(n) -- Defines a 2D translation, moving the element along the X-axis
translateY(n) -- Defines a 2D translation, moving the element along the Y-axis
scale(x,y) -- Defines a 2D scale transformation, changing the elements width and height
scaleX(n) -- Defines a 2D scale transformation, changing the element's width
scaleY(n) -- Defines a 2D scale transformation, changing the element's height
rotate(angle) -- Defines a 2D rotation, the angle is specified in the parameter
skew(x-angle,y-angle) -- Defines a 2D skew transformation along the X- and the Y-axis
skewX(angle) -- Defines a 2D skew transformation along the X-axis
skewY(angle) -- Defines a 2D skew transformation along the Y-axis
```
