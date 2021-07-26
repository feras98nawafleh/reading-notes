# Chart.js and Canvas

## Chart.js

How to Use Chart.js?
Chart.js is easy to use.

First, add a link to the providing CDN (Content Delivery Network):

```js
<script
src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.js">
</script>
```
Then, add a ```<canvas>``` to where you want to draw the chart:

```js
<canvas id="myChart" style="width:100%;max-width:700px"></canvas>
```
The canvas element must have a unique id.

That's all!

Typical Scatter Chart Syntax:
```js
var myChart = new Chart("myChart", {
  type: "scatter",
  data: {},
  options: {}
});
```
## HTML Canvas
HTML Canvas Graphics
The HTML <canvas> element is used to draw graphics on a web page.

The graphic to the left is created with <canvas>. It shows four elements: a red rectangle, a gradient rectangle, a multicolor rectangle, and a multicolor text.

What is HTML Canvas?
The HTML <canvas> element is used to draw graphics, on the fly, via JavaScript.

The <canvas> element is only a container for graphics. You must use JavaScript to actually draw the graphics.

Canvas has several methods for drawing paths, boxes, circles, text, and adding images.
  
Canvas Examples
A canvas is a rectangular area on an HTML page. By default, a canvas has no border and no content.

The markup looks like this:

```html 
 <canvas id="myCanvas" width="200" height="100"></canvas>
 ```
Note: Always specify an id attribute (to be referred to in a script), and a width and height attribute to define the size of the canvas. To add a border, use the style attribute.

Example
  ```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>
  ```
