<!DOCTYPE html>
<html lang="en-GB">
    <!-- notes-html by NewForester:  a series of notes on HTML5 written after studying the HTML Tutorial @ W3Schools -->

<head>
    <title>HTML5: File Paths</title>
    <meta charset="UTF-8" />
    <meta name="description" content="Notes on HTML5 made while following the HTML Tutorial @ W3Schools" />
    <meta name="keywords" content="HTML" />
    <meta name="author" content="NewForester" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="/styles/style-sheet.css" />
</head>

<body>

# HTML5

## HTML File Paths

An absolute file path is the full URL to an Internet file.

A relative file path references a file relative to the current page and is thus within the current web site.

Relative paths should be preferred.
They will lead to fewer problems should your web site change its web address.
It also facilitates local testing.

There are four types of relative file path:

  1. current directory    - `src="animage.png"`
  1. subdirectory         - `src="images/animage.png"`
  1. relative path        - `src="../images/animage.png"`
  1. site path            - `src="/images/animage.png"`

The subdirectory is a subdirectory of the current directory:
for a subdirectory of the site directory use a site path.

Beware:  site paths may not work too well when invoking local files (e.g. konqueror html/file-paths.html)
as the 'site' is not the current directory.

</hr>

</body>
</html>
