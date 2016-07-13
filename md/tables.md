<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: Tables</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="../styles/style-sheet.css" />
    <style>
        table, th, td {
            border: 1px solid black;
            border-collapse: collapse;
        }
    </style>
</head>

<body>

# HTML5

## HTML Tables

The `<table>` element defines a table.
The `<tr>` elements define table rows.

The `<th>` and `<td>` element defines the table headers and data (aka cells).
These last two are the data containers of the table may contain text, images, other tables and so on.

A table may have a `<caption>` element immediately after the `<table>` tag before the first `<tr>` tag:

```html
  <table style="width:100%">
    <caption>Monthly savings</caption>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
    <tr>
      <td>January</td>
      <td>£ 100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>£ 50</td>
    </tr>
  </table>
```

<p>will appear as:</p>
<div class=indent>
  <table style="width:100%">
    <caption>Monthly savings</caption>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
    <tr>
      <td>January</td>
      <td>£ 100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>£ 50</td>
    </tr>
  </table>
</div>


<hr /><!-- Table Borders -->

By default, the elements of a table have no borders.

Use the border property to define borders for both the table and the table cells.
This gives what appears to be a double border.

```html
    table, th, td {
        border: 1px solid black;
        border-collapse: collapse;
    }
```

Use the border-collapse property for a border between cells instead of a border around cells.

The border-spacing property specifies the distance between the double borders:

```html
    table {
        border-spacing: 5px;
    }
    th, td {
        padding: 15px;
    }
    th {
        text-align: left;
    }
```

Contrast spacing with the padding property which specifies the distance between the border and cell contents.

By default, the contents of `<td>` elements are left aligned but those of `<th>` elements are centred and bold.


<hr /><!-- Spanning -->

Individual cells may span columns:

```html
    <table style="width:100%">
      <tr>
        <th>Name</th>
        <th colspan="2">Extension:</th>
      </tr>
      <tr>
        <td>Peter Perfect</td>
        <td>77854</td>
        <td>77855</td>
      </tr>
    </table>
```

<p>will appear as:</p>
<div class=indent>
    <table style="width:100%">
      <tr>
        <th>Name</th>
        <th colspan="2">Extension:</th>
      </tr>
      <tr>
        <td>Peter Perfect</td>
        <td>77854</td>
        <td>77855</td>
      </tr>
    </table>
</div>

Individual cells may span rows:

```html
    <table style="width:100%">
      <tr>
        <th>Name:</th>
        <td>Peter Perfect</td>
      </tr>
      <tr>
        <th rowspan="2">Extension:</th>
        <td>77854</td>
      </tr>
      <tr>
        <td>77855</td>
      </tr>
    </table>
```

<p>will appear as:</p>
<div class=indent>
    <table style="width:100%">
      <tr>
        <th>Name:</th>
        <td>Peter Perfect</td>
      </tr>
      <tr>
        <th rowspan="2">Extension:</th>
        <td>77854</td>
      </tr>
      <tr>
        <td>77855</td>
      </tr>
    </table>
</div>


<hr /><!-- Styles of Individual Tables -->

To declare styles of an individual table, use the `id=` attribute on the `<table>` tag and define the styles thus:

```html
    table#t01 {
        width: 100%;
        background-color: #f1f1c1;
    }

    table#t01 th {
        color: white;
        background-color: black;
    }
```

Alternate rows may be given different properties thus:

```html
    table#t01 tr:nth-child(even) {
        background-color: #eee;
    }
    table#t01 tr:nth-child(odd) {
        background-color: #fff;
    }
```

<hr />

</body>
</html>
