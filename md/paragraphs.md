<!DOCTYPE html>
<html>

<head>
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
