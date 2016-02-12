<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Images

Images are a significant part of many web pages.

Common image formats are JPG, GIF and PNG.
GIF images may be animated (but that makes no difference to the HTML source).

<hr /><!-- Image Syntax -->

The `<img>` element defines an image.
The element is empty:  it has no text content.
The general form is:

```html
    <img src="url" alt="some_text" style="width:width;height:height;">
```

The `alt=` attribute is required.
It provides the alternative text for an image.
This is rendered if the image cannot be loaded
but is also for use by screen readers used by the visually impaired.

The `src=` attribute specifies the address of the image.
As with other Internet addresses, it may be a full URL or a [relative file path](file-paths.html).


<hr /><!-- Image Size -->

The image size should always be specified otherwise the page may flicker while the image is being loaded.

The `style=` attribute may be used to specify the image size.

```hmtl
    <img src="html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">
```

The size is specified in pixels.
Browsers appear to scale (not crop) images.


The image size may alternatively be specified using the `width=` and `height=` attributes.

```html
    <img src="html5.gif" alt="HTML5 Icon" width="128" height="128">
```

It is recommend the `style=` attribute is used to avoid internal or external styles overriding the desired image size.


<hr /><!-- Floating Images -->

Images can float either side of text.

```html
    <p>
        <img src="../images/smiley.gif" alt="Smile" style="float:right;width:42px;height:42px;border:0;">
        A smile to my right.
    </p>

    <p>
        <img src="../images/smiley.gif" alt="Smile" style="float:left;width:42px;height:42px;border:0;">
        A smile to my left.
    </p>
```

<p>will appear as:</p>
<div class=indent>
    <p>
        <img src="../images/smiley.gif" alt="Smile" style="float:right;width:42px;height:42px;border:0;">
        A smile to my right.
    </p>
    <br />
</div>
<div class=indent>
    <p>
        <img src="../images/smiley.gif" alt="Smile" style="float:left;width:42px;height:42px;border:0;">
        A smile to my left.
    </p>
    <br />
</div>


<hr /><!-- Link Images -->

To use an image as a link, simply nest the `<img>` element within the `<a>` element.

```html
    <a href="default.asp">
        <img src="../images/smiley.gif" alt="Smile" style="width:42px;height:42px;border:0;">
    </a>
````

<p>will appear as:</p>
<div class=indent>
    <a href="default.asp">
      <img src="../images/smiley.gif" alt="Smile" style="width:42px;height:42px;border:0;">
    </a>
</div>


<hr /><!-- Link Maps -->

Use the `<map>` element to define an image map.
This is an image with one or more clickable areas.

The association between the two is given by
the `usemap=` attribute of the image and the `name=` attribute of the map.

The `<map>` element contains `<area>` elements
each of which defines a clickable area and a hyper-link.
For example:

```html
    <img src="planets.gif" alt="Planets" usemap="#planetmap" style="width:145px;height:126px;">

    <map name="planetmap">
        <area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
        <area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
        <area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
    </map>
```

<hr />

</body>
</html>
