<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Container Elements

HTML elements are either block level or they are in-line.

Block level elements always begin on a new line and are full width.
Examples are headings and paragraphs.

In-line elements do not start a new line and take up no more width than necessary.
Examples are links and images.

<hr /><!-- Containers -->

The `<div>` element is a container for block elements and their contents.
It has no required attributes but any it does have are applied to its contents.
It is often used to apply style attributes from a CSS style sheet to blocks of content.

```html
    <div style=style="border: 1px solid limegreen;">
      <h2>The Importance of Being Earnest</h2>
      <p>In your own words but not more than 300.</p>
    </div>
```

<p>will appear as:</p>
<div class=indent>
    <div style="border: 1px solid limegreen;">
      <h2>The Importance of Being Earnest</h2>
      <p>In your own words but not more than 300.</p>
    </div>
</div>


<hr /><!-- Spans -->

The `<span>` element is a container for in-line elements and text.
It also has no required attributes but `style=` and `class=` are common.
It ensures a block of text has a consistent style without repetition.

```html
    <h2>The <span style="border: 1px solid limegreen;">Importance of</span> Being Earnest</h2>
```

<p>will appear as:</p>
<div class=indent>
    <h2>The <span style="border: 1px solid limegreen;">Importance of</span> Being Earnest</h2>
</div>

<hr />

</body>
</html>
