<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Colours</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Colours

HTML colours may be specified any one of three ways.

<hr /><!-- Colours by Name -->

HTML supports 140 standard colour names.
See [http://www.w3schools.com/colors/colors_names.asp](http://www.w3schools.com/colors/colors_names.asp).

```html
    <h4 style="background-color:red">
    A red background
    </h4>

    <h4 style="background-color:orange">
    An orange background
    </h4>

    <h4 style="background-color:yellow">
    A yellow background
    </h4>

    <h4 style="background-color:blue;color:white">
    A blue background
    </h4>

    <h4 style="background-color:cyan">
    A cyan background
    </h4>
```

<p>will appear as:</p>
<div class=indent>
    <h4 style="background-color:red">
    A red background
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:orange">
    An orange background
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:yellow">
    A yellow background
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:blue;color:white">
    A blue background
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:cyan">
    A cyan background
    </h4>
</div>


<hr /><!-- Colours by RGB Value -->

Colour may be given as an <abbr title="Red Green Blue">RGB</abbr> value.

```html
    <h4 style="background-color:rgb(255,0,0)">
    Background set to red with rgb(255,0,0)
    </h4>

    <h4 style="background-color:rgb(0,255,0)">
    Background set to green with rgb(0,255,0)
    </h4>

    <h4 style="background-color:rgb(0,0,255);color:white">
    Background set to blue with rgb(0,0,255)
    </h4>

    <h4 style="background-color:rgb(255,255,0)">
    Background set to yellow with rgb(255,255,0)
    </h4>

    <h4 style="background-color:rgb(255,0,255)">
    Background set to magenta with rgb(255,0,255)
    </h4>

    <h4 style="background-color:rgb(0,255,255)">
    Background set to cyan with rgb(0,255,255)
    </h4>
```

<p>will appear as:</p>
<div class=indent>
    <h4 style="background-color:rgb(255,0,0)">
    Background set to red with rgb(255,0,0)
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:rgb(0,255,0)">
    Background set to green with rgb(0,255,0)
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:rgb(0,0,255);color:white">
    Background set to blue with rgb(0,0,255)
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:rgb(255,255,0)">
    Background set to yellow with rgb(255,255,0)
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:rgb(255,0,255)">
    Background set to magenta with rgb(255,0,255)
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:rgb(0,255,255)">
    Background set to cyan with rgb(0,255,255)
    </h4>
</div>


<hr /><!-- Colours by Hex Value -->

Colour may be given as a 6-digit hex value.

```html
    <h4 style="background-color:#FF0000">
    Background set to red using #FF0000
    </h4>

    <h4 style="background-color:#00FF00">
    Background set to green using #00FF00
    </h4>

    <h4 style="background-color:#0000FF;color:white">
    Background set to blue using #0000FF
    </h4>

    <h4 style="background-color:#FFFF00">
    Background set to yellow using #FFFF00
    </h4>

    <h4 style="background-color:#FF00FF">
    Background set to magenta using #FF00FF
    </h4>

    <h4 style="background-color:#00FFFF">
    Background set to cyan using #00FFFF
    </h4>
```

<p>will appear as:</p>
<div class=indent>
    <h4 style="background-color:#FF0000">
    Background set to red using #FF0000
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#00FF00">
    Background set to green using #00FF00
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#0000FF;color:white">
    Background set to blue using #0000FF
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#FFFF00">
    Background set to yellow using #FFFF00
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#FF00FF">
    Background set to magenta using #FF00FF
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#00FFFF">
    Background set to cyan using #00FFFF
    </h4>
</div>


<hr /><!-- Grey Scale -->

Shades of grey are often defined using equal values for the three primary colours:

```html
    <h4 style="background-color:#000000;color:white">
    Background set by using #000000
    </h4>

    <h4 style="background-color:#404040;color:white">
    Background set by using #404040
    </h4>

    <h4 style="background-color:#808080;color:white">
    Background set by using #808080
    </h4>

    <h4 style="background-color:#CCCCCC;">
    Background set by using #CCCCCC
    </h4>

    <h4 style="background-color:#FFFFFF;">
    Background set by using #FFFFFF
    </h4>
```

<p>will appear as:</p>
<div class=indent>
    <h4 style="background-color:#000000;color:white">
    Background set by using #000000
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#404040;color:white">
    Background set by using #404040
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#808080;color:white">
    Background set by using #808080
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#CCCCCC;">
    Background set by using #CCCCCC
    </h4>
</div>
<div class=indent>
    <h4 style="background-color:#FFFFFF;">
    Background set by using #FFFFFF
    </h4>
</div>

<hr />

</body>
</html>
