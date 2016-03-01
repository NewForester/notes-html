<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML5 Elements

Elements such as `<form>` and `<table>` indicate the nature of their contents.
In contrast elements such as `<div>` and `<span>` do not:  they have no semantics.

Semantic elements are useful to machine readers of web pages - indexers and search engines as well a screen readers.

HTML5 introduces some important new semantic elements.
They are supported by all modern browsers and older browsers can be taught to treat them as block elements.

The new elements are intended to make conventions such as `<div id="nav">`, `<div class="header">` and `<div id="footer">` obsolete.
They are:

 1. article       - a grouping of self contained contents
 1. aside         - secondary information (such as a sidebar)
 1. details       - details that can be hidden/revealed by user action
 1. figcaption    - a caption for an image and for forth
 1. figure        - to group a caption with an its image and so forth
 1. footer        - meta-information, such as copyright, about a page, section
 1. header        - introductory text for a page, section or article
 1. main          - the content of a page that is not repeated elsewhere
 1. mark          - in-line element that serves to highlight text
 1. nav           - major block of navigation links
 1. section       - a thematic grouping of contents, typically with a heading
 1. summary       - a summary for `<details>` that cannot be hidden
 1. time          - denotes a human readable date/time (with machine readable value)

One might expect a page to have a header and footer and often a navigation bar (`<nav>`).
Beyond that it is not clear how these elements will be used in practice.

Does a section have article or vice versa or are they mutually exclusive ?
There are no guidelines and nesting is perfectly possible.

Many of the other elements new with HTML5 may the thought of as structural elements:

 1. bdi       - used to isolate text that might be formatted in a different direction from its surroundings
 1. dialog    - defines a dialogue box or window
 1. menuitem  - a command/menu item that may be invoked from a pop-up menu
 1. meter     - a scalar measurement within a known range (i.e. display a gauge)
 1. progress  - a progress bar (not the same as a gauge)
 1. wbr       - indicates a word break opportunity in a long word

There are now elements for [graphics](graphics.html):

 1. canvas    - draw graphics on the fly (usually with JavaScript)
 1. svg       - draw scalable vector graphics

There are also new elements for [media](media.html):

 1. audio     - defines sound content
 1. embed     - defines containers for external applications (i.e. plug-ins)
 1. source    - defines sources for `<audio>` and `<video>`
 1. track     - defines tracks for `<audio>` and `<video>`
 1. video     - defines video or 'movie' content

There are three elements for East Asian topography:

 1. rp        - what to show in browsers that do not support ruby notation
 1. rt        - ruby notation explanation / pronunciation
 1. ruby      - spans ruby notation

There are three are new [form](forms-elements.html) elements:

 1. datalist  - pre defined option for input controls
 1. keygen    - key pair generator for forms
 1. output    - for the display of a derived value

and a large number of new [types and attributes](form-input-types.html) for the form input element.

HTML5 accepts four syntax variants for attributes:

 1. empty         - `disabled`
 1. unquoted      - `value=John`
 1. single quoted - `value='John Doe'`
 1. double quoted - `value="John Doe"`

The last is recommended for compatibility with XHTML.

</body>
</html>
