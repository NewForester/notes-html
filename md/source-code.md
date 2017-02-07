<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="../styles/style-sheet.css" />
</head>

<body>
# HTML5


## HTML Computer Code

HTML uses variable spaced fonts whereas computer code is generally displayed using fixed spaced fonts.


<hr /><!-- Computer Code -->

The `<code>` element may be used to present source code.

```html
    <code>
    unless (caller(0)) {
        run(@ARGV) or print_illumination();
        exit();
    }
    </code>
```

<p>will appear as:</p>
<div class=indent>
    <code>
    unless (caller(0)) {
        run(@ARGV) or print_illumination();
        exit();
    }
    </code>
</div>


<hr /><!-- Source Code -->

The `<code>` element does not preserve white space and line-breaks unless enclosed in the `<pre>` element.

```html
    <pre><code>
    unless (caller(0)) {
        run(@ARGV) or print_illumination();
        exit();
    }
    </code></pre>
```

<p>will appear as:</p>
<div class=noindent>
    <pre><code>
    unless (caller(0)) {
        run(@ARGV) or print_illumination();
        exit();
    }
    </code></pre>
</div>


<hr /><!-- Keyboard Board Input -->

The `<kbd>` element delimits keyboard input.

```html
    <p>Then convert with: <kbd>pandoc quotations.md > quotations.html</kbd></p>
```

<p>will appear as:</p>
<div class=indent>
    <p>Then convert with: <kbd>pandoc quotations.md > quotations.html</kbd></p>
</div>


<hr /><!-- Terminal Output -->

The `<samp>` element delimits sample output from a computer program.

```html
    <pre>
    <samp>
    [    0.000000] Initializing cgroup subsys cpuset
    [    0.000000] Initializing cgroup subsys cpu
    [    0.000000] Linux version 3.2.0-4-amd64 (debian-kernel@lists.debian.org) (gcc version 4.6.3 (Debian 4.6.3-14) ) #1 SMP Debian 3.2.84-1
    [    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-3.2.0-4-amd64 root=UUID=34203936-4c81-4ef9-a335-48b8e41653d2 ro quiet
    </samp>
    </pre>
```

<p>will appear as:</p>
<div class=noindent>
    <pre>
    <samp>
    [    0.000000] Initializing cgroup subsys cpuset
    [    0.000000] Initializing cgroup subsys cpu
    [    0.000000] Linux version 3.2.0-4-amd64 (debian-kernel@lists.debian.org) (gcc version 4.6.3 (Debian 4.6.3-14) ) #1 SMP Debian 3.2.84-1
    [    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-3.2.0-4-amd64 root=UUID=34203936-4c81-4ef9-a335-48b8e41653d2 ro quiet
    </samp>
    </pre>
</div>


<hr /><!-- Variables -->

The `<var>` element delimits a program variable or a mathematical expression.

```html
    <p>Euler's Equation: <var>e<sup>ix</sup> = cos x + i sin x</var></p>
```

<p>will appear as:</p>
<div class=indent>
    <p>Euler's Equation: <var>e<sup>ix</sup> = cos x + i sin x</var></p>
</div>

<hr />

</body>
</html>
