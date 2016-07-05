<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Formatting</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Formatting

HTML provides a number of elements that allow text with special meaning to be tagged.
In terms of what is displayed, they do a similar job to the `style=` attribute.


<hr /><!-- Bold and Strong Text Elements -->

The `<b>` and `<strong>` elements both delimit text that browsers usually display as bold text.

```html
    <p>Some <b>bold text</b> in a paragraph.</p>

    <p>Some <strong>important text</strong> in a paragraph.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>Some <b>bold text</b> in a paragraph.</p>
    <p>Some <strong>important text</strong> in a paragraph.</p>
</div>

Bold has historically be used to emphasise important text.
Use `<strong>` for emphasis and `<b>` for plain bold.


<hr /><!-- Italic and Emphasised Text Elements-->

The `<i>` and `<em>` elements both delimit text that browsers usually display in italics.

```html
    <p>Some <i>text in italics</i> in a paragraph.</p>

    <p>Some <em>emphasised text</em> in a paragraph.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>Some <i>text in italics</i> in a paragraph.</p>
    <p>Some <em>emphasised text</em> in a paragraph.</p>
</div>

Italics have historically be used to emphasise text.
Use `<em>` for emphasis and `<i>` for plain italics.


<hr /><!-- The Smaller Text Element -->

The `<small>` element defines smaller text:

```html
    <p>The next word is <small>smaller</small> that the rest.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>The next word is <small>smaller</small> that the rest.</p>
</div>


<hr /><!-- Deleted and Inserted Text Elements -->

The `<del>` and `<ins>` elements delimit deleted and inserted text.

```html
    <p>I have <del>altered</del> changed my mind.</p>

    <p>I have added <ins>yet</ins> another word.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>I have <del>altered</del> changed my mind.</p>
    <p>I have added <ins>yet</ins> another word.</p>
</div>

Deleted text is usually rendered crossed-out (strike through) and inserted text is usually underlined.


<hr /><!-- Subscript and Superscript Elements -->

The `<sub>` and `<sup>` elements delimit subscript and superscript text.

```html
    <p>This is <sub>subscripted</sub> text.</p>

    <p>This is <sup>superscripted</sup> text.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>This is <sub>subscripted</sub> text.</p>
    <p>This is <sup>superscripted</sup> text.</p>
</div>

<hr />

</body>
</html>
