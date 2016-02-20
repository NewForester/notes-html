<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Head

The `<head>` element is a container for meta-data
that is placed after the `<html>` tag before the `<body>` tag.

Meta-data is data about the HTML document that is not displayed on the web page.
It includes:

  1. `<title>`  - the title of the document;
  1. `<base>`   - the base URL for address and target URLs on the web page;
  1. `<meta>`   - general purpose meta data;
  1. `<style>`  - style information specific to the web page;
  1. `<link>`   - the address of an external CSS style sheet (or similar);
  1. `<script>` - a client side script;

The HTML5 standard allows the `<html>`, `<head>` and `<body>` tags to be omitted.
Omitting the `<head>` tag has been common practice for quite some time.
However, W3Schools recommends none of these tags are omitted.


<hr /><!-- The Title Element -->

The `<title>` element declares the title of the HTML document.
It is required by the standards and provides a title for:

  * browser tabs,
  * page bookmarks and
  * search engine results.

A simple example:

```html
    <title>My First Page</title>
```


<hr /><!-- The Base Element -->

The `<base>` element may be used to define a base URL for all relative paths and targets (and how open them).
For example:

```html
    <base href="http://www.w3schools.com/images/" target="_blank" />
```


<hr /><!-- The Meta Element -->

The `<meta>` element provides general meta-data used by the browsers, search engines and other web services.
Examples include:

```html
    <meta charset="UTF-8" />
    <meta name="description" content="Free Web tutorials" />
    <meta name="keywords" content="HTML, CSS, XML, JavaScript" />
    <meta name="author" content="John Doe" />
    <meta http-equiv="refresh" content="30" />
```

A document may have as many `<meta>` elements as it needs.
There are a limited number of values the `name=` attribute may take.

HTML5 introduced a mechanism that allows web designers to take control of the view port using a `<meta>` element.
So that web pages may have a reasonable initial appearance on all devices, it is recommended you include the following by default:

```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This instructs the browser to use a reasonable zoom level and use the full width of the screen.


<hr /><!-- The Style Element -->

The `<style>` element defines style information used to format this web page.
A simple example:

```html
    <style>
      body {background-colour: powderblue;}
    </style>
```


<hr /><!-- The Link Element -->

The `<link>` element references an external style sheet to be used to format this and other web pages.
A web page may have several `<link>` elements.

```html
    <link rel="stylesheet" href="style-sheet.css">
```

Potentially this element may reference external files other than just style sheets.


<hr /><!-- The Script Element -->

The `<script>` element is used to define a client-side (JavaScript) script.
I expect there may be several such elements in the same document.
See the [HTML Scripts](scripts.html) page.

The `<noscript>` element may be used to provide text to be displayed when the browser is not script capable or scripts have been disabled.


<hr />

</body>
</html>
