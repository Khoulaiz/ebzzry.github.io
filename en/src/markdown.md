My Markdown Style Guide
=======================

<center>April 3, 2017</center>
<center>Updated: April 5, 2017</center>

>“The laws that govern circumstances are abolished by new circumstances.”<br>
>―Napoleon Bonaparte

I like writing in Markdown—it’s readable, lightweight, and portable. It’s plain text so you won’t
need special applications to read or write with it. In this article, I’ll post my guidelines on how
I write Markdown files. I follow a certain set of rules so that my files look consistent with one
another, and so that GNU Emacs will be able to format it nicely.


Table of contents
-----------------

- [Headings](#headings)
- [Spacing](#spacing)
- [Code blocks](#codeblocks)
- [Bullets](#bullets)
- [Anchors](#anchors)
- [Line width](#linewidth)
- [Extras](#extras)
- [Closing remarks](#closing)


Headings <a name="headings"></a>
--------------------------------


### Level 1 <a name="level1"></a>

Level 1 headings are ideal when used as Document titles. They should be used only once in and they
must be in the first line of a file. It should describe what the file or document is all about. I
use the `=` (equals) symbol to indicate the level 1 heading, instead of the `#` symbol. Using the
`=` symbol makes it easy to spot the heading, and it distinguishes it from the other markers. I use
it this way:

```markdown
How to Fly Like a Lobster
=========================
```

instead of

```markdown
# How to Fly Like a Lobster
```


### Level 2 <a name="level2"></a>

Level 2 headings indicate the top-level sections of a document. They are the primary dividers in a
file. Similar to the level 1 heading, I use the `-` (hyphen) symbol to mark the heading. I use it
this way:

```markdown
Preparing Your Pincers
----------------------
```

instead of

```markdown
## Preparing Your Pincers
```


### Lower levels <a name="lowerlevels"></a>

For level 3 and lower headings, I use the `#` with the appropriate number of repetitions to indicate
the level.

Level 3:

```markdown
### Fuel
```

Level 4:

```markdown
#### Organic
```

And, so on.



Spacing <a name="spacing"></a>
------------------------------

The space between document elements should be consistent to facilitate readability. After a heading,
create a blank line:

```markdown
Yeah, yeah, yeah
================

Some text here
```

When starting a new level, create two blank lines before it:

```markdown
Yeah, yeah, yeah
================

Some text here


Preparing Your Pincers
----------------------

Meh
```

Another good reason for having a blank space after every heading is to make it easy for text editors
like GNU Emacs to to format the text. The keyboard shortcut <kbd>M-q</kbd> bound by default to
`fill-paragraph`, reformats a text block so that the maximum line width is filled correctly. The
command `fill-paragraph` uses the `fill-column` variable–bound by default to 70—to reformat a text
body.

So, if you have the text:

```markdown
Preparing Your Pincers
----------------------

Meh meh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh meh
```

And you press <kbd>M-q</kbd> while point (cursor) is somewhere in the last line, it becomes:

```markdown
Preparing Your Pincers
----------------------

Meh meh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh
mehmeh meh mehmeh meh mehmeh meh meh
```


Code blocks <a name="codeblocks"></a>
-------------------------------------

When the code or command block occupies one to two lines, indent it with four spaces:

```bash
    VAR=blahblahblah
    function meh () { echo meh }
```

If there are three or more lines, use a pair of three backticks (```) to delimit the start and end
of a code block:

    ˋˋˋ
    $ mkdir foo
    $ echo foo > foo/foo
    $ rm -rf foo
    $ date
    ˋˋˋ 

Bullets <a name="bullets"></a>
------------------------------

When making lists, I like to use the `-` hyphen charactr to indicate the first level. I use the `+`
(plus) character to indicate the second level. Then for level 3 and lower, I use `*` (asterisk).

The `-` symbol is easier to type on a keyboard than `*`. Also, unlike `+` it doesn’t require to
press <kbd>Shift</kbd> on standard keyboards. Compared to `*`, the hyphen has a more consistent
glyph across different typefaces.

For example:

```markdown
- lobsters
  + pincers
  + thorax
- crabs
  + pincers
    * laser cannon
    * chainsaw
      * detachable
- unicorns
```


Anchors <a name="anchors"></a>
------------------------------

When the target document format of your Markdown files is HTML, it is a good habit to label your
sections properly. For example, this section is written as:

```markdown
Anchors <a name="anchors"></a>
------------------------------

```

This makes it easy later on to create a table of contents, like so:

```markdown
Table of contents
-----------------

- [Anchors](#anchors)
```


Line width <a name="linewidth"></a>
-----------------------------------

In the old days, it’s good to wrap your lines at the 70 character line width. Nowadays, a higher
limit—made possible by modern graphics system—is more desirable so that we can pack more information
in one line.

70 characters:

```
Meh meh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh
mehmeh meh mehmeh meh meh meh meh mehmeh meh mehmeh meh mehmeh meh meh
```

100 characters:

```
Meh meh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh mehmeh meh meh meh meh
mehmeh meh mehmeh meh mehmeh meh meh
```


Extras <a name="extras"></a>
----------------------------

When using GNU Emacs, I use [these](https://gist.github.com/0c8fb40ac8db1463a933cfc19f219431)
commands, bound to <kbd>M-g =</kbd>, <kbd>M-g -</kbd>, and <kbd>M-g `</kbd>, respectively, to make
it easy for me to insert the delimiters. For example, if I have the following text, where ^ is point
(cursor):

```markdown
What is it Like Out There?

^
```

then, I press <kbd>M-g =</kbd>, it will become:

```markdown
What is it Like Out There?
==========================
                         ^
```

The same apply with level 2 headings. So if I have:

```markdown
Monsters and angels

^
```

then, I press <kbd>M-g -</kbd>, it will become:

```markdown
Monsters and angels
-------------------
                  ^
```


Closing remarks <a name="closing"></a>
--------------------------------------

By following these simple guidelines, I create consistency among my Markdown source files. These
guidelines serve as my template when creating new documents or modifying existing ones. If you have
suggestions and criticisms, send in your pull requests!