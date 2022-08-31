# Detailed markdown docs
[GITHUB DOCS](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

# Summary

- [Titles](#titles)
- [Links](#links)
- [Images](#images)
- [CodeBlocks](#code-blocks)
- [Tables](#tables)



# Titles

As we started writing a markdown document, we need to add a title and some sub-headers.

Markdown supports two styles of headers, Setext and atx.

Setext-style headers are “underlined” using equal signs (for first-level headers) and dashes (for second-level headers). For example:

```markdown
This is an H1
=============

This is an H2
-------------
```

Any number of underlining =’s or -’s will work.

Atx-style headers use 1-6 hash characters at the start of the line, corresponding to header levels 1-6. For example:

```markdown
# This is an H1

## This is an H2

###### This is an H6
```

Optionally, you may “close” atx-style headers. This is purely cosmetic — you can use this if you think it looks better. The closing hashes don’t even need to match the number of hashes used to open the header. (The number of opening hashes determines the header level.) :

```markdown
# This is an H1 #

## This is an H2 ##

### This is an H3 ######
```



# Links

Markdown supports two styles of links: inline and reference.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately after the link text’s closing square bracket. Inside the parentheses, put the URL where you want the link to point, along with an optional title for the link, surrounded in quotes. For example:

```markdown
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)
```

Reference-style links use a second set of square brackets, inside which you place a label of your choosing to identify the link:

```markdown
This is [an example][id] reference-style link.
```

You can optionally use a space to separate the sets of brackets:

```markdown
This is [an example] [id] reference-style link.
```

Then, anywhere in the document, you define your link label like this, on a line by itself:

```markdown
[id]: http://example.com/ "Optional Title Here"
```

**GitHub** and **GitBook** supports URL autolinking. They will autolink standard URLs, so if you want to link to a URL (instead of setting link text), you can simply enter the URL and it will be turned into a link to that URL.

# Images

```markdown
# Inline

![Alternative text](/path/to/img.jpg "Optional title")

# Reference

![Alternative text][id]
[id]: url/to/image "Optional title"
```

As you may have noticed, images in Markdown are very similar to links. The difference is that:

- the square brackets must be prefixed with an exclamation mark and
- inside they may have some alternative text. A description of the image, which is displayed if the image can't be loaded.


# Code Blocks

Pre-formatted code blocks are used for writing about programming or markup source code. Rather than forming normal paragraphs, the lines of a code block are interpreted literally.

Here is an example:

```markdown
This is a code block
```

To produce a code block in Markdown, simply indent every line of the block by at least 4 spaces or 1 tab.

For example:

```markdown
This is a normal paragraph:

    This is a code block.
```

You can also create code block separated by:

    ```

### Inline code blocks

Inline code blocks can be written using: `

For example:

    This is a `inline code block`

### Syntax highlighting

You can define the language to be used for syntax highlighting by adding the name on the opening tag. Example:

    ```javascript
    var a = {};
    ```



# Tables

Tables aren't part of the core Markdown spec, but they are part of GFM (GitHub Markdown) and Markdown Here supports them.

Here is an example of table with the output below:

```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |

Colons can be used to align columns.

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Example:

```
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```


