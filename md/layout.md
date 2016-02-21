<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Layouts

Web-pages, as with other publications, often display content in multiple columns.

HTML5 offers several new semantic elements to make it simpler to define the parts of a page to be laid out.

  1. `<header>`     - the header for a document or a section;
  1. `<footer>`     - the footer for a document or a section;
  1. `<nav>`        - container for navigation links;
  1. `<section>`    - a document section;
  1. `<article>`    - an independent, self contained article;
  1. `<aside>`      - sidebar and other ancillary content;

There are three ways of laying out an HTML page (using HTML tables is not recommended):

  1. use a CSS framework
  1. use the CSS float: property
  1. use the CSS3 flexbox mode

Frameworks allow you to create a layout quickly but you have to know the framework.
W3.CSS and Bootstrap are examples.


<hr /><!-- The CSS Float Property -->

The CSS float: method is quick to learn:
you need to know how the CSS float: and clear: properties work.
See [CSS Float and Clear](http://www.w3schools.com/css/css_float.asp).

The downside is that floating elements are tied to the document flow and this may harm flexibility.

Here is a suggestion as to how the navigation bar may be made to float beside the main article while
fitting in between the header and footer.

```html
header, footer {
    padding: 1em;
    color: white;
    background-color: black;
    clear: left;
    text-align: center;
}

nav {
    float: left;
    max-width: 160px;
    margin: 0;
    padding: 1em;
}
```


<hr /><!-- The CSS3 Flexbox -->

Flexbox is a new, CSS3, layout mode.
It ensures predictable and satisfactory page layout on different screen sizes and display devices.

The downside is that it does not work with older browsers (e.g. IE 10 and earlier).

This is what the CSS3 flexbox declaration might look like:

```html
@media all and (min-width: 768px) {
    .nav {text-align:left;-webkit-flex: 1 auto;flex:1 auto;-webkit-order:1;order:1;}
    .article {-webkit-flex:5 0px;flex:5 0px;-webkit-order:2;order:2;}
    footer {-webkit-order:3;order:3;}
```

See [CSS Flexbox](http://www.w3schools.com/css/css3_flexbox.asp).


<hr /><!-- Responsive Web Design -->

Responsive Web Design is about using CSS and HTML to design a web page so that it looks good on any screen
because the browser is able resize and adjust content.

You can do it yourself with the `float:` attribute or
you can use a responsive style sheet like [W3.CSS](http://www.w3schools.com/w3css/default.asp).


<hr />

</body>
</html>
