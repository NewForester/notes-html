<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Form Elements</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML4 Form Elements

The HTML4 elements that may appear inside a `<form>` element are:

  1. input    - by far the most important;
  1. label    - used to add a label to an `<input>` element;
  1. select   - used to define drop down lists;
  1. option   - provides `<select>` (and `<datalist>`) elements with options to select;
  1. optgroup - used to group and label `<option>` elements;
  1. textarea - used for multi-line input;
  1. button   - used to define additional clickable buttons;
  1. fieldset - used to group related form elements;
  1. legend   - provides a `<fieldset>` element with a caption;

The `<input>` element is by far the most important form element.
How  they are displayed depends on their `type=` attributes as described on the [Input Types](forms-input-type.html) page.


<hr /><!-- Grouping Form Data -->

The `<fieldset>` element may be used to group related fields and the `<legend>` element to give the field set a caption.
The browser will draw a box around the field set.

```html
    <fieldset>
      <legend>Personal information:</legend>
      First name:       <input type="text" name="firstname" value="Mickey"><br>
      Last name:        <input type="text" name="lastname" value="Mouse"><br>
    </fieldset>
```

<p>will appear as:</p>
<div class=indent>
    <fieldset>
      <legend>Personal information:</legend>
      First name:       <input type="text" name="firstname" value="Mickey" ><br>
      Last name:        <input type="text" name="lastname" value="Mouse" ><br>
    </fieldset>
</div>


<hr /><!-- Clickable Buttons -->

Clickable buttons (in addition to the submit and reset buttons) may be defined with the `<button>` element.
The button legend is the element content.

```html
    <button type="button" onclick="alert('Hello World!')">
      Click Me!
    </button>
```

<p>will appear as:</p>
<div class=indent>
    <button type="button" onclick="alert('Hello World!')">
      Click Me!
    </button>
</div>

The `onclick=` attribute defines the action taken when the button is clicked.
Presumably this is a script action.


<hr /><!-- Text Areas -->

A text area is a multi-line input field whose height and width are defined in characters:

```html
    <textarea name="message" rows="10" cols="30">
      The cat sat on the mat.
    </textarea>
```

<p>will appear as:</p>
<div class=indent>
    <textarea name="message" rows="3" cols="30">
      The cat sat on the mat.
    </textarea>
</div>

The element content is displayed in the text area.


<hr /><!-- Drop Down Lists -->

The `<select>` element is used, in conjunction with `<option>` elements, to define a drop-down list.
The `selected` attribute may be used to 'pre-select' an option, otherwise the first option is selected.
The `<optgroup>` element may be used to group options.

```html
    <select>
      <optgroup label="Swedish Cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
      </optgroup>
      <optgroup label="German Cars">
         <option value="mercedes">Mercedes</option>
         <option value="audi">Audi</option>
       </optgroup>
    </select>
```

<p>will appear as:</p>
<div class=indent>
    <select>
      <optgroup label="Swedish Cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
      </optgroup>
      <optgroup label="German Cars">
         <option value="mercedes">Mercedes</option>
         <option value="audi">Audi</option>
       </optgroup>
    </select>
</div>


<hr /><!-- Input Field Labels -->

The `<label>` element can be used instead of plain text to provide a field with a label.
The `for=` attribute of the `<label>` tag must be the same as the `id=` attribute of the `<input>` tag.

```html
    <input type="radio" name="gender" id="male" value="male">
    <label for="male">Male</label><br>
    <input type="radio" name="gender" id="female" value="female">
    <label for="female">Female</label><br>
    <input type="radio" name="gender" id="other" value="other">
    <label for="other">Other</label><br>
```

<p>will appear as:</p>
<div class=indent>
    <input type="radio" name="gender" id="male" value="male">
    <label for="male">Male</label><br>
    <input type="radio" name="gender" id="female" value="female">
    <label for="female">Female</label><br>
    <input type="radio" name="gender" id="other" value="other">
    <label for="other">Other</label><br>
</div>

The use of the extra field improves usability since the label, not just the radio button, may be clicked.


## HTML5 Form Elements

The form elements new with HTML5 are:

 1. datalist  - used for short drop-down lists with pre-defined choices;
 1. keygen    - used for the generation of a public-private key pair;
 1. output    - used for a derived field perhaps calculated by a script;

New elements not recognised by older browsers will simply be ignored.

With `<keygen>`, the public key is sent to the server while the private key is stored locally.
The private key is later used to authenticate the client with the server.

The `<datalist>` list element provides a list of values to be used with an `<input>` element.
The two are linked by their `id=` and `list=` attributes.

```html
    <input list="browsers">
    <datalist id="browsers">
      <option value="Internet Explorer">
      <option value="Firefox">
      <option value="Chrome">
      <option value="Opera">
      <option value="Safari">
    </datalist>
```

<p>will appear as:</p>
<div class=indent>
    <input list="browsers">
    <datalist id="browsers">
      <option value="Internet Explorer">
      <option value="Firefox">
      <option value="Chrome">
      <option value="Opera">
      <option value="Safari">
    </datalist>
</div>

Compare and contrast with the `<select>` element, which also uses `<option>` elements.

</body>
</html>
