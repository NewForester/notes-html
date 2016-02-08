<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Comments

<hr /><!-- Comments -->

HTML comment tags enclose comments in HTML documents.

```html
    <p>This is a
    <!--
    A comment that will not be displayed
    -->
    sentence.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>This is a
    <!--
    A comment that will not be displayed
    -->
    sentence.</p>
</div>

Comments are not displayed:
they may be used to document the HTML source code.

Comments are useful for debugging:
they may be used to comment out parts of the document.

<hr /><!-- Conditional Comments -->

Conditional comments may be browser specific (and not part of the standard).

```html
    <!--[if IE 9]>
        .... some HTML here ....
    <![endif]-->
```

<hr />

</body>
</html>
