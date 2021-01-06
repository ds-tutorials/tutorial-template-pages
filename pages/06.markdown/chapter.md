---
title: Markdown
media_order: milky-way.jpg
taxonomy:
    category:
        - docs
intro:
    level: beginner
---

Markdown is a lightweight markup language. It is designed to allow easily typing plain text that can easily be converted into formatted HTML.

Two big rules to remember are about how Markdown deals with new lines and spacing. Whenever creating a new paragraph, list, heading, or other block of text, make two new lines (press enter/return twice) so that the blocks are clearly separated. Text separated with only one line may be treated as text separated with only a space.

Markdown also collapses any excess spacing. In other words, if you separate two words with two or more spaces, they will still only be displayed with one space between them.

## Markdown Syntax

If you are unfamiliar with Markdown, you will probably want to review the [Grav Markdown documentation](https://learn.getgrav.org/16/content/markdown). There are also many additional reference guides for Markdown available on the internet. This page will provide examples of the various structures you may want to use.

### Headings

In Markdown:

```md
# Heading Level One

## Heading Level Two

### Heading Level Three

#### Heading Level Four

##### Heading Level Five

###### Heading Level Six
```

Result:

# Heading Level One

## Heading Level Two

### Heading Level Three

#### Heading Level Four

##### Heading Level Five

###### Heading Level Six

---

Headings are particularly important because they provide visual and semantic (meaningful non-visual) structure to your pages. Every page should have one heading level one, which will be the page title and is already built into the tutorial template. Headings go from level one to level six, with level determined by number of hashtags.

### Paragraphs

Paragraphs are the most basic unit you are likely to be working with. These are written exactly as normal. You do not have to do anything special.

### Links

Links are very similar to images. They use the format `[Link text](link URL)`. The main difference is that there is no exclamation point at the start.

In Markdown:

```md
Check out the [OU Libraries website](https://www.libraries.ou.edu).
```

Result:

Check out the [OU Libraries website](https://www.libraries.ou.edu).

---

For accessibility, always make sure that the link text makes it clear where the link will lead to, even without context.

An example of ambiguous link text (to avoid):

Check out the OU Libraries website [here](https://www.libraries.ou.edu).

#### Linking to a Specific Section

It is possible to link to a specific section or element in one of the pages of your tutorial, as long as that element has an id associated with it. This theme will automatically create an id for each heading, as they are the most likely elements you would want to link to. The id will be all lower case with spaces replaced with dashes - just like the relationship between page title and folder name. There should never be duplicate ids on a page, so if the heading would create one, the theme will add a number. So if you had three headings, each of which were called `This Heading`, the links would be `this-heading`, `this-heading-1`, and `this-heading-2`. The order of the ids is based first on heading level, and then on page order. Your browser should have a way to inspect elements if you want to check the id of any of your headings.

To link to a specific part of a page, you will need to add a hashtag to the end of the link, and then the id of the heading you want to link to. For example: `https://www.my-domain.oucreate.com/a-random-page#this-heading`.

You can also link to a specific section on the same page. In this case, you do not have to provide a full url - it is enough to use the hashtag and id. For example: `#this-heading`. This is often most useful when you have a single page with a lot of text - you can create a table of contents at the beginning of the page and link to each section for easy navigation.

### Lists

In Markdown:

```md
An unordered list of colors

- Blue
- Green
- Red

An ordered list of colors

1. Blue
2. Green
3. Red
```

Result:

An unordered list of colors

- Blue
- Green
- Red

An ordered list of colors

1. Blue
2. Green
3. Red

### Images

Images in Markdown follow the format `![Image alternative text](image-name.jpg)`. Note the alternative text - this is extremely important to include with all of your images.

The format shown above works for any image you upload to the page. If you want to include an image you are not uploading to that page, you will need to provide the full link to the image instead of just the image name.

Markdown for uploaded image:

```md
![The Milky Way over New Zealand](milky-way.jpg)
```

Result:

![The Milky Way over New Zealand](milky-way.jpg)

### Bold and Italics

In Markdown:

```md
This is **bold** text. This is _italicized_ text.
```

Result:

This is **bold** text. This is _italicized_ text.

### Blockquotes

In Markdown:

```md
> The problem with quotes on the Internet is that it is hard to verify their authenticity. - Abraham Lincoln
```

Result:

> The problem with quotes on the Internet is that it is hard to verify their authenticity. - Abraham Lincoln

#### Notices

Markdown notices provide another way to set text apart from the rest of the page and work in much the same way. Instead of using the greater than sign, notices use exclamation points.

In Markdown:

```md
! Notice 1

!! Notice 2

!!! Notice 3

!!!! Notice 4
```

Result:

! Notice 1

!! Notice 2

!!! Notice 3

!!!! Notice 4

#### Getting Fancy

You can include other Markdown elements inside a blockquote or notice. For example:

```md
!!! ##### Notice with Heading Level Five
!!!
!!! This is a Markdown notice with additional structure.
!!! 
!!! - List item 1
!!! - List item 2
!!! - List item 3
```

Becomes:

!!! ##### Notice with Heading Level Five
!!!
!!! This is a Markdown notice with additional structure.
!!! 
!!! - List item 1
!!! - List item 2
!!! - List item 3

### Tables

In Markdown:

```md
| Column 1 | Column 2 |
|----------|----------|
| Item a1  | Item a2  |
| Item b1  | Item b2  |
```

Result:

| Column 1 | Column 2 |
|----------|----------|
| Item a1  | Item a2  |
| Item b1  | Item b2  |

The lines at the front and end, as well as the neat spacing, are not necessary. The following works equally well:

```md
Column 1 | Column 2
-|-
Item a1 | Item a2
Item b1 | Item b2
```

### Horizontal Lines

In Markdown:

```md
---
```

The result is the same line you may have noticed a couple times on this page already:

---

### Code

#### Inline Code

You can provide sections of code within paragraphs by using backticks. This also comes in handy for more than just providing programming instructions.

In Markdown:

```md
To access the admin panel dashboard, append `\admin` to the site URL.
```

Result:

To access the admin panel dashboard, append `\admin` to the site URL.

#### Code Blocks

In Markdown:

~~~md
```
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```
~~~

Result:

```
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```

You can also use tildes `~~~` instead of backticks ` ``` `.

##### Syntax Highlighting

The Highlight plugin provides syntax highlighting for code blocks in markdown. For this to work, you will need to provide the language the code is written in. The above example used Python (py) code, but did not specify the language. You will notice that even so it has some syntax highlighting. It is always better to specify the language if you can, however.

In Markdown:

~~~md
```py
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```
~~~

Result:

```py
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```

#### Copying Code to Clipboard

The Learn2 theme, which the Tutorial Template inherits from, provides an option to copy code to the clipboard. By default, the Tutorial Template theme sets all inline code sections to not include this option, and all fenced code blocks to include it.

To include the copy-to-clipboard option for inline code:

```md
To access the admin panel dashboard, append `clip: \admin` to the site URL.
```

Result:

To access the admin panel dashboard, append `clip: \admin` to the site URL.

---

To remove the copy-to-clipboard option for a code block:

~~~md
```py
noclip:
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```
~~~

Result:

```py
noclip:
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
```

## Extra Options

### Resizing Images

If you want to resize an image you can add `?cropResize=width,height` to the end of your image URL. You must provide both numbers, but cropResize will scale the image so that it fits within the box you have specified but does not necessarily fill that box. (It will also cut off any empty space, so if you are resizing an image with the original dimensions of 400,400, `?cropResize=100,1000` and `?cropResize=200,100` should have no difference. This is the most likely function you will want to use, but the [Grav media documentation](https://learn.getgrav.org/content/media) has information on a number of other functions.

Example usage for an image named `my-image.png` within the folder of the page you are displaying it: `![alt text](my-image.png?cropResize=300,300)`

### Shortcodes

The Shortcode Core plugin provides additional Markdown functionality called shortcodes. For information on how to use these, view the [Shortcode Core documentation](https://github.com/getgrav/grav-plugin-shortcode-core/blob/master/README.md).

### HTML

Markdown will also accept HTML code directly. Some of the shortcodes referenced above add additional HTML functionality, but if there is something more complex you want to do that Markdown doesn't implement, feel free to add HTML to your pages.

### Markdown Editors

If you find that you love Markdown as much as I do, you can download editors for your computer that will make it easy to write notes and documents in Markdown. [Visual Studio Code](https://code.visualstudio.com/) is an all-purpose editor that can support Markdown, as well as programming languages like Python or Javascript. [Obsidian](https://obsidian.md/) is a Markdown only editor that can help you organize your notes. It is free for personal use. Of course, there are many other excellent editors out there, as well! Let me know your favorite and I will add it to this section.