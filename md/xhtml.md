<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML and XHTML

XHTML is HTML written as XML:

  1. XHTML stands for eXtensible HyperText Markup Language;
  1. it is HTML defined as an XML application
  1. it is supported by all major browsers
  1. it is almost identical;
  1. it is stricter;

By writing XHTML documents, you adhere to a stricter standard, which should mean better documents.
There is certainly nothing to be lost by doing so.

<hr /><!-- Differences -->

Differences in document structure:

  1. `DOCTYPE` is mandatory
  1. the `xmlns` attribute of the `<html>` element is mandatory
  1. `<html>`, `<head>`, `<title>` and `<body>` elements are mandatory
  1. there can only be one root element

For example:

```html
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

    <html xmlns="http://www.w3.org/1999/xhtml">

    <head>
      <title>Title of document</title>
    </head>

    <body>
      some content
    </body>

    </html>
```

XHTML elements:

  1. must be closed
  1. must be properly nested
  1. must be in lower case

Elements must be closed so `<br />` not `<br>`.

XHTML attribute:

  1. names must be in lower case
  1. values must be quoted
  1. values cannot be minimised

Minimisation is not allowed, so `checked="checked"` not simply `checked`.

It is possible to validate XHTML documents on-line.

See also the [XML Tutorial](http://www.w3schools.com/xml/default.asp).

</body>
</html>
