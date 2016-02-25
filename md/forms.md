<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Forms

The `<form>` element encloses a form used to collect user data.

The contents of a form are typically text and special, form specific, elements.
The most important of which is the `<input>` element.

There are a number of different `<input>` elements distinguished by the `type=` attribute.
The default is `type=text`.

Furthermore, `<input>` elements have other attributes that are `type=` specific to some degree.

HTML5 introduces a large number (compared with the previous standard) of new types and attributes.
Support for these among contemporary browsers is still incomplete.
An unsupported input type is treated as `type=text`.

Some of the new types imply the browser may validate input without script support.
Given the complexity of internationalisation, I suspect these are not as universal as might have been intended.


## Introduction

The `<form>` element encloses a form used to collect user input.
The form itself is not, by default, visible.

The `<input>` element is the most important of the form specific elements.
How the element is displayed depends on its `type=` attribute.

The `type=text` attribute defines a one line field for text input.
The default text field width is 20 characters.

Each input field should have a `name=` attribute.
If the `name=` attribute is omitted, any data entered into the field will not be submitted.

Each form needs at least one submit button that, when clicked, submits the data entered by the user to a form handler.

The form handler is (usually) specified using the `action=` attribute of the `<form>` element.
It is typically a server page with a script for processing input data.

```html
    <form action="action_page.php">
      First name:<br>
      <input type="text" name="firstname"><br>
      Last name:<br>
      <input type="text" name="lastname"><br>
      <br>
      <input type="submit" value="Go for it">
    </form>
```

<p>will appear as:</p>
<div class=indent>
    <form action="action_page.php">
      First name:<br>
      <input type="text" name="firstname"><br>
      Last name:<br>
      <input type="text" name="lastname"><br>
      <br>
      <input type="submit" value="Go for it">
    </form>
</div>

The default legend (`value=`) for the submit button is "Submit Query".


## HTML4 Form Attributes

For HTML4, the attributes for the `<form>` element are:

 1. accept            - file types for file upload (not supported in HTML5);
 1. accept-charset    - charset encoding of the submission;
 1. action            - where to submit the form data;
 1. enctype           - how to (MIME) encode data submitted using POST;
 1. method            - data submission with the HTTP GET or POST methods;
 1. name              - the name of the form;
 1. target            - where to display the response to a submission (_blank etc);


<!-- The Action Attribute -->

The `action=` attribute specifies where the form data is sent for processing when the form is submitted.
If omitted, the action is set to the current page (whatever than means).

<!-- The Method Attribute -->

The `method=` attribute specifies the HTTP method to be used to submit data.
The choices are:

  * get or
  * post

The default is `method="get"`.
However, when the form is submitted, the form data is visible in the page address field.
This method is only suitable for small amounts of data that are not sensitive.

Use `method="post"` for sensitive (personal, private, confidential) information.
It has no size limitations and so can be used for large amounts of data, including file upload.


## HTML5 Form Attributes

The `<form>` element attributes new with HTML5 are:

 1. autocomplete  - form auto-completion on or off;
 1. novalidate    - do not validate input before submission;

The `novalidate=` attribute specifies the form data should not be validated when submitted.
Not validated by whom ?  The browser ?  Scripts ?

The `autocomplete=` attribute specifies whether the browser can suggest completions based on values entered previously.
Typically, "on" for the form and "off" for sensitive fields.

The

 * action,
 * enctype,
 * method,
 * novalidate and
 * target

attributes can also be specified with the `<input type=submit>` where they override the form attribute.

</body>
</html>
