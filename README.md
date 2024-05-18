# Project-Template
Github boilerplate files, such as ReadMe and gitignore.

# What to include?
gitignore, license, readme.md, 

# License
While I like the idea of requiring the ability to incorporate improvements from your version of my code as part of the deal of being allowed to use my code,
which I believe to be the main benefit of GPL, the nature of MIT may increase the chances of a potential contributor even looking at a project in the first place.
Using any GPL code forces a project to become GPL compliant, which might cause a change to the default license of this project.

# Coding Conventions
Use language specific style guides, generally.
Tabs over spaces (the whole point of tab is to indent a section of text), unless that would interfere with a language's own requirements.
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

# Setext headings
A setext heading consists of one or more lines of text, each containing at least one non-whitespace character, with no more than 3 spaces indentation, followed by a setext heading underline. The lines of text must be such that, were they not followed by the setext heading underline, they would be interpreted as a paragraph: they cannot be interpretable as a code fence, ATX heading, block quote, thematic break, list item, or HTML block.

A setext heading underline is a sequence of = characters or a sequence of - characters, with no more than 3 spaces indentation and any number of trailing spaces. If a line containing a single - can be interpreted as an empty list items, it should be interpreted this way and not as a setext heading underline.

The heading is a level 1 heading if = characters are used in the setext heading underline, and a level 2 heading if - characters are used. The contents of the heading are the result of parsing the preceding lines of text as CommonMark inline content.

In general, a setext heading need not be preceded or followed by a blank line. However, it cannot interrupt a paragraph, so when a setext heading comes after a paragraph, a blank line is needed between them.

Simple examples:

Example 50
Foo *bar*
=========

Foo *bar*
---------
 
<h1>Foo <em>bar</em></h1>
<h2>Foo <em>bar</em></h2>
The content of the header may span more than one line:

Example 51
Foo *bar
baz*
====
 
<h1>Foo <em>bar
baz</em></h1>

# Indented code blocks
An indented code block is composed of one or more indented chunks separated by blank lines. An indented chunk is a sequence of non-blank lines, each indented four or more spaces. The contents of the code block are the literal contents of the lines, including trailing line endings, minus four spaces of indentation. An indented code block has no info string.

An indented code block cannot interrupt a paragraph, so there must be a blank line between a paragraph and a following indented code block. (A blank line is not needed, however, between a code block and a following paragraph.)

Example 77
    a simple
      indented code block
 
<pre><code>a simple
  indented code block
</code></pre>

