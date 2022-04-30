//** CSS Background **//

-- CSS Multiple Backgrounds --

Css allows you to add multiple background images for an element, through the `background-image` property.

The different background images are separeted by commas, and the images are stacked on top of each other, where the first image is closest to the viewer.

The following example has two background images, the first image is a flower (aligned to the bottom and right) and the second image is a paper background (aligned to the top-left corner):

```
#example1 {  background-image: url(img_flwr.gif), url(paper.gif);  
  background-position: right bottom, left top;  
  background-repeat: no-repeat, repeat;}
```

Multiple background images can be specified using either the individual background properties (as above) or the `background` shorthand property.

The following example uses the `background` shorthand property (same result as example above):

```
#example1 {  background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;}
```

-- CSS Background Size --

The CSS `background-size` property allows you to specify the size of background images.

The size can be specified in lengths, percentages, or by using one of the two keywords: contain or cover.

The following example resizes a background image to much smaller than the original image (using pixels).

Example:

```
#div1 {  background: url(img_flower.jpg);  
  background-size: 100px 80px;  
  background-repeat: no-repeat;}
```

The two other possible values for `background-size` are `contain` and `cover`. 

The `contain` keyword scales the background image to be as large as possible (but both its width and its height must fit inside the content area). As such, depending on the proportions of the background image and the background positioing area, there may be some areas of the background which are not covered by the background image.

The `cover` keyword scales the background image so that the content area is completely covered by the background image (both its width and height are equal to or exceed the content area). As such, some parts of the background image may not be visible in the background positioning area.

The following example issustrates the use of `contain` and `cover`:

```
#div1 {  background: url(img_flower.jpg);  
  background-size: contain;  
  background-repeat: no-repeat;}  
  
#div2 {  background: url(img_flower.jpg);  
  background-size: cover;  
  background-repeat: no-repeat;}
```

-- Define Sizes of Multiple Background Images --

The `background-size` property who accepts multiple values for background size (using a comma-separated list), when working with multiple backgrounds.

The following example has three background images specified, with different background-size value for each image:

```
#example1 {  background: url(img_tree.gif) left top no-repeat, url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;  
  background-size: 50px, 130px, auto;}
```

-- Full Size Background Image --

Now we want to have a background image on a website that covers the entire browser window at all times.

The requirements are as follows:

• Fill the entire page with the image (no white space)
• Scale image as needed
• Center image on page
• Do not cause scrollbars

The following example shows how to do it; Use the `<html>` element (the `<html>` element is always at least the height of the browser window). Then set a fixed and centered background on it. The adjust its size with the background-size property:

```
html {  background: url(img_man.jpg) no-repeat center fixed;  
  background-size: cover;}
```

-- Hero Image --

You could also use different background properties on a `<div>` to create a hero image (a large image with text), and place it where you want.

```
.hero-image {  background: url(img_man.jpg) no-repeat center;  
  background-size: cover;  
  height: 500px;  
  position: relative;}
```

-- CSS background-origin Property --

The CSS `background-origin` property specifies where the background image is positioned.

The propery takes three different values:

• border-box - the background image starts from the upper left corner of the border
• padding-box - (default) the background image starts from the upper left corner of the padding edge
• content-box - the background image starts from the upper left corner of the content

The following example illustrates the `background-origin` property:

```
#example1 {  border: 10px solid black;  
  padding: 35px;  
  background: url(img_flwr.gif);  
  background-repeat: no-repeat;  
  background-origin: content-box;}
```

-- CSS background-clip Property --

The CSS `background-clip` property specifies the painting area of the background.

The property takes three different values:

• border-box -- (default) the background is painted to the outside edge of the border
• padding-box -- the background is painted to the outside edge of the padding
• content-box -- the background is painted within the content box

Example:

```
#example1 {  border: 10px dotted black;  
  padding: 35px;  
  background: yellow;  
  background-clip: content-box;}
```

-- CSS Advanced Background Properties --

`background` -- A shorthand property for setting all the background properties in one declaration
`background-clip` -- Specifies the painting area of the background
`background-image` -- Specifies one or more background images for an element
`background-origin` -- Specifies where the background imae(s) is/are positioned
`background-size` -- Specifies the size of the background image(s)