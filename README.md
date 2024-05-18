# Project-Template
Github boilerplate files.

# What to include?
| Type | | Name |
| --- | --- | --- |
| Ignore | | .gitignore |
| License | | LICENSE |
| Read Me| | README.md |

# License
While I like the idea of requiring the ability to incorporate improvements
from your version of my code as part of the deal of being allowed to use my code,
which I believe to be the main benefit of GPL,
the nature of MIT may increase the chances of a potential contributor
even looking at a project in the first place.

Using any GPL code forces a project to become GPL compliant,
which might cause a change to the default license of this project.

# Coding Conventions
Use language specific style guides, generally.  
Tabs over spaces (the whole point of tab is to indent a section of text),
unless that would interfere with a language's own requirements.  
Need style guids for python, C#, godot, R, javascript.

As a beginner, many of my projects will include comment blocks at the bottom of files containing examples and explanations of functions and syntax.  
I need to come up with a tool to automatically strip these sections from production code, for copyright issues if nothing else.  
While not all markdown styles require blank lines between all element types, it helps keep things organized.  

# Github flavored markdown
Need a readme template that includes common examples.
Heading, coloring?, tables, lists, code blocks, links.

# Design Doc
Most of my projects include a text file containing an ideas dump.

# Thematic breaks
A line consisting of 0-3 spaces of indentation, followed by a sequence of three or more matching -, _, or * characters, each followed optionally by any number of spaces or tabs, forms a thematic break.

Example
***
<hr />
---
<hr />
___
<hr />

# Simple headings
A space after the hash mark is required.

Example
# one
## two
### three
#### four
##### five
###### six
 
<h1>one</h1>
<h2>two</h2>
<h3>three</h3>
<h4>four</h4>
<h5>five</h5>
<h6>six</h6>

# Indented code blocks

Example

    a simple
      indented code block
 
# Fenced code blocks

Backticks:

```
< Fenced Code Block using backticks. >
```

Tildes:

~~~
< Fenced Code Block using tildes. >
~~~

# HTML blocks
There are seven kinds of HTML block, which can be defined by their start and end conditions. The block begins with a line that meets a start condition (after up to three spaces optional indentation). It ends with the first subsequent line that meets a matching end condition, or the last line of the document, or the last line of the container block containing the current HTML block, if no line is encountered that meets the end condition. If the first line meets both the start condition and the end condition, the block will contain just that line.

## Script, Pre, or style

```
<script> </script>
<pre> </pre>
<style> </style>
```

## Bang and Question
For comments and PHP.

```
<!-- Comment goes here. -->
<? PHP ?>
```

## CDATA
Basically comment mode for markup

```
<![CDATA[ XML goes here ]]>
```

## I dont know

```
<!Any uppercase ASCII letter>
```

## A bunch of tags

```
Start condition: line begins the string < or </ followed by one of the strings (case-insensitive) address, article, aside, base, basefont, blockquote, body, caption, center, col, colgroup, dd, details, dialog, dir, div, dl, dt, fieldset, figcaption, figure, footer, form, frame, frameset, h1, h2, h3, h4, h5, h6, head, header, hr, html, iframe, legend, li, link, main, menu, menuitem, nav, noframes, ol, optgroup, option, p, param, section, source, summary, table, tbody, td, tfoot, th, thead, title, tr, track, ul, followed by whitespace, the end of the line, the string >, or the string />.
End condition: line is followed by a blank line.
```

## Singletons

```
Start condition: line begins with a complete open tag (with any tag name other than script, style, or pre) or a complete closing tag, followed only by whitespace or the end of the line.
End condition: line is followed by a blank line.
```

# Link reference definitions
A link reference definition consists of a link label, indented up to three spaces, followed by a colon (:), optional whitespace (including up to one line ending), a link destination, optional whitespace (including up to one line ending), and an optional link title, which if it is present must be separated from the link destination by whitespace. No further non-whitespace characters may occur on the line.

