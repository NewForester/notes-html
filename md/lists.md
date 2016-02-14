<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Lists

HTML defines three types of list:

  1. unordered lists;
  1. ordered lists;
  1. description lists.

List items can contain other HTML elements, not just text.
A nested list is list item that is, itself, a list element.


<hr /><!-- Unordered Lists -->

The `<ul>` element defines an unordered list.
The `<li>` element defines individual list items.

```html
    <ul>
      <li>Orange</li>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
```

<p>will appear as:</p>
<div class=indent>
    <ul>
      <li>Orange</li>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
</div>

The `list-style-type` property may be used to specify an alternative marker for list items.

  1. disc   - bullet marker (the default)
  1. circle - circle marker
  1. square - a black square
  1. none   - no marker


<hr /><!-- Ordered Lists -->

The `<ol>` element defines an ordered list.
List items are numbered.


```html
    <ol>
      <li>Orange</li>
      <li>Apple</li>
      <li>Banana</li>
    </ol>
```

<p>will appear as:</p>
<div class=indent>
    <ol>
      <li>Orange</li>
      <li>Apple</li>
      <li>Banana</li>
    </ol>
</div>

The `type=` attribute may be used to specify alternative numbering for list items.

  1. type="1"   - numbers (the default)
  1. type="A"   - uppercase letters (A, B, ...)
  1. type="a"   - lowercase letters (a, b, ...)
  1. type="I"   - uppercase Roman numerals (I, II, ...)
  1. type="i"   - lowercase Roman numerals (i, ii, ...)


<hr /><!-- Description Lists -->

The `<dl>` element defines an description list.

It is a list of terms with a description for each.
The `<dt>` and `<dd>` elements define terms and descriptions respectively.

```html
    <dl>
      <dt>Orange</dt>
      <dd>a citrus fruit</dd>
      <dt>Banana</dt>
      <dd>a tropical fruit</dd>
    </dl>
```

<p>will appear as:</p>
<div class=indent>
    <dl>
      <dt>Orange</dt>
      <dd>a citrus fruit</dd>
      <dt>Banana</dt>
      <dd>a tropical fruit</dd>
    </dl>
</div>


<hr /><!-- Horizontal Lists -->

CCS styles can be used to style lists in many different ways.
A common example is to list elements horizontally and turn list items into a selection menu.

```html
    <head>
      <style>
        ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: #333333;
        }

        li {
            float: left;
        }

        li a {
            display: block;
            color: white;
            text-align: center;
            padding: 16px;
            text-decoration: none;
        }

        li a:hover {
            background-color: #111111;
        }
      </style>
    </head>

    <body>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#news">News</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#about">About</a></li>
      </ul>
    </body>
```

<hr />

</body>
</html>
