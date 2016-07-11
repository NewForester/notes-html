<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Links</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Links

Hyper-links (aka links) are what make the web a web.
Navigating from page to page is as simple a clicking on a link.
Although a web pages is not required to have links, almost all of them do.

Links are most often text but may be an image or any HTML element.
The text is usually underlined to indicate the link is there.

When you move the mouse over a link, the mouse 'arrow' will change shape
to indicate you can now click to follow the link.
Usually the 'arrow' changes into a small hand.

<hr /><!-- Link Syntax -->

The `<a>` (anchor) element defines a hyper-link.
The general form for link with text is:

```html
    <a href="url">link text</a>
```

An example:

```html
    <a href="https://www.python.org/">The Python Software Foundation</a>
```

<p>will appear as:</p>
<div class=indent>
    <a href="https://www.python.org/">The Python Software Foundation</a>
    <br />
</div>

The link address:

  1. is given by the `href=` attribute (https://www.python.org/);
  1. may be a full URL or a [relative file path](file-paths.html);
  1. without a forward slash may result in two browser requests being sent to the server.

The link text:

  1. is the visible part (The Python Software Foundation);
  1. is the active part that will send you to the link address when clicked;
  1. is usually displayed in a different colour from ordinary text.


<hr /><!-- Link Colours -->

The link text is displayed in different colours.  By default:

 1. blue - an unvisited link
 1. purple - a visited link
 1. red - the active link

The default colours can be overridden using styles:

```html
   <style>
       a:link    {color:green;  background-color:transparent; text-decoration:none}
       a:visited {color:pink;   background-color:transparent; text-decoration:none}
       a:hover   {color:red;    background-color:transparent; text-decoration:underline}
       a:active  {color:yellow; background-color:transparent; text-decoration:underline}
   </style>
```

<hr /><!-- Link Target -->

The `target=` attribute specifies where in the browser
the web page addressed by the hyper-link should be opened.

  1.  _blank     - open in a new window/tab
  1.   _self     - open in the same window/tab as it was clicked (the default)
  1.  _parent    - open in the parent frame
  1.  _top       - open in the full body of the window
  1.  frame-name - open in a named frame

This example will open the linked document in a new browser window/tab:

```html
    <a href="https://www.python.org/" target="_blank">The Python Software Foundation</a>
```

<!-- Quoi ? -->
Use `target="_top"` to break out of the frame when your web page is locked in a frame.


<hr /><!-- Images as Links -->

It is common to use images as links:

```html
    <a href="default.asp">
        <img src="../images/smiley.gif" alt="Smily Face" style="width:42px;height:42px;border:0;">
    </a>
```

<p>will appear as:</p>
<div class=indent>
    <a href="default.asp">
        <img src="../images/smiley.gif" alt="Smily Face" style="width:42px;height:42px;border:0;">
    </a>
    <br />
</div>

The `border:0;` prevents Internet Explorer (9 and earlier) displaying a border around the image-as-a-link.


<hr /><!-- Link Bookmarks -->

HTML bookmarks allow readers to jump to specific parts of a web page.
Any HTML element can be a bookmark but usually bookmarks are headings.

The `id=` attribute is used to define a bookmark:

```hmtl
    <h2 id="biblio">Bibliography</h2>
```

To reference the bookmark from this page:

```html
    <a href="#biblio">Visit the Bibliography</a>
```

To reference the bookmark from another page:

```html
    <a href="biblio.html#biblio">Visit the Bibliography</a>
```

<hr />

</body>
</html>
