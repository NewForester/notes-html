<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Styles</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Styles

The `style=` attribute of an HTML element can be used to set a number of element properties.
The general form is:

```html
    <tag-name style="property:value">
    <tag-name style="property1:value1;property2:value2;...">
```

Note both `property` and `value` are defined by CSS and that
usually such properties are not defined for individual elements but are defined in the metadata for the page.


<hr><!-- Background Colour Property -->

The `background-color:` property is eponymous:

```html
    <p style="background-color:aquamarine;">Text on an aquamarine background.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p style="background-color:aquamarine;">Text on an aquamarine background.</p>
</div>


<hr /><!-- Text Colour Property -->

The `color:` property sets the text colour for element contents:

```html
    <p style="color:blue;">This is a blue sentence.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p style="color:blue;">This is a blue sentence.</p>
</div>


<hr /><!-- Font Property -->

The `font-family:` property declares the text font to be used for element contents:

```html
    <p style="font-family:courier;">This is a courier paragraph.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p style="font-family:courier;">This is a courier paragraph.</p>
</div>


<hr /><!-- Text Size Property -->

The `font-size:` property declares the text size of element contents:

```html
    <p style="font-size:150%">An enlarged paragraph.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p style="font-size:150%">An enlarged paragraph.</p>
</div>


<hr /><!-- Text Alignment -->

The `text-align:` property declares the desired horizontal alignment for element contents:

```html
    <p style="text-align:center;">Piggy in the middle</p>
```

<p>will appear as:</p>
<div class=indent>
    <p style="text-align:center;">Piggy in the middle</p>
</div>

<hr />

</body>
</html>
