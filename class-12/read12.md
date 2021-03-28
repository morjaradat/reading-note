# CHART.JS

- Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

## Setting up

### download Chart.js. from : <https://github.com/chartjs/Chart.js>

### Drawing a line chart by create a canvas element in our HTML

1. we need to write a script that will retrieve the context of the canvas,
2. Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’:

### Drawing a pie chart

1. Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element:

--<-canvas id="countries" width="600" height="400"><-/canvas-->

2. we need to get the context and to instantiate the chart:

var countries= document.getElementById("countries").getContext("2d");<br>
new Chart(countries).Pie(pieData, pieOptions);
3. we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section:

- `var pieData = [`
 `{`
 `value: 20,`
 `color:"#878BB6"`
 `},`
 `{`
 `value : 40,`
 `color : "#4ACAB4"`
 `},`
 {`
 ` value : 10,`
 ` color : "#FF8153"`
 `},`
 `{`
 ` value : 30,`
 ` color : "#FFEA88"`
 `}`
`];`

4.Now, immediately after the pieData we’ll add our options:

(var pieOptions = {
 segmentShowStroke : false,
 animateScale : true
}`)

### Drawing a bar chart

- Finally, let’s add  a bar chart to our page. Happily the syntax for the bar chart is very similar to the line chart we’ve already added. First, we add the canvas element:

(`<canvas id="income" width="600" height="400"></canvas>`)
Next, we retrieve the element and create the graph:

var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);
And finally, we add in the bar chart’s data:

(`var barData = {
 labels : ["January","February","March","April","May","June"],
 datasets : [
  {
   fillColor : "#48A497",
   strokeColor : "#48A4D1",
   data : [456,479,324,569,702,600]
  },
  {
   fillColor : "rgba(73,188,170,0.4)",
   strokeColor : "rgba(72,174,209,0.4)",
   data : [364,504,605,400,345,320]
  }

 ]
}`)

# Basic usage of canvas

## The `<canvas>` element

- `At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties.`

- `The id attribute isn't specific to the <canvas> element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance).`
-`The <canvas> element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas`

## Required `</canvas>` tag

- `As a consequence of the way fallback is provided, unlike the <img> element, the <canvas> element requires the closing tag (</canvas>).`
- `If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.`

- `If fallback content is not needed, a simple <canvas id="foo" ...></canvas> is fully compatible with all browsers that support canvas at all.`

## The rendering context

- `The <canvas> element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context.`

## Checking for support

- `The fallback content is displayed in browsers which do not support <canvas>. Scripts can also check for support programmatically by testing for the presence of the getContext() method. Our code snippet from above becomes something like this:`
`var canvas = document.getElementById('tutorial');`

`if (canvas.getContext) {`
 `var ctx = canvas.getContext('2d');`
  `// drawing code here`
`} else {`
 `// canvas-unsupported code here`
`}`

## A skeleton template

`<!DOCTYPE html>`
`<html>`
  `<head>`
  `<meta charset="utf-8"/>`
   `<title>Canvas tutorial</title>`
  `<script type="text/javascript">`
  `function draw() {`
  `var canvas = document.getElementById('tutorial');`
  `if (canvas.getContext) {`
  `var ctx = canvas.getContext('2d');`
  `}`
 `}`
 `</script>`
 `<style type="text/css">`
 `canvas { border: 1px solid black; }`
 `</style>`
 `</head>`
 `<body onload="draw();">`
 `<canvas id="tutorial" width="150" height="150"></canvas>`
 `</body>`
`</html>`

# Drawing shapes with canvas

## The grid

- Before we can start drawing, we need to talk about the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default..

![p]()

## Drawing rectangles

- There are three functions that draw rectangles on the canvas:

1. fillRect(x, y, width, height) <br>
Draws a filled rectangle.
2. strokeRect(x, y, width, height)<br>
Draws a rectangular outline.
3. clearRect(x, y, width, height)<br>
Clears the specified rectangular area, making it fully transparent.

## Drawing paths

- A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

1. First, you create the path.
2. Then you use drawing commands to draw into the path.
3. Once the path has been created, you can stroke or fill the path to render it.

- the functions used to perform these steps:

1. beginPath()
2. Path methods
3. closePath()
4. stroke()

## Lines

- For drawing straight lines, use the lineTo() method.
- lineTo(x, y) :
Draws a line from the current drawing position to the position specified by x and y.

## Arcs

- To draw arcs or circles, we use the arc() or arcTo() methods.

- arc(x, y, radius, startAngle, endAngle, counterclockwise) :
Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by counterclockwise (defaulting to clockwise).
- arcTo(x1, y1, x2, y2, radius) :
Draws an arc with the given control points and radius, connected to the previous point by a straight line.

## Bezier and quadratic curves

- These are generally used to draw complex organic shapes.

- quadraticCurveTo(cp1x, cp1y, x, y) :
Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
- bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y) :
Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

## Rectangles

- In addition to the three methods we saw in Drawing rectangles, which draw rectangular shapes directly to the canvas, there's also the rect() method, which adds a rectangular path to a currently open path.

- rect(x, y, width, height) :
Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.

## Path2D objects

- To simplify the code and to improve performance, the Path2D object, available in recent versions of browsers, lets you cache or record these drawing commands. You are able to play back your paths quickly.

- Path2D() :
The Path2D() constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.

# Applying styles and colors

## Colors

- Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

- fillStyle = color :
Sets the style used when filling shapes.
- strokeStyle = color :
Sets the style for shapes' outlines.

## Transparency

- In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke and/or fill style.

- globalAlpha = transparencyValue /
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

## Line styles

- There are several properties which allow us to style lines.

1. lineWidth = value
Sets the width of lines drawn in the future.
2. lineCap = type
Sets the appearance of the ends of lines.
3. lineJoin = type
Sets the appearance of the "corners" where lines meet.
4. miterLimit = value
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
5. getLineDash()
Returns the current line dash pattern array containing an even number of non-negative numbers.
6. setLineDash(segments)
Sets the current line dash pattern.
7. lineDashOffset = value
Specifies where to start a dash array on a line.

## Gradients

- Just like any normal drawing program, we can fill and stroke shapes using linear, radial and conic gradients. We create a CanvasGradient object by using one of the following methods. We can then assign this object to the fillStyle or strokeStyle properties.

1. createLinearGradient(x1, y1, x2, y2)
Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).
2. createRadialGradient(x1, y1, r1, x2, y2, r2)
Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.
3. createConicGradient(angle, x, y)
Creates a conic gradient object with a starting angle of angle in radians, at the position (x, y).

## Patterns

- In one of the examples on the previous page, we used a series of loops to create a pattern of images. There is, however, a much simpler method: the createPattern() method.

- `createPattern(image, type)`
`Creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a <video> element, or the like. type is a string indicating how to use the image.`

## Shadows

- Using shadows involves just four properties:

1. shadowOffsetX = float
Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
2. shadowOffsetY = float
Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
3. shadowBlur = float
Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.
4. shadowColor = color
A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

# Drawing text

## Drawing text

- The canvas rendering context provides two methods to render text:

1. fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
2. strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

## Styling text

- There are some more properties which let you adjust the way the text gets displayed on the canvas:

1. font = value
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
2. textAlign = value
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
3. textBaseline = value
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
4. direction = value
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

## Advanced text measurements

- In the case you need to obtain more details about the text, the following method allows you to measure it.

- measureText() :
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.
