<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Scripts

JavaScript is used to add dynamic and interactive content to web pages.
A simple, but common use, is form validation.

The `<script>` element is used to delimit a client-side script.
In practice, client-side scripts are written in JavaScript.

The script is either the contents of the `<script>` element or
an external script referenced by the `src=` attribute
using a full URL or a [relative file path](file-paths.html).


Selection of HTML elements on a web page usually involves:

```javascript
    document.getElementById(id)
```

where `id` corresponds to the value of the element's `id=` attribute.

A (not exactly dynamic) example:

```html
    <script>
        document.getElementById("demo").innerHTML = "Hello JavaScript!";
    </script>
```

assigns the text "Hello JavaScript!" to the contents of the HTML element with the id "demo".

The JavaScript language is covered in more detail in a separate
[JavaScript Tutorial](http://www.w3schools.com/js/default.asp).


<hr /><!-- A Taste of JavaScript -->

JavaScript can change HTML element content:

```html
    document.getElementById("demo").innerHTML = "Hello JavaScript!";
```

JavaScript can change HTML element styles:

```html
    document.getElementById("demo").style.color = "red";
```

JavaScript can change HTML element attributes:

```html
    document.getElementById("image").src = "picture.gif";
```


<hr /><!-- The <noscript> Element -->

The `<noscript>` element is used to provide alternative content for users of browsers with scripts disabled or otherwise not supported.


<hr /><!-- The <button> Element -->

Here is a quick example of how a `<button>` element can be used as a trigger to run a JavaScript function to update the web page.

```html
    <button type="button" onclick="myFunction()">Click Me!</button>

     <p id="demo">This is a demonstration.</p>

    <script>
    function myFunction() {
       document.getElementById("demo").innerHTML = "Hello JavaScript!";
    }
    </script>
```

<hr />

</body>
</html>
