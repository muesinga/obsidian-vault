The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag has two required attributes:

• src - Specifies the path to the image
• alt - Specifies an alternate text for the image

-- The src Attribute --

The required `src` attribute specifies the path (URL) to the image.

Note: When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon and the `alt` text are shown if the browser cannot find the image.

-- The alt Attribute --

The required `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).

The value of the `alt` attribute should describe the image:

Example:

`<img src="img_chania.jpg" alt="Flowers in Chania">`

-- Image Size - Width and Height --

You can use the `style` attribute to specify the width and height of an image.

Example:

`<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">`

Alternatively, you can use the `width` and `height` attributes:

Example:

`<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">`

-- Width and Height, or Style? --

The `width`, `height`, and `style` attributes are all valid in HTML.

However, we suggest using the `style` attribute. It prevents styles sheets from changing the size of images.

-- Images in Another Folder --

If you have your images in a sub-folder, you must include the folder name in the `src` attribute:

-- Images on Another Server/Website --

Some web sites points to an extenal image on another server.

To point to an image on another server, you must specify an absolute (full) URL in the `src` attribute:

`<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">`

-- Animated Images --

HTML allows animated GIFs

-- Image as a Link --

To use an image as a link, put the `<img>` tag inside the `<a>` tag.

-- Image Floating --

Use the CSS `float` preperty to let the image to the right or to the left of a text.

//** Image Map **//

The HTML `<mp>` tag defines an image map. An image map is an image with clickable areas. The areas are defined with one or more `<area>` tags.

The idea behind an image map is that you should be able to perform different actions depending on where in the image you click.

To create an image map you need an image, and some HTML code that describes the clickable areas.

-- The Image --

The image is inserted using the `<img>` tag. The only difference from other images is that you must add a `usemap` attribute:

`<img src="workplace.jpg" alt="Workplace" usemap="#workmap">`

The `usemap` value starts with a hash tag `#` followed by the name of the image map, and is used to create a relationship between the image and the image map.

-- Create Image Map --

Then, add `<map>` element.

The `<map>` element is used to create an image map, an is linked to the image by using the required `name` attribute.

`<map name="workmap">`

The `name` attribute must have the same value as the `<img>`'s `usemap` attribute.

-- The Areas --

Then, add the clickable areas.

A clickable area is defined using the `<area>` element.

-- Shape --

You must define the clickable area, and you can choose one of these values:

• `rect` - defines a rectangular region
• `circle` - defines a circular region
• `poly` - defines a polygonal region
• `default` - defines the entire region

You must also define some coordinates to be able to place the clickable are onto the image.

-- Shape="rect" --

The coordinates for `shape="rect"` come in pairs, one for the x-axis and one for the y-axis.

The coordinates `34. 44` is located 34 pixels from the left margin and 44 pixels from the top.

The coordinates `270, 350` is located 270 pixels from the left margin and 350 pixels from the top.

Now we have enough data to create a clickable rectangular area:

`<area shape="rect" coords="34, 44, 270, 350" href="computer.htm">``

-- Shape="circle" --

To add a circle area, first locate the coordinates of the center of the circle:

`337, 300`

The specify the radius of the circle:

`44` pixels

Now you have enough data to create a clickable circular area:

`<area shape="circle" coords="337, 300, 44" href="coffee.htm">`

-- Shape="poly" --

The `shape="poly"` contains several coordinate points, which creates a shape formed with straight lines (a polygon).

This can be used to create any shape.

-- Image Map and JavaScript --

A clickable area can also trigger a JavaScript function.

//** Background Images **//

To add a background image on a HTML element, use the HTML `style` attribute and the CSS `background-image` property.

Add a background image on a HTML element:

`<div style="background-image:url('img_girl.jpg');">`

You can specify the background image in the `<style>` element:

`<style>
div {
	background-image: url('img_girl.jpg');
}
</style>`

-- Background Repeat --

If the background image is smaller than the element, the image will repeat itself, horizontally and vertically, until it reaches the end of the element.

To avoid the background image from repeating itself, set the `background-repeat` property to `no-repeat`

-- Backgroud Cover --

If you want the background image to cover the entire element, you can set the `background-size` property to `cover.`

Also, to make sure the entire element is always covered, set the `background-attachment` property to `fixed:`

This way, the background image will cover the entire element, with no stretching (the image will keep its original proportions)

-- Background Stretch --

If you want the background image to stretch to fit the entire element, you can set the `background-size`property to `100% 100%`

//** The Picture Element **//

The HTML `<picture>` element allows you to display different pictures for different devices of screen sizes.

The HTML `<picture>` element gives web developers more flexibility in specifying image resources.

The `<picture>` element contains one or more `<source>` elements, each referring to different images through the `srcset` attribute. This way the browser can choose the image that best fits the current view and/or device.

Each `<source>` element has a `media` attribute that defines when the image is the most suitable

-- When to use the Picture Element --

There are two main purposes for the `<picture>` element:

1) Bandwidth

If you have a small screen or device, it is not necessary to load a large image file. The browser will use the first `<source>` element with matching attribute values, and ignore any of the following elements.

2) Format Support

Some browsers of devices may not support all image formats. By using the `<picture>` element, you can add images of all formats, and the browser will use the first format it recognizes, and ignore any of the following elemets.

-- HTML Image Tags --

`<img>` -- defines an image
`<map>` -- defines an image map
`<area>` -- defines a clickable area inside an image map
`<picture>` -- defines a container for multiple image resources