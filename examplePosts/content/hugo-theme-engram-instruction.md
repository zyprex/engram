---
title: "Hugo Theme Engram Instruction"
date: 2020-12-15T13:50:21+08:00
categories: hugo
---

# feature list

1. consistent user experience both in Mobile and Desktop
1. 5th color theme fit your background image
1. easy to remove unwanted themes or make new themes
1. 3 view mode happy your eyes
1. all markdown images are lazy load
1. each page can use it's own background image
1. high speed without `backgroundImage` in `config.toml`, or with fast view mode
1. touch margin flip page up or down, touch corner go top or bottom
1. supported js library
   - [katex](https://katex.org/) for latex math formulation
   - [mermaid](https://github.com/mermaid-js/mermaid) for sequence, flow chart, pie chart, gantt etc.


# quick start

## apply config.toml

```toml
newContentEditor = "vim"
languageCode = "en-us"
baseURL = "/"
title = "Zyprex's Blog"
theme = "Engram"
paginate = 10
summaryLength = 200
hasCJKLanguage = true
enableEmoji=true
minify = true

[params]
    author = "zyprex"
    avatar = "/img/git_face.png"
    favicon = "/img/git_face.png"
    # optional
    description = "Zyprex's Awesome Hugo Site"
    backgroundImage = "/img/default.jpg"

[markup.goldmark.renderer]
    # support raw HTML
    unsafe= true

[markup.tableOfContents]
    startLevel = 1
    endLevel = 6
    ordered = false

[markup.highlight]
    anchorLineNos = false
    codeFences = true
    guessSyntax = false
    hl_Lines = ""
    lineAnchors = ""
    lineNoStart = 1
    lineNos = true
    lineNumbersInTable = true
    noClasses = true
    style = "monokai"
    tabWidth = 2

[frontmatter]
   lastmod = ["lastmod", ":fileModTime", ":default"]
   date = [":filename", ":default"]
```

## full modal of frontmatter

```yaml
title: "Hugo Theme Engram Instruction"
date: 2020-12-15T13:50:21+08:00
tags: ['x','y','z']
categories: x
toc: true
mermaid: false
math: false
backgroundImage: "/img/default.jpg"
draft: true
```

# test page

those test page show more detail of this site's function

1. test markdown style
1. test lazy image load
1. test shortcode style
1. test long text with full feature enable (SLOW LOAD WARN! be patient)

# Appreciation

  [Lorem Ipsum](https://www.lipsum.com/ "Lorem Ipsum - All the facts - Lipsum generator")

  [godoc](https://godoc.org/time#Time "godoc-time")

  [css-protips](https://github.com/AllThingsSmitty/css-protips "css-protips")

  [pure-css-tabs](https://codeconvey.com/simple-css-tabs-without-javascript/ "simple-css-tabs-without-javascript")

  [google-fonts](https://developers.google.cn/fonts/docs/getting_started "google-fonts")

  [icon svg](https://iconsvg.xyz/)

  [flex-align](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)
