## This is some things about Charts :


* First  download ```Chart.js```. Copy the ```Chart.min.js``` out of the unzipped folder and into the directory youâ€™ll be working in. Then create a new html page and import the script:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```

### Line Chart

* To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

```
<canvas id="buyers" width="600" height="400"></canvas>
```

Next

```
<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```

* Inside the same script tags we need to create our data, in this instance itâ€™s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins â€˜var buyers=â€™:

```
var buyerData = {
 labels : ["January","February","March","April","May","June"],
 datasets : [
  {
   fillColor : "rgba(172,194,132,0.4)",
   strokeColor : "#ACC26D",
   pointColor : "#fff",
   pointStrokeColor : "#9DB86D",
   data : [203,156,99,251,305,247]
  }
 ]
}
```

### Pie Chart

* First

```
<canvas id="countries" width="600" height="400"></canvas>
```

Next

```
var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);
```

* Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section:

```
var pieData = [
 {
  value: 20,
  color:"#878BB6"
 },
 {
  value : 40,
  color : "#4ACAB4"
 },
 {
  value : 10,
  color : "#FF8153"
 },
 {
  value : 30,
  color : "#FFEA88"
 }
];
```

Next

```
var pieOptions = {
 segmentShowStroke : false,
 animateScale : true
}
```

### Bar Chart

* First

```
<canvas id="income" width="600" height="400"></canvas>
```

Next

```
var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);
```

* add in the bar chartâ€™s data:

```
var barData = {
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
}
```

### The ```<canvas>``` element

* the ```<canvas>``` element has only two attributes, ```width``` and ```height```. These are both optional and can also be set using ```DOM properties```.

* ```<canvas>``` only supports two primitive shapes: rectangles and paths (lists of points connected by lines).

* Rectangle

  * ```fillRect(x, y, width, height)```
        Draws a filled rectangle.

  * ```strokeRect(x, y, width, height)```
        Draws a rectangular outline.

  * ```clearRect(x, y, width, height)```
        Clears the specified rectangular area, making it fully transparent.

* Paths

  * ```beginPath()```
    Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.

  * ```Path methods```
    Methods to set different paths for objects.

  * ```closePath()```
    Adds a straight line to the path, going to the start of the current sub-path.

  * ```stroke()```
    Draws the shape by stroking its outline.

  * ```fill()```
    Draws a solid shape by filling the path's content area.

* ```moveTo(x, y)``` moves the pen to the coordinates specified by x and y.

* For drawing straight lines, use the ```lineTo()``` method.

* To draw arcs or circles, we use the ```arc()``` or ```arcTo()``` methods.

  * ```arc(x, y, radius, startAngle, endAngle, counterclockwise)```
    Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by counterclockwise (defaulting to clockwise).

  * ```arcTo(x1, y1, x2, y2, radius)```
    Draws an arc with the given control points and radius, connected to the previous point by a straight line.

* Bezier and quadratic curves

  * ```quadraticCurveTo(cp1x, cp1y, x, y)```
    Draws a quadratic BÃ©zier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
  * ```bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)```
    Draws a cubic BÃ©zier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

* Path2D objects

  * The ```Path2D()``` constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.

### Applying Styles and colors

* Color
  * ```fillStyle = color```
    Sets the style used when filling shapes.

  * ```strokeStyle = color```
    Sets the style for shapes' outlines.

* Line

  * ```lineWidth = value```
    Sets the width of lines drawn in the future.

  * ```lineCap = type```
    Sets the appearance of the ends of lines.

  * ```lineJoin = type```
    Sets the appearance of the "corners" where lines meet.

  * ```miterLimit = value```
    Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

  * ```getLineDash()```
    Returns the current line dash pattern array containing an even number of non-negative numbers.

  * ```setLineDash(segments)```
    Sets the current line dash pattern.

  * ```lineDashOffset = value```
    Specifies where to start a dash array on a line.

* The ```lineCap```property determines how the end points of every line are drawn. There are three possible values for this property and those are: ```butt```, ```round``` and ```square```. By default this property is set to ```butt```.

* The ```lineJoin``` property determines how two connecting segments (of lines, arcs or curves) with non-zero lengths in a shape are joined together (degenerate segments with zero lengths, whose specified endpoints and control points are exactly at the same position, are skipped).

* The ```setLineDash``` method and the ```lineDashOffset``` property specify the dash pattern for lines. The ```setLineDash``` method accepts a list of numbers that specifies distances to alternately draw a line and a gap and the ```lineDashOffset``` property sets an offset where to start the pattern.

* Patterns

  * ```createPattern(image, type)```
    Creates and returns a new canvas pattern object. ```image``` is a ```CanvasImageSource``` (that is, an ```HTMLImageElement```, another canvas, a ```<video>``` element, or the like. ```type``` is a string indicating how to use the image.

* Shadows

  * ```shadowOffsetX = float```
    Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

  * ```shadowOffsetY = float```
    Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

  * ```shadowBlur = float```
    Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.

  * ```shadowColor = color```
    A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

### Drawing text

* ```fillText(text, x, y [, maxWidth])```
    Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
* ```strokeText(text, x, y [, maxWidth])```
    Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

* Styling Text

  * ```font = value```
    The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.

  * ```textAlign = value```
    Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

  * ```textBaseline = value```
    Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.

  * ```direction = value```
    Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.


[Back to Home](README.md)
