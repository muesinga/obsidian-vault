//** HTML SVG **//

SVG defines vector-based graphics in XML format.

-- What is SVG? --

• SVG stands for Scalable Vector Graphics
• SVG is used to define graphics for the Web
• SCG is a W3C recommendation

-- The HTML `<svg>` Element --

The HTML `<svg>` element is a container for SVG graphics.

SVG has several methods for drawing paths, boxes, circles, text, and graphic images.

Examples:

-- SVG Circle --

```
<!DOCTYPE html>  
<html>  
<body>  
  
<svg width="100" height="100">  
 <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />  
</svg>  
  
</body>  
</html>
```

-- SVG Rectangle --

```
<svg width="400" height="100">  
 <rect width="400" height="100" style="fill:rgb(0,0,255);stroke-width:10;stroke:rgb(0,0,0)" />  
</svg>
```

-- SVG Rounded Rectangle --

```
<svg width="400" height="180">  
 <rect x="50" y="20" rx="20" ry="20" width="150" height="150"  
  style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />  
</svg>
```

--SVG Star --

```
<svg width="300" height="200">  
 <polygon points="100,10 40,198 190,78 10,78 160,198"  
  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />  
</svg>
```

-- SVG Logo --

```
<svg height="130" width="500">  
 <defs>  
 <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">  
 <stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />  
 <stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />  
 </linearGradient>  
 </defs>  
 <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />  
 <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>  
 Sorry, your browser does not support inline SVG.  
</svg>
```

-- Differences Between SVG and Canvas --

SVG is a language for describing 2D graphics in XML.

Canvas draws 2D graphics, on the fly (with a JavaScript)

SVG is XML based, which means that every element is available within the SVG DOM. You can attach JavaScript event handlers for an element.

In SVG, each drawn shape is remembered as an object. If attributes of SCG object are changes, the browser can automatically re-render the shape.

Canvas is rendered pixel by pixel. In canvas, once the graphic is drawn, it is forgotten by the browser. If its position should be changed, the entire scene neede to be redrawn, including any objects that might have been covered by the graphic.

-- Comparison of Canvas and SVG --

Canvas:

• Resolution dependent
• No support for event handlers
• Poor text rendering capabilities
• You can save the resulting image as .png or .jpg
• Well suited for graphic-intensive games

SVG


• Resolution independent
• Support for event handlers
• Best suited for applications with large rendering areas (Google Maps)
• Slow rendering if complex (anything that uses the DOM a lot will be slow)
• Not suited for game applications