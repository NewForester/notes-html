<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Iframes</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Iframes

An `<iframe>` element is used to display a web page within a web page.
It in-lines a web page within a frame.

```html
    <iframe src="URL"></iframe>
```

the `src=` attribute specifies the Internet address of the page to in-line,
which may be a full URL or a [relative file path](file-paths.html).


The `height=` and `width=` attributes may used to specify the dimensions of the `<iframe>` element.
These are in pixels by default but can also be specified in percent.

An `<iframe>` element has a border by default.
This can be removed or given a different style using the CSS `border:` property with the `style=` attribute.
For example:

```html
    <iframe src="https://en.wikipedia.org/wiki/" height="200" width="600" style="border:2px solid blue;"></iframe>
```

<p>will appear as:</p>
<div class=indent>
    <iframe src="https://en.wikipedia.org/wiki/" height="200" width="600" style="border:2px solid blue;"></iframe>
</div>


<hr /><!-- An <iframe> as a link target -->

An `<iframe>` element can be the target of a link.
Clicking on the link will display the target page in the `<iframe>` element.

There is an implicit connection between the `target=` attribute of the link and
the `name=` attribute of the frame.

```html
    <iframe src="https://en.wikipedia.org/wiki/" height="200" width="600" name="gnu_frame"></iframe>

    <p><a href="https://www.gnu.org/" target="gnu_frame">GNU Project Home Page</a></p>
```

<p>will appear as:</p>
<div class=indent>
    <iframe src="https://en.wikipedia.org/wiki/" height="200" width="600" name="gnu_frame"></iframe>
</div>
<div class=indent>
    <p><a href="https://www.gnu.org/" height="200" width="600" target="gnu_frame">GNU Project Home Page</a></p>
</div>

<hr />

</body>
</html>
