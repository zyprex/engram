---
title: "Hugo Theme Engram Markdown"
date: 2020-12-18T12:59:00+08:00
categories: hugo
toc: true
math: true
mermaid: ture
---

# Basic Markdown Syntex
## Text
### Heading 
{{<fold title="Head" open="">}}
    # heading 1
    ## heading 2
    ### heading 3
    #### heading 4
    ##### heading 5
    ###### heading 6
# heading 1
## heading 2
### heading 3
#### heading 4
##### heading 5
###### heading 6
{{</fold>}}
### Emphasis 
{{<fold title="Emphasis" open="">}}
    _italic_ __bold__
    *italic* **bold**
    
    ~~strikethrough~~
    
    _**bold&italic**_

_italic_ __bold__
*italic* **bold**

~~strikethrough~~

_**bold&italic**_
{{</fold>}}
### Lists
{{<fold title="Lists" open="">}}
    - item1
      - item1-1
      - item1-2
      - item1-3
        - item1-3-1
        - item1-3-2
        - item1-3-3
    - item2
    - item3
    - item4
    
    1. item1
    1. item2
    1. item3
    1. item4

- item1
  - item1-1
  - item1-2
  - item1-3
    - item1-3-1
    - item1-3-2
    - item1-3-3
- item2
- item3
- item4

1. item1
1. item2
1. item3
1. item4
{{</fold>}}
### Blockquotes
{{<fold title="Blockquotes" open="">}}
    > blockquote
    > > # nested blockquote 
    > > > ## nested blockquote nested again

> blockquote
> > # nested blockquote 
> > > ## nested blockquote nested again
{{</fold>}}
### link
    [link_name](link "title")
[link_name](link "title")

### Line Breaks
To create a line break, end a line with two or more spaces
### Horizontal Rules
To create a horizontal rule, use three or more asterisks (`***`), dashes (`---`), or underscores (`___`) on a line by themselves.

-----------------------

## Image
    ![](/img/brige.jpg "brige")
![](/img/brige.jpg "brige")



# Extended Markdown Syntex
## Table

    Fruit Name  | Apple  | Banana
    :---        | :---:  | ---:
    *price*     | 12.0   | 34.0
    *count*     | 13000  | 19000

Table
Fruit Name  | Apple  | Banana
:---        | :---:  | ---:
*price*     | 12.0   | 34.0
*count*     | 13000  | 19000
## Code Block
    ```html
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
    </head>
    <body>
        the very basic of an html file
    </body>
    </html>
    ```

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
    the very basic of an html file
</body>
</html>
```
code block with unknow language

    ```fakelang
    # |__aAbBcCdDeEfFgGhHiIjJkKlLmMnN
    # oOpPQqrRsStTuUvVwWxXyYzZ
    main:
      <data> arr=[1234567890,!@#$%^&*"'\.?/];
      for i in arr { print(i); }
    ```

```fakelang
# |__aAbBcCdDeEfFgGhHiIjJkKlLmMnN
# oOpPQqrRsStTuUvVwWxXyYzZ
main:
  <data> arr=[1234567890,!@#$%^&*"'\.?/];
  for i in arr { print(i); }
```
## Footnote
    footnote[^1]
      [^1]: I am a footnote

## Inline HTML
Hugo not support inline HTML, but you can enable it by set unsafe option in your `config.toml`

```toml
# :file_folder:/config.toml
[markup.goldmark.renderer]
    unsafe = true
```
    <abbr title="Graphics Interchange Format">GIF</abbr>
    sup<sup>123</sup> sub<sub>123</sub> <mark>mark</mark> <kbd>ctrl</kbd> key

<abbr title="Graphics Interchange Format">GIF</abbr>
sup<sup>123</sup> sub<sub>123</sub> <mark>mark</mark> <kbd>ctrl</kbd> key

# Github Flavored Markdown
## Emoji
https://www.webfx.com/tools/emoji-cheat-sheet/
```toml
# :file_folder:/config.toml
enableEmoji = true
```
:see_no_evil: :hear_no_evil: :speak_no_evil:
:heart: :star: :warning: :link:

## TaskList
    ```
    - [x] checked
    - [ ] unchecked
    ```

tasklist (GFM: Github Flavored Markdown)
- [x] checked
- [ ] unchecked

# Extension of Javascript Liberary
## katex
:bell: on article FrontMatter, value `math` must be `true`.

    inline math formulation $\sqrt{2}$

inline math formulation $\sqrt{2}$

    $$
    f(x) = \int_{-\infty}^\infty
        f\hat\xi,e^{2 \pi i \xi x}
        \,d\xi
    $$

$$
f(x) = \int_{-\infty}^\infty
    f\hat\xi,e^{2 \pi i \xi x}
    \,d\xi
$$

## mermaid
:bell: on article FrontMatter, value `mermaid` must be `true`.
```html
<div class="mermaid">
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
</div>
```
<div class="mermaid">
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
</div>

# Ref
[Markdownguide](https://www.markdownguide.org/basic-syntax)

[Github Flavored Markdown](https://github.github.com/gfm/)
