<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Quotations</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Quotations

<hr /><!-- Quotation element -->

The `<q>` element delimits a short quotation.

```html
    <p>The crowd called <q>Long live the King !</q></p>
```

<p>will appear as:</p>
<div class=indent>
    <p>The crowd called <q>Long live the King !</q></p>
</div>

Browsers usually insert quotation marks around quotation element contents.


<hr /><!-- Block Quotation Elements -->

The `<blockquote>` element delimits a long quotation from another source.

```html
    <blockquote cite=https://en.wikipedia.org/wiki/APL_%28programming_language%29>
        APL (named after the book A Programming Language) is a programming language developed
        in the 1960s by Kenneth E. Iverson.
    </blockquote>
```

<p>will appear as:</p>
<div class=noindent>
    <blockquote cite=https://en.wikipedia.org/wiki/APL_%28programming_language%29>
    APL (named after the book A Programming Language) is a programming language developed
    in the 1960s by Kenneth E. Iverson.
    </blockquote>
</div>

Browsers usually indent block quote element contents.


<hr /><!-- Abbreviations -->

The `<abbr>` element may be used to define abbreviations and acronyms.

```html
    <p>The <abbr title="A Programming Language">APL</abbr> is a programming language developed from mathematical notation.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>The <abbr title="A Programming Language">APL</abbr> is a programming language developed from mathematical notation.</p>
</div>

Such elements may be of use to browsers, translation systems and search engines.


<hr /><!-- Contact Information -->

The `<address>` element may be used to identify contact information for the author of an HTML document.

```html
    <address>
    Written by Winnie-the-Pooh.<br>
    Visit us at:<br>
    Pooh Corner<br>
    Hundred Acre Wood<br>
    England<br>
    </address>
```

<p>will appear as:</p>
<div class=indent>
    <address>
    Written by Winnie-the-Pooh.<br>
    Visit us at:<br>
    Pooh Corner<br>
    Hundred Acre Wood<br>
    England<br>
    </address>
</div>

Browsers usually display the contact information in italics and add a line break before and after.


<hr /><!-- Citations -->

The `<cite>` element declares the title of a work.

```html
    <p><cite>The House at Pooh Corner</cite> by A.A.Milne.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p><cite>The House at Pooh Corner</cite> by A.A.Milne.</p>
</div>

Browsers usually display citations in italics.


<hr /><!-- Bi-directional Override -->

The `<bdo>` element is used to override the current text direction.

```html
    <p>Some text <bdo dir="rtl">back to front</bdo>.</p>
```

<p>will appear as:</p>
<div class=indent>
    <p>Some text <bdo dir="rtl">back to front</bdo>.</p>
</div>

The `dir=` attribute defines the text direction.

<hr />

</body>
</html>