A link reference definition does not correspond to a structural element of a document. Instead, it defines a label which can be used in reference links and reference-style images elsewhere in the document. Link reference definitions can come either before or after the links that use them.

Example 161
[foo]: /url "title"

[foo]
 
<p><a href="/url" title="title">foo</a></p>
Example 162
   [foo]: 
      /url  
           'the title'  

[foo]
 
<p><a href="/url" title="the title">foo</a></p>
Example 163
[Foo*bar\]]:my_(url) 'title (with parens)'

[Foo*bar\]]
 
<p><a href="my_(url)" title="title (with parens)">Foo*bar]</a></p>
Example 164
[Foo bar]:
<my url>
'title'

[Foo bar]
 
<p><a href="my%20url" title="title">Foo bar</a></p>

# Tables (extension)
GFM enables the table extension, where an additional leaf block type is available.

A table is an arrangement of data with rows and columns, consisting of a single header row, a delimiter row separating the header from the data, and zero or more data rows.

Each row consists of cells containing arbitrary text, in which inlines are parsed, separated by pipes (|). A leading and trailing pipe is also recommended for clarity of reading, and if there’s otherwise parsing ambiguity. Spaces between pipes and cell content are trimmed. Block-level elements cannot be inserted in a table.

The delimiter row consists of cells whose only content are hyphens (-), and optionally, a leading or trailing colon (:), or both, to indicate left, right, or center alignment respectively.

```
Markdown: 
| foo | bar |
| --- | --- |
| baz | bim |

HTML:
<table>
<thead>
<tr>
<th>foo</th>
<th>bar</th>
</tr>
</thead>
<tbody>
<tr>
<td>baz</td>
<td>bim</td>
</tr>
</tbody>
</table>
```

## Markdown

| foo | bar |
| --- | --- |
| baz | bim |

## HTML

<table>
<thead>
<tr>
<th>foo</th>
<th>bar</th>
</tr>
</thead>
<tbody>
<tr>
<td>baz</td>
<td>bim</td>
</tr>
</tbody>
</table>

# Block quotes

```
> Can include the space.
>No space is okay, but is it really?
```

> Can include the space.
>No space is okay, but is it really?

# Lists

A couple different types of lists.

## Bullet List

```
A bullet list marker is a -, +, or * character.

* Bulletted List
* Second Thing
* Third Thing
```

* Bulletted List
* Second Thing
* Third Thing

## Ordered List

```
An ordered list marker is a sequence of 1–9 arabic digits (0-9),
followed by either a . character or a ) character.
(The reason for the length limit is that with 10 digits we start seeing integer overflows in some browsers.)

1. First Item
2. Second Item
3. Thing Three
```

1. First Item
2. Second Item
3. Thing Three

# Task list items (extension)
GFM enables the tasklist extension, where an additional processing step is performed on list items.

A task list item is a list item where the first block in it is a paragraph which begins with a task list item marker and at least one whitespace character before any other content.

A task list item marker consists of an optional number of spaces, a left bracket ([), either a whitespace character or the letter x in either lowercase or uppercase, and then a right bracket (]).

When rendered, the task list item marker is replaced with a semantic checkbox element; in an HTML output, this would be an <input type="checkbox"> element.

If the character between the brackets is a whitespace character, the checkbox is unchecked. Otherwise, the checkbox is checked.

This spec does not define how the checkbox elements are interacted with: in practice, implementors are free to render the checkboxes as disabled or inmutable elements, or they may dynamically handle dynamic interactions (i.e. checking, unchecking) in the final rendered document.

```
- [ ] foo
- [x] bar
```

- [ ] foo
- [x] bar

Task lists can be arbitrarily nested:

```
- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim
```

- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim

# Backslash escapes
Any ASCII punctuation character may be backslash-escaped:

```
\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\`\{\|\}\~
```