# Fenced code blocks
A code fence is a sequence of at least three consecutive backtick characters (`) or tildes (~). (Tildes and backticks cannot be mixed.) A fenced code block begins with a code fence, indented no more than three spaces.

The line with the opening code fence may optionally contain some text following the code fence; this is trimmed of leading and trailing whitespace and called the info string. If the info string comes after a backtick fence, it may not contain any backtick characters. (The reason for this restriction is that otherwise some inline code would be incorrectly interpreted as the beginning of a fenced code block.)

Backticks:

```
<
 >
```
 
<pre><code>&lt;
 &gt;
</code></pre>

Tildes:

~~~
<
 >
~~~
 
<pre><code>&lt;
 &gt;
</code></pre>

# HTML blocks
An HTML block is a group of lines that is treated as raw HTML (and will not be escaped in HTML output).

There are seven kinds of HTML block, which can be defined by their start and end conditions. The block begins with a line that meets a start condition (after up to three spaces optional indentation). It ends with the first subsequent line that meets a matching end condition, or the last line of the document, or the last line of the container block containing the current HTML block, if no line is encountered that meets the end condition. If the first line meets both the start condition and the end condition, the block will contain just that line.

Start condition: line begins with the string <script, <pre, or <style (case-insensitive), followed by whitespace, the string >, or the end of the line.
End condition: line contains an end tag </script>, </pre>, or </style> (case-insensitive; it need not match the start tag).

Start condition: line begins with the string <!--.
End condition: line contains the string -->.

Start condition: line begins with the string <?.
End condition: line contains the string ?>.

Start condition: line begins with the string <! followed by an uppercase ASCII letter.
End condition: line contains the character >.

Start condition: line begins with the string <![CDATA[.
End condition: line contains the string ]]>.

Start condition: line begins the string < or </ followed by one of the strings (case-insensitive) address, article, aside, base, basefont, blockquote, body, caption, center, col, colgroup, dd, details, dialog, dir, div, dl, dt, fieldset, figcaption, figure, footer, form, frame, frameset, h1, h2, h3, h4, h5, h6, head, header, hr, html, iframe, legend, li, link, main, menu, menuitem, nav, noframes, ol, optgroup, option, p, param, section, source, summary, table, tbody, td, tfoot, th, thead, title, tr, track, ul, followed by whitespace, the end of the line, the string >, or the string />.
End condition: line is followed by a blank line.

Start condition: line begins with a complete open tag (with any tag name other than script, style, or pre) or a complete closing tag, followed only by whitespace or the end of the line.
End condition: line is followed by a blank line.

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

Example 198
| foo | bar |
| --- | --- |
| baz | bim |
 
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

The header row must match the delimiter row in the number of cells. If not, a table will not be recognized:

Example 203
| abc | def |
| --- |
| bar |
 
<p>| abc | def |
| --- |
| bar |</p>
The remainder of the table’s rows may vary in the number of cells. If there are a number of cells fewer than the number of cells in the header row, empty cells are inserted. If there are greater, the excess is ignored:

Example 204
| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |
 
<table>
<thead>
<tr>
<th>abc</th>
<th>def</th>
</tr>
</thead>
<tbody>
<tr>
<td>bar</td>
<td></td>
</tr>
<tr>
<td>bar</td>
<td>baz</td>
</tr>
</tbody>
</table>

# Block quotes
A block quote marker consists of 0-3 spaces of initial indent, plus (a) the character > together with a following space, or (b) a single character > not followed by a space.

Example
> # Foo
> bar
> baz
 
<blockquote>
<h1>Foo</h1>
<p>bar
baz</p>
</blockquote>

The spaces after the > characters can be omitted

# List items
A list marker is a bullet list marker or an ordered list marker.

A bullet list marker is a -, +, or * character.

An ordered list marker is a sequence of 1–9 arabic digits (0-9), followed by either a . character or a ) character. (The reason for the length limit is that with 10 digits we start seeing integer overflows in some browsers.)

The following rules define list items:

Basic case. If a sequence of lines Ls constitute a sequence of blocks Bs starting with a non-whitespace character, and M is a list marker of width W followed by 1 ≤ N ≤ 4 spaces, then the result of prepending M and the following spaces to the first line of Ls, and indenting subsequent lines of Ls by W + N spaces, is a list item with Bs as its contents. The type of the list item (bullet or ordered) is determined by the type of its list marker. If the list item is ordered, then it is also assigned a start number, based on the ordered list marker.

Exceptions:

When the first list item in a list interrupts a paragraph—that is, when it starts on a line that would otherwise count as paragraph continuation text—then (a) the lines Ls must not begin with a blank line, and (b) if the list item is ordered, the start number must be 1.
If any line is a thematic break then that line is not a list item.
For example, let Ls be the lines

Example 231
A paragraph
with two lines.

    indented code

> A block quote.
 
<p>A paragraph
with two lines.</p>
<pre><code>indented code
</code></pre>
<blockquote>
<p>A block quote.</p>
</blockquote>
And let M be the marker 1., and N = 2. Then rule #1 says that the following is an ordered list item with start number 1, and the same contents as Ls:

Example 232
1.  A paragraph
    with two lines.

        indented code

    > A block quote.
 
<ol>
<li>
<p>A paragraph
with two lines.</p>
<pre><code>indented code
</code></pre>
<blockquote>
<p>A block quote.</p>
</blockquote>
</li>
</ol>

# Task list items (extension)
GFM enables the tasklist extension, where an additional processing step is performed on list items.

A task list item is a list item where the first block in it is a paragraph which begins with a task list item marker and at least one whitespace character before any other content.

A task list item marker consists of an optional number of spaces, a left bracket ([), either a whitespace character or the letter x in either lowercase or uppercase, and then a right bracket (]).

When rendered, the task list item marker is replaced with a semantic checkbox element; in an HTML output, this would be an <input type="checkbox"> element.

If the character between the brackets is a whitespace character, the checkbox is unchecked. Otherwise, the checkbox is checked.

This spec does not define how the checkbox elements are interacted with: in practice, implementors are free to render the checkboxes as disabled or inmutable elements, or they may dynamically handle dynamic interactions (i.e. checking, unchecking) in the final rendered document.

Example 279
- [ ] foo
- [x] bar
 
<ul>
<li><input disabled="" type="checkbox"> foo</li>
<li><input checked="" disabled="" type="checkbox"> bar</li>
</ul>
Task lists can be arbitrarily nested:

Example 280
- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim
 
<ul>
<li><input checked="" disabled="" type="checkbox"> foo
<ul>
<li><input disabled="" type="checkbox"> bar</li>
<li><input checked="" disabled="" type="checkbox"> baz</li>
</ul>
</li>
<li><input disabled="" type="checkbox"> bim</li>
</ul>

# Lists
A list is a sequence of one or more list items of the same type. The list items may be separated by any number of blank lines.

Two list items are of the same type if they begin with a list marker of the same type. Two list markers are of the same type if (a) they are bullet list markers using the same character (-, +, or *) or (b) they are ordered list numbers with the same delimiter (either . or )).

A list is an ordered list if its constituent list items begin with ordered list markers, and a bullet list if its constituent list items begin with bullet list markers.

The start number of an ordered list is determined by the list number of its initial list item. The numbers of subsequent list items are disregarded.

A list is loose if any of its constituent list items are separated by blank lines, or if any of its constituent list items directly contain two block-level elements with a blank line between them. Otherwise a list is tight. (The difference in HTML output is that paragraphs in a loose list are wrapped in <p> tags, while paragraphs in a tight list are not.)

Changing the bullet or ordered list delimiter starts a new list:

Example 281
- foo
- bar
+ baz
 
<ul>
<li>foo</li>
<li>bar</li>
</ul>
<ul>
<li>baz</li>
</ul>
Example 282
1. foo
2. bar
3) baz
 
<ol>
<li>foo</li>
<li>bar</li>
</ol>
<ol start="3">
<li>baz</li>
</ol>

# Backslash escapes
Any ASCII punctuation character may be backslash-escaped:

Example 308
\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\`\{\|\}\~
 
<p>!&quot;#$%&amp;'()*+,-./:;&lt;=&gt;?@[\]^_`{|}~</p>
Backslashes before other characters are treated as literal backslashes:

Example 309
\→\A\a\ \3\φ\«
 
<p>\→\A\a\ \3\φ\«</p>
Escaped characters are treated as regular characters and do not have their usual Markdown meanings:

Example 310
\*not emphasized*
\<br/> not a tag
\[not a link](/foo)
\`not code`
1\. not a list
\* not a list
\# not a heading
\[foo]: /url "not a reference"
\&ouml; not a character entity
 
<p>*not emphasized*
&lt;br/&gt; not a tag
[not a link](/foo)
`not code`
1. not a list
* not a list
# not a heading
[foo]: /url &quot;not a reference&quot;
&amp;ouml; not a character entity</p>
If a backslash is itself escaped, the following character is not:

Example 311
\\*emphasis*
 
<p>\<em>emphasis</em></p>

# Emphasis
*foo bar*
 
<p><em>foo bar</em></p>

***strong emph***
***strong** in emph*
***emph* in strong**
**in strong *emph***
*in emph **strong***

# Strikethrough (extension)
GFM enables the strikethrough extension, where an additional emphasis type is available.

Strikethrough text is any text wrapped in a matching pair of one or two tildes (~).

Example 491
~~Hi~~ Hello, ~there~ world!
 
<p><del>Hi</del> Hello, <del>there</del> world!</p>
As with regular emphasis delimiters, a new paragraph will cause strikethrough parsing to cease:

Example 492
This ~~has a

new paragraph~~.
 
<p>This ~~has a</p>
<p>new paragraph~~.</p>

# Links
A link contains link text (the visible text), a link destination (the URI that is the link destination), and optionally a link title. There are two basic kinds of links in Markdown. In inline links the destination and title are given immediately after the link text. In reference links the destination and title are defined elsewhere in the document.

A link text consists of a sequence of zero or more inline elements enclosed by square brackets ([ and ]). The following rules apply:

Links may not contain other links, at any level of nesting. If multiple otherwise valid link definitions appear nested inside each other, the inner-most definition is used.

Brackets are allowed in the link text only if (a) they are backslash-escaped or (b) they appear as a matched pair of brackets, with an open bracket [, a sequence of zero or more inlines, and a close bracket ].

Backtick code spans, autolinks, and raw HTML tags bind more tightly than the brackets in link text. Thus, for example, [foo`]` could not be a link text, since the second ] is part of a code span.

The brackets in link text bind more tightly than markers for emphasis and strong emphasis. Thus, for example, *[foo*](url) is a link.

A link destination consists of either

a sequence of zero or more characters between an opening < and a closing > that contains no line breaks or unescaped < or > characters, or

a nonempty sequence of characters that does not start with <, does not include ASCII space or control characters, and includes parentheses only if (a) they are backslash-escaped or (b) they are part of a balanced pair of unescaped parentheses. (Implementations may impose limits on parentheses nesting to avoid performance issues, but at least three levels of nesting should be supported.)

A link title consists of either

a sequence of zero or more characters between straight double-quote characters ("), including a " character only if it is backslash-escaped, or

a sequence of zero or more characters between straight single-quote characters ('), including a ' character only if it is backslash-escaped, or

a sequence of zero or more characters between matching parentheses ((...)), including a ( or ) character only if it is backslash-escaped.

Although link titles may span multiple lines, they may not contain a blank line.

An inline link consists of a link text followed immediately by a left parenthesis (, optional whitespace, an optional link destination, an optional link title separated from the link destination by whitespace, optional whitespace, and a right parenthesis ). The link’s text consists of the inlines contained in the link text (excluding the enclosing square brackets). The link’s URI consists of the link destination, excluding enclosing <...> if present, with backslash-escapes in effect as described above. The link’s title consists of the link title, excluding its enclosing delimiters, with backslash-escapes in effect as described above.

Here is a simple inline link:

Example 494
[link](/uri "title")
 
<p><a href="/uri" title="title">link</a></p>

Autolinks
Autolinks are absolute URIs and email addresses inside < and >. They are parsed as links, with the URL or email address as the link label.

A URI autolink consists of <, followed by an absolute URI followed by >. It is parsed as a link to the URI, with the URI as the link’s label.

An absolute URI, for these purposes, consists of a scheme followed by a colon (:) followed by zero or more characters other than ASCII whitespace and control characters, <, and >. If the URI includes these characters, they must be percent-encoded (e.g. %20 for a space).

For purposes of this spec, a scheme is any sequence of 2–32 characters beginning with an ASCII letter and followed by any combination of ASCII letters, digits, or the symbols plus (“+”), period (“.”), or hyphen (“-”).

Here are some valid autolinks:

Example 603
<http://foo.bar.baz>
 
<p><a href="http://foo.bar.baz">http://foo.bar.baz</a></p>
Example 604
<http://foo.bar.baz/test?q=hello&id=22&boolean>
 
<p><a href="http://foo.bar.baz/test?q=hello&amp;id=22&amp;boolean">http://foo.bar.baz/test?q=hello&amp;id=22&amp;boolean</a></p>
Example 605
<irc://foo.bar:2233/baz>
 
<p><a href="irc://foo.bar:2233/baz">irc://foo.bar:2233/baz</a></p>

# Hard line breaks
A line break (not in a code span or HTML tag) that is preceded by two or more spaces and does not occur at the end of a block is parsed as a hard line break (rendered in HTML as a <br /> tag):

Example 658
foo  
baz
 
<p>foo<br />
baz</p>
For a more visible alternative, a backslash before the line ending may be used instead of two spaces:

Example 659
foo\
baz
 
<p>foo<br />
baz</p>
More than two spaces can be used:

Example 660
foo       
baz
 
<p>foo<br />
baz</p>
Leading spaces at the beginning of the next line are ignored:

Example 661
foo  
     bar
 
<p>foo<br />
bar</p>
Example 662
foo\
     bar
 
<p>foo<br />
bar</p>
Line breaks can occur inside emphasis, links, and other constructs that allow inline content:

Example 663
*foo  
bar*
 
<p><em>foo<br />
bar</em></p>
Example 664
*foo\
bar*
 
<p><em>foo<br />
bar</em></p>
Line breaks do not occur inside code spans

Example 665
`code  
span`
 
<p><code>code   span</code></p>
Example 666
`code\
span`
 
<p><code>code\ span</code></p>
or HTML tags:

Example 667
<a href="foo  
bar">
 
<p><a href="foo  
bar"></p>
Example 668
<a href="foo\
bar">
 
<p><a href="foo\
bar"></p>
Hard line breaks are for separating inline content within a block. Neither syntax for hard line breaks works at the end of a paragraph or other block element:

Example 669
foo\
 
<p>foo\</p>
Example 670
foo  
 
<p>foo</p>
Example 671
### foo\
 
<h3>foo\</h3>
Example 672
### foo  
 
<h3>foo</h3>
6.13Soft line breaks
A regular line break (not in a code span or HTML tag) that is not preceded by two or more spaces or a backslash is parsed as a softbreak. (A softbreak may be rendered in HTML either as a line ending or as a space. The result will be the same in browsers. In the examples here, a line ending will be used.)

Example 673
foo
baz
 
<p>foo
baz</p>
Spaces at the end of the line and beginning of the next line are removed:

Example 674
foo 
 baz
 
<p>foo
baz</p>
A conforming parser may render a soft line break in HTML either as a line break or as a space.

A renderer may also provide an option to render soft line breaks as hard line breaks.
