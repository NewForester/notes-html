<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML5 Multimedia

Multimedia is the combination of audio and visual media such as in a film.
This includes images, music, sound, videos, animation and graphics
although images and graphics under HTML are covered elsewhere.

Browsers have handled multimedia through plug-ins for a very long time.

HTML5 includes standard support for multimedia without plug-ins.
Major browsers had provided this support before the standard.


### HTML5 Video

The common video formats are:

 1. MPEG      - by Moving Pictures Expert Group
 1. AVI       - by Microsoft - Audio Video Interleave
 1. WMV       - by Microsoft - Windows Media Video
 1. QuickTime - by Apple
 1. RealVideo - by Read Media (for low bandwidth video streams)
 1. Flash     - by Macromedia (often needs a plug-in)
 1. Ogg       - by Xiph Org Foundation (Open Source)
 1. WebM      - by Mozilla, Opera, Google and others
 1. MP4       - Moving Pictures Expert Group but based on QuickTime

HTML5 requires support of MP4, WebM and Ogg.
The MIME types are as you would expect (video/mp4 etc).

All major browsers support MP4.
Internet Explorer and Safari do not support WebM or Ogg.

The `<video>` element provides a standard way to embed video in an HTML document.
Before HTML5, video could only be played in a browser using a plug-in.

```html
    <video width="320" height="240" controls>
      <source src="movie.mp4" type="video/mp4">
      <source src="movie.ogg" type="video/ogg">
      Your browser does not support the video tag.
    </video>
```

Specifying dimensions for the element is recommended to avoid flicker during page load.

The `controls` attribute tells the browser to add video controls such as play and pause.
An alternative is `autoplay` but this attribute is not supported by some popular mobile devices.

The `<source>` element allows the specification of alternative files and formats.
The file type of media files is often an indication of the format of the media content.
However, the MIME type, not the file type, is used.

The content is displayed only if the browser does not support the `<video>` element.

HTML5 defines DOM methods, properties and events for the `<video>` element that allow
web pages, through scripts, to act as fully functional video playback devices.
See the [HTML5 Audio/Video DOM Reference](https://www.w3schools.com/tags/ref_av_dom.asp).


### HTML5 Audio

The common audio formats are:

 1. MIDI      - Musical Instrument Digital Interface (sound cards)
 1. RealAudio - by Read Media (for low bandwidth audio streams)
 1. WMA       - by Microsoft - Windows Media Audio
 1. AAC       - by Apple - Advanced Audio Coding
 1. WAV       - by IBM and Microsoft
 1. Ogg       - by Xiph Org Foundation (Open Source)
 1. MP3       - the sound part of MPEG
 1. MP4       - the sound part of MP4

HTML5 requires support of MP3, WAV and Ogg.
The MIME type for MP3 is (audio/mpeg); the others are as you would expect.

All major browsers support MP3.
Internet Explorer and Safari do not support Ogg and Internet Explorer also does not support WebM.

The `<audio>` element provides a standard way to embed audio in an HTML document.
Before HTML5, audio could only be played in a browser using a plug-in.

```html
    <audio controls>
      <source src="horse.ogg" type="audio/ogg">
      <source src="horse.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
```

The `controls` attribute tells the browser to add audio controls such as play and pause.

The `<source>` element allows the specification of alternative files and formats.
The file type of media files is often an indication of the format of the media content.
However, the MIME type, not the file type, is used.

The content is displayed only if the browser does not support the `<audio>` element.

HTML5 defines DOM methods, properties and events for the `<audio>` element that allow
web pages, through scripts, to act as fully functional audio playback devices.
See the [HTML5 Audio/Video DOM Reference](https://www.w3schools.com/tags/ref_av_dom.asp).


### HTML5 Plug-ins

A plug-in is a helper application that extends the functionality of a (browser) application.
Well known but less often used are Java applets.
Examples include map display, virus scanning, and bank id verification

The `<object>` element may be used to embed plug-ins, snippets of HTML and even images.
It is supported by all browsers.

```html
    <object width="400" height="50" data="bookmark.swf"></object>
    <object width="100%" height="500px" data="snippet.html"></object>
    <object data="audi.jpeg"></object>
```

The `<embed>` element may also be used to embed objects and has been supported by all the major browsers for years.

```html
    <embed width="400" height="50" src="bookmark.swf" />
    <embed width="100%" height="500px" src="snippet.html" />
    <embed src="audi.jpeg" />
```

The difference between the two is that `<object>` elements can have content that is displayed if the `data=` file cannot be found
while `<embed>` has no closing tag, so no content.

When it comes to images, the difference between `<img>` and `<embed>` is that the former requires the `alt=` attribute while the latter ignores it.

Since `<embed>` has no alternative text mechanism I guess it is not recommended.


### HTML5 YouTube Videos

It is stated that one of the easiest ways to play videos is to use YouTube.
This may be less work than converting video formats.

When you save or play a YouTube video, an id is displayed.
You can refer to this in HTML code.

To embed a YouTube video in HTML:

 1. upload the video to YouTube;
 1. take note of the video id;
 1. define an `<iframe>` element;
 1. set the `src=` attribute to references the video;
 1. set the width an height attributes to the specify the player dimensions;
 1. add other URL parameters.

Other URL parameters include autoplay, loop, a playlist and controls.

```html
    <iframe width="420" height="315"
      src="https://www.youtube.com/embed/XGSy3_Czz8k">
    </iframe>
```

Note `<iframe>` is supported by HTML5; it is `<frame>` and `<frameset>` that are not.
The use of `<object>` and `<embed>` is deprecated.

</body>
</html>
