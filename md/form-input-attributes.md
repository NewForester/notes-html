<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Form-input-attributes</title>
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

Additional attributes may be used to qualify an input field.


## HTML4 Form Input Attributes

In HTML4, the additional attributes that may be used to qualify an input field are:

 1. value             - the default or initial value
 1. name              - the name the input field (submitted with the field value)
 1. disabled          - the field is disabled (it will not be submitted)
 1. readonly          - the field is read-only (its value cannot be changed by the user)
 1. checked           - pre-select checkbox or radio button field on page (form) load
 1. size              - the width (in characters) of a (text based) field
 1. maxlength         - the maximum number of characters that can be entered into the field
 1. accept            - the acceptable file type(s) for a field `type="file"`
 1. src               - the URL for a field `type="image"`
 1. alt               - the alternative text for a field `type="image"`
 1. align             - the alignment of the image for a field `type="image"` (not supported in HTML5)

The file types specified by `accept=` may be a list of comma separated file extensions, MIME types or one or more of `image/`, `audio/` and `video/*`.

The browser gives no feedback when `maxlength` is reached:  use a script to alert the user.


## HTML5 Form Input Attributes

HTML5 defines new attributes many of which imply greater validation of user input by the browser.
However, there are many ways, with and without scripts, that 'illegal' input may be submitted.
The server should do its own checking.

The additional attributes new to HTML5 are:

 1. autocomplete      - on or off: when 'on' the browser may make suggestions based on values entered previously;
 1. autofocus         - the input field should gain focus when the page in loaded (reset);
 1. dirname           - something to do with the text direction, presumably for Asian languages;
 1. form              - specifies, for a standalone `<input>` element, the forms it belongs to;
 1. height/width    - the dimensions in pixels of a field `type="image"`
 1. list              - cross-references a `<datalist>` element that pre-defines field values;
 1. min/max         - the range of values of a number field;
 1. multiple          - the user can enter more than one value in the field;
 1. pattern           - a regular expression against which data entered into the field is checked;
 1. placeholder       - text to appear in the field when the form is displayed before the user enters any data;
 1. required          - the field must be filled in before the form can be submitted;
 1. step              - often used with `min=` and/or `max=` to specify the modulus of valid values;

Not all attributes make sense with all input types but which go with which is beyond the scope of these notes.
Assume inappropriate attributes or attributes not understood by older browsers are simply ignored.

The `placeholder=` attribute is often a hint as to what the user should enter.

The `title=` attribute is often used as a tool-tip to suggest the regular expression expected by `pattern=`.

```html
   Country code: <input type="text" name="country_code" pattern="[A-Za-z]{3}" title="Three letter country code">
```

The `multiple` attribute when used with `type=file` allows the user to select more than one file using the "Browse" button.
Typically multiple selection is with shift-click or ctrl-click.

The `multiple` attribute when used with `type=email` allows the user to enter a comma separated list of e-mail addresses.

It would appear that when using the `list=` attribute, the `type=` attribute is not needed.

Normally, how a form appears derived directly from its contents.
How, then, does this work for field with the `form=` attribute ?


<hr /><!-- HTML 5 Form Override Attributes -->

HTML5 also defines the following input field attributes that may be used to override the eponymous form attribute:

 * formaction,
 * formenctype,
 * formmethod,
 * formnovalidate and
 * formtarget.

They are valid for submit fields, which rather implies a form may have more than one.
Since `formnovalidate` does not take a value, it is used to override the form default, which is validate.


<hr />

</body>
</html>