\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\`\{\|\}\~

Backslashes before other characters are treated as literal backslashes:

```
\→\A\a\ \3\φ\«
```

\→\A\a\ \3\φ\«

Escaped characters are treated as regular characters and do not have their usual Markdown meanings:

```
\*not emphasized*
\<br/> not a tag
\[not a link](/foo)
\`not code`
1\. not a list
\* not a list
\# not a heading
\[foo]: /url "not a reference"
\&ouml; not a character entity

\\*emphasis*
```

\*not emphasized*
\<br/> not a tag
\[not a link](/foo)
\`not code`
1\. not a list
\* not a list
\# not a heading
\[foo]: /url "not a reference"
\&ouml; not a character entity

\\*emphasis*

# Emphasis

```
*foo bar*
 
***strong emph***
***strong** in emph*
***emph* in strong**
**in strong *emph***
*in emph **strong***
```

*foo bar*
 
***strong emph***
***strong** in emph*
***emph* in strong**
**in strong *emph***
*in emph **strong***

# Strikethrough (extension)
GFM enables the strikethrough extension, where an additional emphasis type is available.

Strikethrough text is any text wrapped in a matching pair of one or two tildes (~).

```
~~Hi~~ Hello, ~there~ world!
```

~~Hi~~ Hello, ~there~ world!

As with regular emphasis delimiters, a new paragraph will cause strikethrough parsing to cease:

```
This ~~has a

new paragraph~~.
```

This ~~has a

new paragraph~~.

# Links

```
[link](/uri "title")
```

[link](/uri "title")

## Autolinks
Autolinks are absolute URIs and email addresses inside < and >. They are parsed as links, with the URL or email address as the link label.

A URI autolink consists of <, followed by an absolute URI followed by >. It is parsed as a link to the URI, with the URI as the link’s label.

An absolute URI, for these purposes, consists of a scheme followed by a colon (:) followed by zero or more characters other than ASCII whitespace and control characters, <, and >. If the URI includes these characters, they must be percent-encoded (e.g. %20 for a space).

For purposes of this spec, a scheme is any sequence of 2–32 characters beginning with an ASCII letter and followed by any combination of ASCII letters, digits, or the symbols plus (“+”), period (“.”), or hyphen (“-”).

Here are some valid autolinks:

```
<http://foo.bar.baz>
<http://foo.bar.baz/test?q=hello&id=22&boolean>
<irc://foo.bar:2233/baz>
```

<http://foo.bar.baz>
<http://foo.bar.baz/test?q=hello&id=22&boolean>
<irc://foo.bar:2233/baz>

# Hard line breaks
A line break (not in a code span or HTML tag) that is preceded by two or more spaces and does not occur at the end of a block is parsed as a hard line break (rendered in HTML as a <br /> tag):

```
foo  
baz
```

foo  
baz

For a more visible alternative, a backslash before the line ending may be used instead of two spaces:

```
foo\
baz
```

foo\
baz

More than two spaces can be used:

```
foo       
baz
```

foo       
baz

Leading spaces at the beginning of the next line are ignored:

```
foo  
     bar
```

foo  
     bar
 
```
foo\
     bar
```

foo\
     bar

Line breaks can occur inside emphasis, links, and other constructs that allow inline content:

```
*foo  
bar*
```

*foo  
bar*

```
*foo\
bar*
```

*foo\
bar*

# Soft line breaks
A regular line break (not in a code span or HTML tag) that is not preceded by two or more spaces or a backslash is parsed as a softbreak. (A softbreak may be rendered in HTML either as a line ending or as a space. The result will be the same in browsers. In the examples here, a line ending will be used.)

```
foo
baz
```

foo
baz
 
Spaces at the end of the line and beginning of the next line are removed:

```
foo 
 baz
```

foo 
 baz
 
A conforming parser may render a soft line break in HTML either as a line break or as a space.

A renderer may also provide an option to render soft line breaks as hard line breaks.

# Color
<span style="color:blue">some *blue* text</span>.
