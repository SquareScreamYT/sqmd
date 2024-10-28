# sq's Markdown

## Introduction

This is a guide to using sqmd, a Markdown-like language that is a superset of Markdown with extended features. This document is best viewed in VS Code with [this extension pack](https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview).

## Headings

Headings in sqmd are the same as in Markdown:

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

## Text Formatting

Text formatting in sqmd is the same as in Markdown:

```
*Italic*
**Bold**
~~Strikethrough~~
_Underline_
```

*Italic*  
**Bold**  
~~Strikethrough~~  
<u>Underline</u>  

---

To highlight text, use surround your text with 2 equal signs:

```
==Highlighted Text==
```

<mark>Highlighted Text</mark>

---

To make it so that your sentence doesn't create a new line, use a \ at the end of the line.

```
This is the first line.\
This is the second line.
```

This is the first line.
This is the second line.

## Horizontal Lines

To make a horizontal line, use three dashes:

---

## Code Blocks

To create a code block, use three backticks:
`````
```
Code Block
```

`Code Block` within a sentence

````
```
Code Block inside a code block
```
````
`````

```
Code Block
```

`Code Block` within a sentence

````
```
Code Block inside a code block
```
````

## Block Quotes

To create a block quote, use a greater than symbol:

```
> Block Quote
> > More Block Quote
```

> Block Quote
> > More Block Quote

## Lists

To create a list, use dashes or numbers:

```
- Item
- Item
  - Item
  - Item
- Item

1. Item 1
2. Item 2
  a. Item 2a
  b. Item 2b
3. Item 3
```

- Item
- Item
  - Item
  - Item
- Item

1. Item 1
2. Item 2  
  a. Item 2a  
  b. Item 2b
3. Item 3

## Links

To create a link, use square brackets for the text and parentheses for the link:

```
[Link](https://example.com)
```

[Link](https://example.com)

## Images

To create an image, use an exclamation point, square brackets for the alt text, and parentheses for the link, and curly brackets for the size:

```
![sq button](/sq_button.svg){200,100}
```

<img src="https://raw.githubusercontent.com/SquareScreamYT/SquareScreamYT.github.io/refs/heads/main/sq_button.svg" alt="sq button" width="200" height="100">

## Tables

To create a table, use pipes to separate columns and dashes to separate rows:

```
| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Row 1    | Row 1    | Row 1    |
| Row 2    | Row 2    | Row 2    |
| Row 3    | Row 3    | Row 3    |
```

| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Row 1    | Row 1    | Row 1    |
| Row 2    | Row 2    | Row 2    |
| Row 3    | Row 3    | Row 3    |

You can also use colons to align the columns:

```
| Left Aligned | Center Aligned | Right Aligned |
| :----------- | :------------: | ------------: |
| Left         | Center         | Right         |
```

| Left Aligned | Center Aligned | Right Aligned |
| :----------- | :------------: | ------------: |
| Left         | Center         | Right         |

You can add to the column and row span by using `\k` for row span and `\l` for column span:

```
| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Row 1    | Row 1 \l            |
| Row 2    | Row 2    | Row 2 \k |
| Row 3    | Row 3    |          |
```

<table>
  <tr>
    <td><b>Column 1</b></td>
    <td><b>Column 2</b></td>
    <td><b>Column 3</b></td>
  </tr>
  <tr>
    <td >Row 1</td>
    <td colspan=2>Row 1</td>
  </tr>
  <tr>
    <td >Row 2</td>
    <td>Row 2</td>
    <td rowspan=2>Row 2</td>
  </tr>
  <tr>
    <td>Row 3</td>
    <td>Row 3</td>
  </tr>
</table>

Remember to leave a blank where the extra cell would be.

## Task List

To create a task list, use a dash followed by a space and a bracket:

```
- [ ] Task
- [x] Completed Task
```

- [ ] Task
- [x] Completed Task

## Subscripts and Superscripts

To create a subscript, use a tilde followed by the text:

```
H~2~O
```

H<sub>2</sub>O

To create a superscript, use a caret followed by a text:

```
x^2^
```

x<sup>2</sup>

## Definition List
To create a definition list, use a colon followed by a space and the definition:

```
Term 1
: Definition 1

Term 2
: Definition 2
```

<dl>
<dt>Term 1</dt>
<dd>Definition 1</dd>

<dt>Term 2</dt>
<dd>Definition 2</dd>
</dl>

## Emoji

To create an emoji, use a colon followed by the name of the emoji:

```
:smile:
:apple:
:books:
```

:smile:  
:apple:  
:books:

## Colors

To set a text to a color, use `\c` followed by a hexcode, and then `\e`: 

```
\c#ff6347\eThis red is really nice
```

<span style="color:#ff6347">This red is really nice</span>

To set the highlight color, use `\h` followed by a hexcode, and then `\e`:

```
\h#ff6347\eIt looks like the color of a tomato
```

<mark style="background-color:#ff6347">It looks like the color of a tomato</mark>

To reset the color, use `\r`:

```
\c#ff6347\eRed\r White
```

<span style="color:#ff6347">Red</span> <span style="color:#ffffff">White</span>

## Abbreviations

To create an abbreviation, use an asterisk followed by square brackets surrounding the abbreviation, and then a colon followed by the full name:

```
*[MD]: MarkDown
```

<abbr title="MarkDown">MD</abbr>

## Comments
Comments in sqmd are the same as in Javascript:

```
// This is a single line comment

/*
This is a
multi-line
comment
*/
```

Comments are not displayed in the output.

## Default Colors

To add default colors, use `/* */` at the start of the file:

```
/*
  background-color:#0d1117,
  text-color:#dadfda,
  highlight-color:#272115,
  code-color:#151b23,
  link-color:#0000ee
*/
```

This will change the default colors to of the output.

## Footnotes

To create a footnote, use a caret followed by a number:

```
Here is a footnote[^1]

[^1]: This is the footnote
```

Here is a footnote[^1]

[^1]: This is the footnote
