<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Paragraphs</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Paragraphs

<hr><!-- Paragraph Elements -->

The `<p>` element encloses a paragraph.

```html
    <p>A paragraph
    may consist of
    many lines.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>A paragraph
    may consist of
    many lines.</p>
</div>

A browser will reformat text within a paragraph removing extra lines and spaces.

Most browsers will display paragraphs correctly if you forget the closing tag.
Do not reply on this.


<hr><!-- Line Breaks -->

The `<br>` element inserts a line break.
Use it when you want a new line without starting a new paragraph.

```html
    <p>A paragraph <br /> with a line break.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>A paragraph <br /> with a line break.</p>
</div>


<hr><!-- Pre-formatted Text -->

The `<pre>` element encloses pre-formatted text.

```html
    <pre>
    Pre-formatted  text  with  extra
    lines  and  spaces.
    </pre>
```

<div><p>will appear as:</p>
<div class=noindent>
    <pre>
    Pre-formatted  text  with  extra
    lines  and  spaces.
    </pre>
</div>

A browser will display the text as is, with extra lines and spaces.
It may also use a different (fixed width) font.

<hr />

</body>
</html>
