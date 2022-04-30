//** HTML Responsive **//

Responsive web design is about creating web pages that look good on all devices!

A responsive web design will automatically adjust for different screen sizes and viewports.

Responsive Web Design is about using HTML and CSS to automatically resize, hide, shrink, or enlarge, a website, to make it look good on all devices (desktops, tablets, and phones):

-- Setting The Viewport --

To create a responsive website, add the following `<meta>` tag to all your web pages:

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`

-- Responosive Images --

Responsive images are images that scale nicely to fit any browser size.

-- Using the Width Property --

If the CSS `width` property is set to 100%, the image will be repsonsive and scale up and down.

`<img src="img_girl.jpg" **style="width:100%;">`

Notice that in the example above, the image can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the `max-width` property instead.

-- Using the max-width Property --

If the `max-width` property is set to 100%, the image will scale don if it has to, but never scale up to be larger than its original size.

Example:

`<img src="img_girl.jpg" style="**max-width:100%;**height:auto;">`

-- Show Different Images Depending on Browser Width --

The HTML `<picture>` element allows you to define different images for different browser window sizes.

Example:

```
<picture>  
 <source srcset="img_smallflower.jpg" media="(max-width: 600px)">  
 <source srcset="img_flowers.jpg" media="(max-width: 1500px)">  
 <source srcset="flowers.jpg">  
 <img src="img_smallflower.jpg" alt="Flowers">  
</picture>
```

-- Responsive Text Size --

The text size can be set with a "vw" unit, which means the "viewport width".

That way the text size will follow the size of the browser window.

Example:

`<h1 style="font-size:10vw**">Hello World</h1>`

VIewport is the browser window size. 1w = 1% of viewport width. If the viewport is 50cm wide, 1vw is 0.5cm.

-- Media Queries --

In addition to resize text and images, it is also common to use media queries in responsive web pages.

With media queries you can define completely different styles for different browser sizes.

Example: resize the browser window to see that the three div elements below will display horizontally on large screens and stacked vertically on small screens

```
<style>  
.left, .right { float: left;  
  width: 20%; /* The width is 20%, by default */}  
  
.main { float: left;  
  width: 60%; /* The width is 60%, by default */}  
  
/* Use a media query to add a breakpoint at 800px: */  
@media screen and (max-width: 800px) { .left, .main, .right { width: 100%; /* The width is 100%, when the viewport is 800px or smaller */ }}  
</style>
```