<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Classes</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
    <style>
      span.note {
        font-size: 120%;
        color: red;
      }
    </style>
</head>

<body>

# HTML5

## CSS Classes

The `class=` attribute can be used to ensure elements have the same style without repetition.

For example:

```html
    div.cities {
      background-color: black;
      color: white;
      margin: 20px 0 20px 0;
      padding: 20px;
    }
```

defines a style class to be applied to all `<div>` elements with the `class="cities"` attribute.

In-line elements can also use the `class=` attribute:
For example:

```html
    span.note {
      font-size: 120%;
      color: red;
    }
```

might be used thus:

```html
    <h1>My <span class="note">Important</span> Heading</h1>
    <p>This is some <span class="note">important</span> text.</p>
```

<p>and would appear as:</p>
<div class=indent>
    <h1>My <span class="note">Important</span> Heading</h1>
    <p>This is some <span class="note">important</span> text.</p>
</div>

A style class may be restricted to a particular element type (as above) or
may be applied to any element by omitting the type from the definition:

```html
    .note {
      font-size: 120%;
      color: red;
    }
```

<hr />

</body>
</html>
