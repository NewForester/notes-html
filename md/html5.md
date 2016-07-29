<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Html5</title>
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

## HTML History

In 1989 Sir Tim Berners-Lee invents the World Wide Web and publishes HTML in 1991.

In 1999 the W3C (World Wide Web Consortium) publishes HTML 4.01 and, in 2000, XHTML.

In 2004, the W3C stops work on HTML in favour of XHTML so WHATWG
(Web Hypertext Application Technology Working Group) was formed to continue HTML development.

In 2006 W3C concedes and the two groups works together.

In 2008 the first HTML5 public draft was released.

In 2012 W3C and WHATWG split.
W3c favour a definitive HTML5 and XHTML standard, WHATWG favour a "living standard".


## HTML5 Changes

The document type declaration is now very simple:

```html
    <!DOCTYPE html>
```

as is that of the character set encoding:

```html
    <meta charset="UTF-8">
```

which is actually the default for HTML5.


<hr /><!-- New Elements -->

The most interesting new elements in HTML5 are:

 1. semantic elements         - `<header>` and so on
 1. form element attributes   - number, data, time and so on
 1. graphic elements          - `<svg>` and `<canvas>`
 1. multi-media elements      - `<audio>` and `<video>`

Older browsers can be 'taught' how to handle new elements.


<hr /><!-- HTML APIs -->

HTML APIs are also new:

 1. geolocation           - to locate a user on the globe
 1. drag and drop         - any element may be draggable
 1. local storage         - a powerful replacement for cookies
 1. application cache     - a cache for code, not just data
 1. web workers           - background scripts that do not affect page performance
 1. server sent events    - (SSE) page update without the client polling the server


<hr /><!-- Elements removed -->

A number of elements are removed:

 1. acronym     - use `<abbr>`
 1. applet      - use `<object>`
 1. basefont    - use CSS
 1. big         - use CSS
 1. center      - use CSS
 1. dir         - use `<ul>`
 1. font        - use CSS
 1. frame
 1. framset
 1. noframes
 1. strike      - use CSS or `<s>` or `<del>`
 1. tt          - use CSS

<hr />


## HTML5 Support

All modern browsers recognise HTML5.

All browsers, old and new, recognise unknown HTML elements as inline elements.
It is possible to 'teach' older browsers to handle 'unknown' elements.

Eight of the new semantic elements are block-level elements.
The CSS display property can be used to tell an old browser to treat them this way:

```html
    header, section, footer, aside, nav, main, article, figure {
        display: block;
    }
```

It is possible to add elements to an HTML page using a browser trick:

```html
    <style>
        myHero { ... }
    </style>

    <myHero>My Hero Element</myHero>
```

For IE 9 and earlier you also need:

```html
    <script>
        document.createElement("myHero")
    </script>
```

For IE 8 and earlier you also need:

```html
    <!--[if lt IE 9]>

        <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>

    <![endif]-->
```

## HTML4 to HTML5 Migration

It is possible to convert a document from HTML4 to HTML5 without destroying any of the original content or structure.

The process appears to be simple.
Change:

```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

    <meta http-equiv="Content-Type" content="text/html;charset=utf-8">
```

to:

```html
    <!DOCTYPE html>

    <meta charset="utf-8">
```

Apply the changes recommended in the previous section to support HTML5 semantic elements in older browsers.

Convert the document to use HTML5 semantic elements.  So:

```html
    <div id="header">
    <div id="menu">
    <div id="content">
    <div class="article">
    <div id="footer">
```

might become:

```html
    <header>
    <nav>
    <section>
    <article>
    <footer>
```

Be sure to change the CSS styling to match:

```html
    div#header { ... }
    div#content { ... }
    div.article { ... }
    div#footer { ... }
    div#menu ul { ... }
    div#menu ul li { ... }
```

might become:

```html
    header { ... }
    section { ... }
    article { ... }
    footer { ... }
    nav ul { ... }
    nav ul li { ... }
```

There are no hard and fast rules as to what is a section and what is an article so a certan amount of good judegement is required.
On a page by page basis, the manner in which `<div>` elements are structured in the old HTML4 may be the best guide.

</body>
</html>
