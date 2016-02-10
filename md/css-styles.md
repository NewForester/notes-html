<!DOCTYPE html>
<html>

<head>
    <style>
        h4      {color: red;}

        #p01  {
            color: red;
            font-family: courier;
            font-size: 160%;
        }
        p.surrounded {
            border: 1px solid powderblue;
            padding: 30px;
            margin: 50px;
        }
    </style>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
    <link rel="stylesheet" href="../styles/css-styles.css" />
</head>

<body>
# HTML5


## HTML Styles - CSS

CSS (Cascading Style Sheets) describe how HTML elements are to be rendered (on screen, paper or other media).
It is covered in detail in the [CSS Tutorial](http://www.w3schools.com/css/default.asp).
Since one style sheet can apply to many elements on many web pages, it can save a lot of work.

CSS styles can be applied to an element:

  1. inline   - using the style attribute of a single HTML element
  1. internal - using the `<style>` element in the `<head>` section of an HTML document
  1. external - using a CSS style sheet (often across all pages of a web site)


<hr /><!-- Inline CSS -->

Inline CSS is used to apply a unique style to a single HTML element
by using the `style=` attribute of the element.

```html
    <h3 style="color:blue;">This is a Blue Heading</h3>
```

<p>will appear as:</p>
<div class=indent>
    <h3 style="color:blue;">A Blue Heading</h3>
</div>


<hr /><!-- Internal CSS -->

Internal CSS is used to define a style for a single HTML page
using the `<style>` element in the `<head>` section of a page.

```html
    <head>
        <style>
            h4      {color: red;}
        </style>
    </head>
    <body>
        <h4>A Red Heading</h4>
    </body>
```

<p>will appear as:</p>
<div class=indent>
    <h4>A Red Heading</h4>
</div>
</div>


<hr /><!-- External CSS -->

An external style sheet is used to define the style for many HTML pages
by using the `<link>` element in the `<head>` section of a page.
The appearance of an entire web site can be defined in a single file.

```html
    <head>
        <link rel="stylesheet" href="css-styles.css" />
    </head>
    <body>
        <h5>A Green Heading</h5>
    </body>
```

<p>will appear as:</p>
<div class=indent>
    <h5>A Green Heading</h5>
</div>

The style sheet "css-styles.css" will contain (at least):

```html
    h5      {color: green;}
```

External style sheets can be referenced using a full URL or a [relative file path](file-paths.html).

<hr />


## HTML Styles and CSS Properties

<!-- CSS Properties -->

There are many CSS properties.
Here are some of those used most often.

  1. color         - defines the text color;
  1. font-family   - defines the text font;
  1. font-size     - defines the text size;
  1. border        - defines a border around an element:
  1. padding       - defines a padding (space) between text and the border:
  1. margin        - defines a margin (space) outside the border:


<hr /><!-- The id attribute -->

The `id=` attribute may be used to apply a specific style set to one element.
The intention is that an element id is unique within a page.

```html
    #p01  {
        color: red;
        font-family: courier;
        font-size: 160%;
    }
```

<p>Then</p>

```html
    <p id="p01">I am different</p>
```

<p>will appear as:</p>
<div class=indent>
    <p id="p01">I am different</p>
</div>


<hr /><!-- The class attribute -->

The `class=` attribute may be used to apply a specific style set to a set of elements.

```html
    p.surrounded {
        border: 1px solid powderblue;
        padding: 30px;
        margin: 50px;
    }
```

<p>Then</p>

```html
    <p class="surrounded">Help ! Get me out of here !</p>
```

<p>will appear as:</p>
<div class=noindent>
    <p class="surrounded">Help ! Get me out of here !</p>
</div>

<hr />

</body>
</html>
