# Markdown and HTML on Tutti

Tutti can parse both Markdown and HTML to produce the web pages that appear on the Tutti site. But to get the best, most reliable results for your documentation, it's important to know the most "Tutti-friendly" practices.

## HTML in Tutti Source Files

HTML is recommended over Markdown, because HTML is standardized, while Markdown is not. HTML is also a far more powerful markup language than Markdown, allowing you to do more with your content.

If you use HTML in your Tutti source files, do not use tags or techniques that are deprecated in [HTML5](https://www.w3.org/html/).

HTML source files do not require &lt;html&gt;, &lt;head&gt;, or &lt;body&gt; tags. The Tutti parser creates valid and well-formed HTML5 pages from source files beginning with an &lt;h1&gt; tag.

## Markdown in Tutti Source Files

In Markdown, there are several different ways to specify the same style, such as headings, italics, or bulleted lists. It is not a standardized markup language.

Tutti uses the same Markdown parser as BBGitHub. While most Markdown techniques render acceptably on Tutti (and should match the rendering on BBGitHub), the examples on this page illustrate the recommended practices.

If you encounter specific problems with the Markdown you're using in your documentation and you can't find a solution on this page, [open a DRQS ticket to group 190](https://blinks.bloomberg.com/screens/DRQS%20A%20/GR%20190) that describes your issue, with a specific example.

To see exactly how everything was done on this page, click *View Source* at the top of this page to access the source file in BBGitHub, then click the *Edit* (pencil) icon to view the Markdown.

## Combining Markdown and HTML

You can use both Markdown and HTML in the same documentation source file.

For example, the following code block works on Tutti, as seen below the code block:

```
This line uses the Markdown for **bold**.

This next line uses HTML for a <s>strikethrough</s>.
```

This line uses the Markdown for **bold**.

This next line uses HTML for a <s>strikethrough</s>.

You can use HTML tags within Markdown elements. For example, the following works on Tutti:

```
This is a Markdown bullet list containing HTML tags:

* This first item has <b>bold</b> text
* This second item has <i>italicized</i> text.
```

This is a Markdown bullet list containing HTML tags:

* This first item has <b>bold</b> text
* This second item has <i>italicized</i> text.

Do not use Markdown within an HTML element. For example, the following will **not** work on Tutti, as seen below the code block:

```
<ul>
  <li>The asterisks in this item will **not** render the word in bold.</li>
  <li>The asterisks in this item will *not* render the word in italics.</li>
</ul>
```

<ul>
  <li>The asterisks in this item will **not** render the word in bold.</li>
  <li>The asterisks in this item will *not* render the word in italics.</li>
</ul>

The rest of this page describes the best way to implement each of the various elements and styles you may need in your documentation.

## Heading 2

```
## Heading 2
```

### Heading 3

```
### Heading 3
```

#### Heading 4

```
#### Heading 4
```

##### Heading 5

```
##### Heading 5
```

## Text Formatting

You can use *italicized text*.

```
You can use *italicized text*.
```

You can use **bold text**.

```
You can use **bold text**.
```

You can use `monospaced text`.

```
You can use `monospaced text`.
```

You can use <s>strikethrough text</s> (but it must be via HTML5).

```
You can use <s>strikethrough text</s> (but it must be via HTML5).
```

> This is a blockquote

```
> This is a blockquote
```

## Bullet Lists and Numbered Lists

Add an empty line between the text above a bulleted list and the first bulleted list item:

* Bulleted list item 1 (no indentation)
* Bulleted list item 2

```
Add an empty line between the text above a bulleted list and the first bulleted list item:

* Bulleted list item 1 (no indentation)
* Bulleted list item 2
```

Add an empty line between the text above a numbered list and the first numbered list item:

1. First numbered list item (no indentation)
1. Second numbered list item
1. Third numbered list item

```
Add an empty line between the text above a numbered list and the first numbered list item:

1. First numbered list item (no indentation)
1. Second numbered list item
1. Third numbered list item
```

> **Note:** If you include an image, a code block, or even a new paragraph of text within a numbered step, it can throw off the renumbering in the next step. See ["List Items Containing Paragraphs"](#list-items-containing-paragraphs) later on this page.

### Nested Lists

#### Two-Level Bullet List

This is a two-level bullet list:

  * Item 1 (indent 2 spaces)
  * Item 2
    * Item 2a (indent 4 spaces)
    * Item 2b

```
This is a two-level bullet list:

  * Item 1 (indent 2 spaces)
  * Item 2
    * Item 2a (indent 4 spaces)
    * Item 2b
```

> **Note:** This indentation will also work if the sublist is a numbered list.

#### Three-Level Bullet List

This is a three-level bullet list:

  * Item 1 (indent 2 spaces)
  * Item 2
    * Item 2a (indent 4 spaces)
        * Item 2ai (indent 8 spaces)
        * Item 2aii
    * Item 2b

```
This is a three-level bullet list:

  * Item 1 (indent 2 spaces)
  * Item 2
    * Item 2a (indent 4 spaces)
        * Item 2ai (indent 8 spaces)
        * Item 2aii
    * Item 2b
```

#### Two-Level Numbered List

Two-level numbered list:

1. Item 1 (no indentation)
1. Item 2
    1. Item 2.1 (indent 4 spaces)
    1. Item 2.2

```
Two-level numbered list:

1. Item 1 (no indentation)
1. Item 2
    1. Item 2.1 (indent 4 spaces)
    1. Item 2.2
```

If you prefer your sublist to be ordered by lower-case letters (a., b., c., ...), use HTML:

<ol>
 <li>Step 1</li>
 <li>Step 2
  <ol type="a">
   <li>Substep 2a</li>
   <li>Substep 2b</li>
   <li>Substep 2c</li>
  </ol>
</li>
 <li>Step 3</li>
</ol>

```
<ol>
 <li>Step 1</li>
 <li>Step 2
  <ol type="a">
   <li>Substep 2a</li>
   <li>Substep 2b</li>
   <li>Substep 2c</li>
  </ol>
</li>
 <li>Step 3</li>
</ol>
```

> **Note:** The substeps render as *i.*, *ii.*, and *iii.* on BBGitHub, but will render as *a.*, *b.*, and *c.* on Tutti.

### List Items Containing Paragraphs

Sometimes, a step in an ordered list requires paragraphs:

1. This is the first step in a numbered list. It is not indented in the Markdown. But it has a second paragraph before the second step. There must be a blank line between paragraphs in the same numbered list item.

    This is the second paragraph in the first step. It must be indented 4 spaces. There must be a blank line between this paragraph and the second step in the numbered list.

2. This is the second step in the numbered list.

```
Sometimes, a step in an ordered list requires paragraphs:

1. This is the first step in a numbered list. It is not indented in the Markdown. But it has a second paragraph before the second step. There must be a blank line between paragraphs in the same numbered list item.

    This is the second paragraph in the first step. It must be indented 4 spaces. There must be a blank line between this paragraph and the second step in the numbered list.

2. This is the second step in the numbered list.
```

Of course, this can also be done with bullet lists:

* This is the first item in a bullet list. It is not indented in the Markdown. But it has a second paragraph before the second bullet list item. There must be a blank line between paragraphs in the same bullet list item.

    This is the second paragraph in the first bullet item. It must be indented 4 spaces. There must be a blank line between this paragraph and the second item in the bullet list.

* This is the second item in the bullet list.

```
Of course, this can also be done with bullet lists:

* This is the first item in a bullet list. It is not indented in the Markdown. But it has a second paragraph before the second bullet item. There must be a blank line between paragraphs in the same bullet list item.

    This is the second paragraph in the first bullet item. It must be indented 4 spaces. There must be a blank line between this paragraph and the second item in the bullet list.

* This is the second item in the bullet list.
```

## Hyperlinks

### Bloomberg Functions

To a Bloomberg Terminal function, like [TOP](https://blinks.bloomberg.com/screens/TOP)

```
To a Bloomberg Terminal function, like [TOP](https://blinks.bloomberg.com/screens/TOP)
```

To a Bloomberg function with a tail, like [ELRN BAS](https://blinks.bloomberg.com/screens/ELRN%20BAS)

```
To a Bloomberg function with a tail, like [ELRN BAS](https://blinks.bloomberg.com/screens/ELRN%20BAS)
```

> **Note:** There must be a `%20` in place of every space in the Bloomberg command.

### Email Addresses

Bloomberg email addresses should be done in Markdown like this:

[Kenny Kistler](https://blinks.bloomberg.com/screens/MSG%203827954)

```
[Kenny Kistler](https://blinks.bloomberg.com/screens/MSG%203827954)
```

> **Note:** There must be a `%20` in place of every space in the Bloomberg command.

Or in HTML like this:

<a href="https://blinks.bloomberg.com/screens/MSG 3827954">Kenny Kistler</a>

```html
<a href="https://blinks.bloomberg.com/screens/MSG 3827954">Kenny Kistler</a>
```

Links to non-Bloomberg email addresses should be done like this in Markdown:

[Splunk Education (America)](https://blinks.bloomberg.com/screens/MSG%20education_AMER@splunk.com)

```
[Splunk Education (America)](https://blinks.bloomberg.com/screens/MSG%20education_AMER@splunk.com)
```

Or like this in HTML:

<a href="https://blinks.bloomberg.com/screens/MSG education_AMER@splunk.com">Splunk Education (America)</a>

```html
<a href="https://blinks.bloomberg.com/screens/MSG education_AMER@splunk.com">Splunk Education (America)</a>
```

### Web URLs

To a non-Tutti URL, like [bloomberg.com](https://www.bloomberg.com/)

```
To a non-Tutti URL, like [bloomberg.com](https://www.bloomberg.com/)
```

### Tutti URLs

To another page within the same directory in your repo: [Platform Overview](overview.md)

```
To another page within the same directory in your repo: [Platform Overview](overview.md)
```
> **Note**: That is, just the filename, *including* the `.md` file extension!

To another page in a different directory in your repo: [Tutti Design Objectives](/tutti-admin-docs/tutti_design_objectives/README)

```
To another page in a different directory in your repo: [Tutti Design Objectives](/tutti-admin-docs/tutti_design_objectives/README)
```

> **Note:** That is, the directory path from your repo's root level, *not including* the `.md` file extension!

To a Tutti page outside your repo: [DPKG](/dpkg/README)

```
To a Tutti page outside your repo: [DPKG](/dpkg/README)
```

> **Note:** That is, everything *after* `.com` in the Tutti page's URL (which *doesn't* include the `.md` file extension!).

To a specific section of a Tutti page *outside your repo*: [DPKG Quick Links](/dpkg/README#quick-links)

```
To a specific section of a Tutti page *outside your repo*: [DPKG Quick Links](/dpkg/README#quick-links)
```

> **Note:** `.md` is **not** included!

To a specific section of a different page *within your repo*: 
[Topic Organization on Tutti](overview.md#topic-organization-on-tutti)

```
To a specific section of a different page *within your repo*: 
[Topic Organization on Tutti](overview.md#topic-organization-on-tutti)
```

> **Note:** `.md` **must be** included!

To a specific section on the same page: [#code-blocks](#code-blocks)

```
To a specific section on the same page: [#code-blocks](#code-blocks)
```

> **Note:** **DO NOT** leave the square brackets empty in a link!

## Code Blocks

```
// This is a code block (rendered)
```

    
    ```
    // This is a code block (coded)
    ```

### Code Block within a List Item

If a code block is within a bullet list item, indentation isn't necessary, because it won't mess up the formatting of the next bullet:

* This is the first item in a bullet list. It is not indented in the Markdown. It contains a code block before the second bullet item. There is a blank line before and after the code block, and the code block is not indented.

```
// code within a bullet list item
```

* This is the second item in the bullet list.

However, this won't work in a conventional Markdown numbered list, because it will break the autonumbering sequence (it will restart the numbering from 1 after the code block). To get around this problem, use the literal number of each step (i.e. don't use 1 for every step) and put a backslash between the number and the period.

1\. This is the first item in a numbered list. It is not indented in the Markdown. It contains a code block before the second numbered item. There is a blank line before and after the code block, and the lines in the code block are not indented.

```js
// code within a numbered list item
// How about a second line?
```

2\. This is the second item in the numbered list.

3\. This is the third item. A blank line is required between steps in this list.

(See this page's source code to see exactly how this is done.)

### Syntax Highlighting

Tutti supports syntax highlighting.

Tutti uses the Python Markdown parser, which has an extension for syntax highlighting that uses Pygments. The list of supported languages can be found at [pygments.org](https://pygments.org/languages).

Enter the language name after the code block backticks:

<pre>```typescript</pre>

```typescript
function greeter(person: string) {
    return "Hello, " + person;
}

let user = "Newman";

document.body.textContent = greeter(user);
```

## Tables

Technically, Markdown doesn't provide any special syntax for tables. There are Markdown syntax extensions that do provide syntax for simple tables.

| Column 1      | Column 2 | Column 3  |
| ----------- | ----------- | --------- |
| Data      | Data       | Data       |
| Data   | Data        | Data        |

<p>&nbsp;</p>

```
| Column 1      | Column 2 | Column 3  |
| ----------- | ----------- | --------- |
| Data      | Data       | Data       |
| Data   | Data        | Data        |
```

Markdown extensions for tables are typically limited in what they can do. For example, they might not allow row or cell spanning or multi-line text within a cell.

If you want to go beyond the limits of a simple table, it's probably best to use HTML:

<!-- 3x3 table plus title row -->
<table width=100% class="tg">

<!-- 3-column title row -->
<tr>
 <th width="33%" class="tg-baqh" nowrap>Column 1 Title</th>
 <th width="33%" class="tg-baqh" nowrap>Column 2 Title</th>
 <th width="33%" class="tg-baqh" nowrap>Column 3 Title</th>
</tr>

<!-- 3-column data row 1-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">HTML tables will easily allow long strings of text that need to wrap to a second line with a cell</p></td>
</tr>

<!-- 3-column data row 2-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">cell data</p></td>
</tr>

<!-- 3-column data row 3-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">cell data</p></td>
</tr>

</table>


```
<!-- 3x3 table plus title row -->
<table width=100% class="tg">

<!-- 3-column title row -->
<tr>
 <th width="33%" class="tg-baqh" nowrap>Column 1 Title</th>
 <th width="33%" class="tg-baqh" nowrap>Column 2 Title</th>
 <th width="33%" class="tg-baqh" nowrap>Column 3 Title</th>
</tr>

<!-- 3-column data row 1-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">cell data</p></td>
</tr>

<!-- 3-column data row 2-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">cell data</p></td>
</tr>

<!-- 3-column data row 3-->
<tr>
 <td valign="top" ><p class="smallTableText">cell data</p></td>
 <td valign="top"><p class="smallTableText">cell data</p></td> 
 <td valign="top"><p class="smallTableText">cell data</p></td>
</tr>

</table>
```

For more information, see [HTML Tables](https://www.w3schools.com/html/html_tables.asp).

## Forcing White Space

If you need to force white space between an image, code block, or table and the next paragraph of text, use the following HTML:

```
<p>&nbsp;</p>
```

## Text Coloring

<p style="color:red">Use HTML to color a paragraph.</p>

```
<p style="color:red">Use HTML to color a paragraph.</p>
```

<p>This is how to color <span style="color:red">a few words</span> in a paragraph.</p>

```
<p>This is how to color <span style="color:red">a few words</span> in a paragraph.</p>
```

For the complete list of available color names, see [HTML Color Names](https://www.w3schools.com/colors/colors_names.asp).

## Font Sizing

<p>&nbsp;</p>

<p style="font-size:26px">This is a paragraph at 26 pixels.</p>
<p style="font-size:12px">This is a paragraph at 10 pixels.</p>

```
<p style="font-size:26px">This is a paragraph at 26 pixels.</p>
<p style="font-size:12px">This is a paragraph at 10 pixels.</p>
```

## Images

To insert an image "as-is" -- that is, at its original size with no resizing capabilities -- use the following Markdown:

```
![](bloomberg3.gif)
```

![](bloomberg3.gif)

<p>&nbsp;</p>

> **Note**: This example assumes that the image file is in the same repo directory as the Markdown source file. If your image file is in a different directory, you must specify the correct path to the image file.

For best results with large screen shots, keep the width of your source image less than 700 pixels and autosize the height based on the width. If your images are small illustrations, such as a UI button or an icon, don't make them much bigger than their actual size.

If you want to size your image dynamically based on the space available to it on the webpage, use HTML like the following:

```
<img src="bloomberg3.gif" width="50%" height="50%">
```

<img src="bloomberg3.gif" width="50%" height="50%">

<p>&nbsp;</p>

Note that the percentages in the `width` and `height` attributes above are not percentages of the original size of the image. They are based on the space available to the image. So this image is given 50% of the space available to it on the webpage, and so the size of the image changes as the size of your browser window changes. (For comparison, the code block represents 100% of the available horizontal space.)
