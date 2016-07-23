<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Encodings</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML Encoding

To display an HTML document correctly, the browser must know which character set (aka encoding) the document uses.

Early HTML used ASCII character encoding.
With only 127 alphanumeric characters, it was adequate for English prose but not much else.
The `charset=` attribute of the `<meta>` element was used for documents in other languages and character entities were used for special symbols.

HTML4 uses ISO-8859-1 by default.
With 255 characters, it extends ASCII with many of the accented characters required for Western European languages.

HTML5 uses UTF-8 by default, which is a Unicode encoding.
It can encode practically any character from any character set.

UTF-8 is backwards compatible with ISO-8859-1, which is backwards compatible with ASCII.

UTF-8 is supported by all HTML4 processors so there is little reason these days not to use it.

Under recent Windows operating systems, you might need to use UTF-16.

<!-- Declaring the character encoding -->

For HTML5, the default character encoding would be declared as follows:

```html
    <meta charset="UTF-8">
```

For HTML4, the equivalent is:

```html
    <meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1">
```

When a browser detects this, is probably uses ANSI (Windows-1252) encoding.
The ANSI encoding is compatible with ISO-8859-1 but has an extra 32 characters defined.

See the [Complete HTML Character Set Reference](http://www.w3schools.com/charsets/default.asp).

<hr />

## HTML URLs

Uniform Resource Locators (URLs) are web addresses.
The (partial) alternative is an IP address.

They have the syntax:

```html
   protocol://prefix.domain:port/path/filename
```

Explanation:

 1. protocol  - the Internet protocol (aka service);
 1. prefix    - a domain prefix (default for http is www)
 1. domain    - the Internet domain name (like w3schools.com)
 1. port      - the port number at the host (default for http is 80)
 1. path      - a path at the server (the root directory of the site by default)
 1. filename  - the name of a document or resource

The better known protocols are:

 1. http      - HyperText Transfer Protocol
 1. https     - Secure HyperText Transfer Protocol
 1. ftp       - File Transfer Protocol
 1. file      - a file available through the local operating system

<hr /><!-- URL Encoding -->

URLs may only be sent over the Internet using the ASCII character set.

URL encoding converts other characters (and the space) to an ASCII representation
that consists of `%` followed by a pair of hexadecimal digits.

A space is represented by `%20` but it is often replaced by a `+` (plus sign).

User input will be encoded by the browser as necessary using the character set of the page.

A UTF-8 code point may require 2 or 3 `%` double digits.
The Euro symbol (`€`), for example, is encoded as `%E2%82%AC`.

For reference, see [URL Encoding Reference](http://www.w3schools.com/tags/ref_urlencode.asp).

</body>
</html>
