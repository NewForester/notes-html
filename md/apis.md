<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML5 APIs

HTML5 standardises a number of APIs that have been supported by most major browsers for quite some time.
These are available to web pages through JavaScript.

The most used are:

 1. geolocation
 1. drag/drop
 1. local storage          - Storage objects
 1. application cache
 1. web workers           - Worker objects
 1. server sent events    - EventSource objects

A web page that uses one of these should best check the browser does actually supports it:

```JavaScript
    if(typeof(EventSource) !== "undefined") {
      // Yes! Server-sent events support!
      // Some code.....
    } else {
      // Sorry! No server-sent events support..
    }
```

### HTML Geolocation

The HTML Geolocation API is used to determine the browser's position on the globe.

The location may be requested by a local client but the assumption is that it is passed to a server.
This may compromise privacy, so the user's agreement is required.

The accuracy of the geolocation depends on the device on which the browser is running.
It is good on devices with GPS, such as smart phones, but may be dreadful on old desktops.

The main methods of the API are:

  * getCurrentPosition,
  * watchPosition and
  * clearWatch

The first is useful from providing local information such as nearby points of interest.
The last two are useful for turn-by-turn navigation.

The data returned by `getCurrentPosition()` always gives:

  * latitude,
  * longitude and
  * accuracy

as decimal numbers. <!-- But what are the units ? -->

The method will also return the following, if available:

  * altitude (and accuracy),
  * heading,
  * speed and
  * timestamp

Personally, I have never agreed to sharing my location.


### HTML5 Drag and Drop

In HTML5 any element can be dragged and dropped.

Use the `draggable=` attribute on the element to be dragged:

```html
   <img draggable="true">
```

Declare an event handler that records what to drag:

```JavaScript
    function drag(ev) {
        ev.dataTransfer.setData("text", ev.target.id);
    }
```

When the element is dragged over another element, another event occurs but the default is to not allow the element to be dropped.
The default behaviour must be overruled.

```JavaScript
    function allowDrop(ev) {
        ev.preventDefault();
    }
```

When the element is dropped, a third event occurs so a third handler is needed to say what happens.

```JavaScript
    function drop(ev) {
        ev.preventDefault();
        var data = ev.dataTransfer.getData("text");
        ev.target.appendChild(document.getElementById(data));
    }
```

These three handlers deal with events, not elements.
The elements are identified by attributes that add the event handlers to the elements.

```html
    <div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

    <div id="div2"
      <img src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">
    </div>
```

### HTML Local Storage

HTML Local Storage is an alternative to cookies.

Information can be stored locally within the browser.
It is never transferred to the server.
Local storage is by domain and protocol: there is no sharing between web sites.

This appears to have advantages for both server load and client privacy.

There are local storage objects, with no expiry date, and session storage objects, that are lost when the browser tab is closed.

Data is stored in name/value pairs.
The value is always a string.

There are two means of access:

```html
    localStorage.setItem("lastname", "Smith");
    localStorage.getItem("lastname");
    localStorage.removeItem("lastname");
```

and

```html
    localStorage.lastname = "Smith";
    localStorage.lastname;
```

I do not know where this is stored nor when it is purged or whether permission is sought or not (I don't think it is).

### HTML Application Cache

The HTML Application Cache is where web applications can be stored for offline use.
That is when the there is no Internet connection.

The advantages are:

 1. offline browsing - the application may be used even with no Internet connection
 1. speed - cached resources load faster
 1. reduced server load - only updated/changed resources are downloaded

An HTML document declares it wants to use the application cache using the `manifest=` attribute to reference a manifest file.

```html
    <html manifest="demo.appcache">
```

The file type `.appcache` is recommended and
the web server must be configured to supply the file with MIME type "text/cache-manifest".

The manifest file is a simple text file with three sections:

 1. CACHE MANIFEST    - cache these files on first download;
 1. NETWORK           - never cache these files;
 1. FALLBACK          - use cached file when on-line file(s) is(are) not available;

The first section must be declared first.
`*` (asterisk) indicates all other files and resources.

The last section comprises a URI and a fall-back file. Eg:

```
    FALLBACK:
    /html/      /offline.html
```

for any file in the `/html/` directory, use `/offline.html` as fall-back.

Lines starting with `#` are comments.

Once an application is cached, it remains so until:

 1. the user clears the browser application cache;
 1. the application cache size limit is reached;
 1. the manifest file on the server is modified;
 1. it is updated by JavaScript.

To trigger cache updates when other files or resources are changed, use a comment with the form:

```
    # 2017-01-30 v1.0.1
```

in the manifest file and make sure it is updated.

My browser is set to ask before caching an application.
I don't remember it ever doing this.

### HTML Web Workers

An HTML Web Worker is a JavaScript run in the background.
When some other script runs (in the foreground) the browser appears to hang until the script finishes.

Web workers are external scripts:
they have no access to (significant) DOM objects such as the window, document or parent objects.

Here is an example:

```JavaScript
    var i = 0;

    function timedCount() {
      i = i + 1;
      postMessage(i);
      setTimeout("timedCount()",500);
    }

    timedCount();
```

saved in "worker.js";

The important part here is the call to the `postMessage()` method.
This posts a message back to the web page.

The worker is created (and started) by the web page creating a Worker object:

```JavaScript
    if (typeof(w) == "undefined") {
        w = new Worker("worker.js");
    }
```

The web page may send and receive messages to and from the worker.
An event listener is needed to receive:

```JavaScript
    w.onmessage = function(event) {
        document.getElementById("result").innerHTML = event.data;
    };
```

The only HTML required is declaring where the message appears:

```html
    <p>Count numbers: <output id="result"></output></p>
```

There should be code to terminate the worker and allow another instance to be created later:

```html
    w.terminate();
    w = undefined;
```


### HTML Server Sent Events

HTML SSE (Server Sent Events) allow the server to send events to the browser client instead of the client polling the server.

This allows browser web pages to keep up to date in real time without huge overhead.

An application might be a news feed.
It is an important feature of social media sites.

An EventSource object must be created that declares the server entity that will generate events:

```JavaScript
    var source = new EventSource("sse.php");
```

Event handlers should be defined for:

 1. onopen      - when a connection to the server is opened
 1. onmessage   - when a message is received from the server
 1. onerror     - when an error occurs

The most important is the second of these:

```html
    source.onmessage = function(event) {
        document.getElementById("result").innerHTML += event.data + "<br>";
    };
```

It seems there is no shut down method.

</body>
</html>
