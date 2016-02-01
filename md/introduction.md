<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


These notes were made while learning HTML using the HTML5 Tutorial provided on-line by w3shools.com.
Their material is "All Rights Reserved".

HyperText Markup Language (HTML) is the standard mark-up language for creating web pages.

HTML, Cascading Style Sheets (CSS) and JavaScript are the key technologies of the World Wide Web.

HTML is the assembly language of the web:
all other mark-up languages are converted to HTML and it is HTML that is rendered by web browsers.

An understanding of HTML is therefore essential to web programming although it may be seldom used directly.

HTML emerged at CERN in 1991. It has been an international standard since 2000.
Work began on HTML5 in 2004.  It merged in 2008 but was not standardised until 2014.
At the beginning of 2017, web browsers may still not be fully HTML5 compatible.


## HTML Documents

An HTML document is a representation of a web page.
It consists of nested HTML elements and nothing more.
These describe the structure of the web page.

HTML elements are represented by HTML tags.
HTML tags label pieces of content.

HTML tags tell a browser how to display a web page.
The browser does not display the tags themselves, only their content.

Each web page has the same top level structure:

```html
    <!DocType html>
    <html>
        <head>
            <!-- metadata - not for display -->
        </head>
        <body>
            <!-- content - for display -->
        </body>
    </html
```

`<!DocType>` declares the document type.
According to the tutorial, `<!DocType html>` is sufficient to declare an HTML5 document.


## HTML Elements

All HTML documents consist of nested HTML elements: elements may contain elements.

HTML elements are represented by HTML tags.
They have the form:

```html
    <tag-name>content ...</tag-name>
```


<!-- HTML Tags -->

HTML tags (normally) come in pairs - the start (or opening) tag and the end (or closing) tag.
The closing tag is the opening tag but with a forward slash inserted before the tag name.

The closing tag is considered optional<!-- by whom - browsers, the standard ?-->.
Do not rely on this.

Elements with no content are called empty elements.
Empty elements, such as `<br>`, do not have an closing tag.

Empty elements may be closed in the opening tag thus:  `<br />`.
HTML5 does not require empty elements be closed but the stricter validation of XHTML does.

HTML tags are case insensitive but lower case is recommended.
Lower case is required for XHTML.


## HTML Attributes

Any HTML element may have HTML attributes that provide additional information.

Attributes are specified in the opening tag and (usually) come in name-value pairs with the form `name=value`.

In the HTML5 standard, attribute names are case insensitive.
However, lower case is recommended and is required for XHTML.

The HTML5 standard does not require attribute values be quoted.
However, quoting is recommended and is required for XHTML.

Quoting of attributes values that contain spaces is necessary.
Either quotes (`"..."`) or apostrophes (`'...'`) may be used.

The choice may be influenced by the value itself:

```html
    <p title="Around ' use quotes">
    <p title='Around " use apostrophe'>
```

No mention at this stage of escape sequences.


## Element and Attribute Examples

<!-- HTML Paragraphs -->

HTML Paragraphs are declared with the `<p>` tag:

```html
    <p>A paragraph.</p>
```

<!-- Title Attribute -->

The `title=` attribute may be added to the `<p>` element.

```html
    <p title="I am a tool-tip">
```

The value of the attribute may be displayed as a tool-tip.

<!-- HTML Hyper-links -->

HTML Hyper-links are declared with the `<a>` tag:

```html
    <a href="http://www.python.com">Anywhere you know ?</a>
```

The `href=` attribute specifies the hyper-link.
The content is the text displayed over the hyper-link.

The hyper-link always starts with the protocol (here `http`).

<!-- HTML Images -->

HTML Images are declared with the `<img>` tag:

```html
    <img src="python.jpg" width="104" height="142" alt="Recognise this ?" />
```

The attributes give the image's file name and the screen display size in pixels.

The `alt=` attribute specifies the alternative text to be displayed when an image cannot.
Note there is no content.

<!-- Language Attribute -->

The `lang=` attribute may be added to the `<html>` element.
It declares the language of an HTML document.  E.g.:

```html
    <html lang="en-US">
```

The first two letters specify the language, the second two, if present, the dialect.

The language is used by accessibility applications and search engines.

</body>
</html>
