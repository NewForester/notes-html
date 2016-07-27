<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Form-input-types</title>
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


## HTML4 Input Element Types

In HTML4, the `type=` attribute for the `<input>` element is one of the following:

 1. text     - a one-line text input field;
 1. password - a password field - data entered is masked;
 1. submit   - a button for submitting data entered by the user to a form handler;
 1. image    - an image rather than a button that is used to submit data entered by the user to a form handler;
 1. reset    - a button to clear the form and reset fields to their default values;
 1. button   - a button other than the submit or reset button that performs some other action;
 1. radio    - one of a limited number of choices of which the user may select only one;
 1. checkbox - one of a limited number of choices of which the user may select more than one or none at all;
 1. file     - a Browse... button that allows one or more files to be selected for upload;
 1. hidden   - a hidden input field (perhaps set or revealed by a script);

<hr /><!-- The Input Type Button -->

The default legend for the submit and reset buttons is "Submit Query" and "Reset" respectively.

```html
    <form>
      <input type="button" onclick="alert('Hello World!')" value="Click Me!">
    </form>
```

<p>will appear as:</p>
<div class=indent>
    <form>
      <input type="button" onclick="alert('Hello World!')" value="Click Me!">
    </form>
</div>


<hr /><!-- The Radio Button -->

The user can select only one radio button with the same `name=` attribute.

```html
    <form>
      <input type="radio" name="gender" value="male" checked> Male<br>
      <input type="radio" name="gender" value="female"> Female<br>
      <input type="radio" name="gender" value="other"> Other
    </form>
```

<p>will appear as:</p>
<div class=indent>
    <form>
      <input type="radio" name="gender" value="male" checked> Male<br>
      <input type="radio" name="gender" value="female"> Female<br>
      <input type="radio" name="gender" value="other"> Other
    </form>
</div>


<hr /><!-- The Checkbox -->

The user can select none, one or more check boxes.
The `name=` attribute need not be unique.

```html
    <form>
      <input type="checkbox" name="vehicle1" value="Bike"> I have a bike<br>
      <input type="checkbox" name="vehicle2" value="Car"> I have a car<br>
      <input type="checkbox" name="vehicle3" value="Plane"> I have a plane<br>
    </form>
```

<p>will appear as:</p>
<div class=indent>
    <form>
      <input type="checkbox" name="vehicle1" value="Bike"> I have a bike<br>
      <input type="checkbox" name="vehicle2" value="Car"> I have a car<br>
      <input type="checkbox" name="vehicle3" value="Plane"> I have a plane<br>
    </form>
</div>


## HTML5 Input Element Types

The type attributes for the `<input>` element new with HTML5 are:

 1. color            - the browser may pop-up a colour picker;
 1. date             - the browser may pop-up a date picker;
 1. datetime-local   - the browser may pop-up a date/time picker;
 1. email            - the browser may check the e-address entered by the user is well formed;
 1. month            - the browser may pop-up a month + year picker;
 1. number           - data entered must be a number (eventually within a range);
 1. range            - the browser may display a slider;
 1. search           - behaves like a regular text field;
 1. tel              - the browser may check the telephone number entered is well formed;
 1. time             - the browser may pop-up a time picker;
 1. url              - the browser may check the URL entered is well formed;
 1. week             - the browser may pop-up a week number + year picker;

New input types that are not supported by older web browsers will behave as `<input type="text">`.
Many of these are intended to allow the browser to do more input validation without the use of scripts.

The `date=` attribute may be used in conjunction with `min=` and `max=` attributes to set after and before limits.

The `datetime-local=` is local in the sense that a time zone cannot be specified.
The same goes for `time=`.

One difference between `number=` and `range=` is the latter should only be used when the exact value is unimportant.

</body>
</html>
