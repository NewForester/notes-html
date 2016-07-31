<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Html5-style-guide</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5


## HTML5 Style Guide

This section is coding conventions and a style guide for HTML5.
Much of it has already been recommended.

HTML5 is not as rigorous as XHTML and although XHTML may have fallen out of favour,
it is recommended the discipline of XHTML be retained.

<!-- Document Level -->

At the document level:

 1. always declare the correct document type;
 1. do not leave out the html element:  use it to specify the document language;
 1. do not leave out the body or the head elements;
 1. the title element is required:  make it meaningful;
 1. define the language and character set as early as possible;
 1. always set the view port;

```html
    <!DOCTYPE html>
    <html lang="en-GB">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>The Answer to Life, the Universe and Everything</title>
    </head>
    <body>
      <!-- Whatever you want.  Whatever you need. -->
    </body>
    </html>
```

<!-- White Space and Comments -->

With respect to white space and comments:

 1. avoid long code lines:  80 characters is suggested as a maximum;
 1. do not add blank lines without a reason:  use for readability between large or logical code blocks;
 1. use *2* spaces for indentation:  do not use the tab key;
 1. it is not necessary to indent every element;
 1. short comments should be written on one line;
 1. longer comments should be opened and closed on separate lines;


```html
    <!-- This is a short comment -->

    <!--
      A longer comment.
      Spread over several lines.
    -->
```

<!-- Elements and Attributes -->

For elements:

 1. write element names in lower case:  certainly avoid mixed case;
 1. close all elements:  never leave off the closing `</element>`;
 1. close empty elements:  use ` />`, not just `>`;
 1. write attribute names in lower case:  certainly avoid mixed case;
 1. quote all attribute values:  they are required when the value contains spaces;
 1. always supply an alt attribute to image elements;
 1. also define the image width and height to reduce flicker;
 1. do not use spaces around the *=* between attribute names and their values;

<!-- Style Sheets -->

For styles and style sheets:

 1. use simple syntax for linking to style sheets:  the type attribute is not necessary;
 1. short CSS rules may be written on one line;
 1. longer CSS rules should be split over a number of lines;

```html
    <link rel="stylesheet" href="styles.css">

    body { border-style: double; }

    body {
      background-color: lightgrey;
      font-family: "Arial Black", Helvetica, sans-serif;
      font-size: 16em;
      color: black;
    }
```

Furthermore:

 1. place the opening bracket on the same line as the selector;
 1. use one space before the opening bracket;
 1. use *2* spaces for indentation;
 1. use semicolon after each property-value pair, including the last;
 1. only use quotes around values if the value contains spaces;
 1. place the closing bracket on a new line, without leading spaces;
 1. avoid lines over 80 characters;

<!-- Loading Javascript -->

For scripts:

 1. use simple syntax for loading external scripts:  the type attribute is not necessary;

Javascript is case sensitive.  The following are not equivalent:

```javascript
    var obj = getElementById("Exemplar");

    var obj = getElementById("exemplar");
```

<!-- Lower case files names -->

For file names:

 1. use lower case file names:  these work with case and case insensitive web servers and file systems;
 1. use the file extensions `.html`, `.css` and `.js`;
 1. assume the server will default the page name to "index.html";

</body>
</html>
