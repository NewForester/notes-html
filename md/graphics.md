<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5

HTML5 graphics has been supported by browsers for quite some time.
It takes two forms:

  * `<canvas>` and
  * `<svg>`

## The HTML5 Canvas Element

The `<canvas>` element is a rectangular place-holder that reserves space in which graphics may be drawn on-the-fly using JavaScript.

It should have an `id=` attribute for use by JavaScript and `height=` and `width=` attributes to declare its dimensions.
The `style=` attribute may be used to give it a border.

A `<canvas>` element provides a context handle for use by JavaScript.

```JavaScript
    var c = document.getElementById("myCanvas");
    var ctx = c.getContext("2d");
```

The context provides methods for drawing on the canvas.

There is a separate W3C [HTML Canvas](https://www.w3schools.com/graphics/canvas_intro.asp) tutorial.

### Examples of Canvas Drawing Methods

```JavaScript

    // line
    ctx.moveTo(0,0);
    ctx.lineTo(200,100);
    ctx.stroke();

    // circle
    ctx.beginPath();
    ctx.arc(95,50,40,0,2*Math.PI);
    ctx.stroke();

    // text
    ctx.font = "30px Arial";
    ctx.fillText("Hello World",10,50);

    // stroke text
    ctx.font = "30px Arial";
    ctx.strokeText("Hello World",10,50);

    // linear gradient
    var grd = ctx.createLinearGradient(0,0,200,0);
    grd.addColorStop(0,"red");
    grd.addColorStop(1,"white");

    ctx.fillStyle = grd;
    ctx.fillRect(10,10,150,80);

    // circular gradient
    var grd = ctx.createRadialGradient(75,50,5,90,60,100);
    grd.addColorStop(0,"red");
    grd.addColorStop(1,"white");

    ctx.fillStyle = grd;
    ctx.fillRect(10,10,150,80);

    // image
    var img = document.getElementById("scream");
    ctx.drawImage(img,10,10);
```


## The HTML5 SVG Element

SVG stands for Scalable Vector Graphics and can be used to define graphics for the Internet.
It is a W3C recommendation.

The `<svg>` element is a container for SVG graphics.
It should have `height=` and `width=` attributes to declare its dimensions.
The `style=` attribute may be used to give it a border.

The container holds XML elements for drawing paths, boxes, circles, text and graphic images.
It does not require JavaScript.

There is a separate W3C [SVG](https://www.w3schools.com/graphics/svg_intro.asp) tutorial.

### Examples of SVG Drawing Methods:

```html
  <!-- a circle -->
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />

  <!-- a rectangle -->
  <rect width="400" height="100" style="fill:rgb(0,0,255);stroke-width:10;stroke:rgb(0,0,0)" />

  <!-- a rounded rectangle -->
  <rect x="50" y="20" rx="20" ry="20" width="150" height="150"
      style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />

  <!-- a star -->
  <polygon points="100,10 40,198 190,78 10,78 160,198"
      style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />

  <!-- a logo -->
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />
    </linearGradient>
  </defs>
  <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
  <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
```

## Canvas and SVG Comparison

Canvas:

  1. requires JavaScript;
  1. draws 2D graphics on-the-fly;
  1. pixel based so the whole canvas is (re-)rendered as a unit;
  1. resolution dependent;
  1. well suited for graphic intensive games;
  1. no support for event handlers;
  1. poor text rendering;
  1. rendered graphic can be saved as a `.png` or `.jpg`

SVG:

  1. XML based notation for describing 2D graphics;
  1. has a DOM (so JavaScript event handlers may be attached);
  1. each shape is an object the browser can (re-)render independently;
  1. resolution independent;
  1. not suitable for game applications;
  1. support for event handlers;
  1. rendering is slow if the graphics are complex and uses the DOM a great deal;
  1. better suited for large rendering areas (Google Maps for example)


## Google Maps

Google Maps allows even a simple web page to display a map.

This uses an HTML API provided by Google.
You need an API key from Google but this is free.

There is a separate W3C [Google Maps](https://www.w3schools.com/graphics/google_maps_intro.asp) tutorial.

### Example of Rendering a Google Map:

It can be as simple as:

```html
    <!DOCTYPE html>
    <html>
    <body>

    <h1>My First Google Map</h1>

    <div id="map" style="width:400px;height:400px;background:yellow"></div>

    <script>
    function myMap() {
        var mapOptions = {
            center: new google.maps.LatLng(51.5, -0.12),
            zoom: 10,
            mapTypeId: google.maps.MapTypeId.HYBRID
        }
        var map = new google.maps.Map(document.getElementById("map"), mapOptions);
    }
    </script>

    <script
      src="https://maps.googleapis.com/maps/api/js?key=AIzaSyBu-916DdpKAjTmJNIgngS6HL_kDIKU0aU&callback=myMap">
    </script>
</body>
</html>

```

Explanation:

  1. the `<div id="map"` defines the map container and its size;
  1. the `var map = new` creates the map in the container;
  1. the `center` attribute gives the latitude and longitude;
  1. the `zoom` attribute gives the resolution;
  1. the `mapTypeId` gives the map's type (HYBRID);
  1. alternatives are ROADMAP, SATELLITE, HYBRID and TERRAIN;
  1. presumably `map` is a handle through which the on-screen map can be manipulated;
  1. the external script references the Google API;
  1. the JavaScript function `myMap()` is passed as a callback function

</body>
</html>
