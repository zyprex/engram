---
title: "Hugo Theme Engram Shortcode"
date: 2020-12-15T17:54:35+08:00
categories: hugo
toc: true
---

# hugo shortcode intro

some useful shortcode I made for hugo theme engram.

## What's a shortcode

the shortcode is a piece of html defined in `THEME/layouts/shortcode/`


## A simple example

```html
<div class="{{.Get "class"}}">
  {{- .Inner -}}
</div>
```

this file located in shortcode folder and it's named `d.html`

then at your page, you can write below line.
**NOTE:**  don't keep any space between '{' and '<'

```html
{{ <d class="a-c">}}
some center text
{{ </d>}}
```

below is effect:
{{<d class="a-c">}}
some center text
{{</d>}}

for official guide, please see 
  [hugo shortcode-templates](https://gohugo.io/templates/shortcode-templates/ "shortcode-templates")
or [hugo build-in shortcode](https://gohugo.io/content-management/shortcodes/ "shortcode-build-in")

# shortcode showcase (with example)

## highlight shortcode (hugo build-in)
code:

    {{ < highlight go "linenos=table,hl_lines=1-2 4,linenostart=199" >}}
    package main
    import "fmt"
    func main() {
        fmt.Println("hello highlight")
    }
    {{ < / highlight >}}

result:

{{< highlight go "linenos=table,hl_lines=1-2 4,linenostart=199" >}}
package main
import "fmt"
func main() {
    fmt.Println("hello highlight")
}
{{< / highlight >}}

## (uh) underline highlight
code:

    {{ <uh fg="red">}} underline highlight <b>text</b> {{ </uh>}}

result:

{{<uh fg="red">}} underline highlight <b>text</b> {{</uh>}}

## phrase

code:

    {{ <phrase>}}
    quick fox jump over the lazy dog  
    quick fox jump over the lazy dog  
    quick fox jump **over** the lazy dog
    {{ </phrase>}}

result:

{{<phrase>}}
quick fox jump over the lazy dog  
quick fox jump over the lazy dog  
quick fox jump **over** the lazy dog
{{</phrase>}}


## avatar
**NOTE**: this will use `config.toml` params `avatar`

code:

    {{ <avatar slogan="just do it">}}

result:
{{<avatar slogan="just do it">}}

## tooltip
code:

    {{ <tooltip "this is tooltip content, it can very long or use raw html">}} here {{ </tooltip>}}

result:

mouse over {{<tooltip "this is tooltip content, it can very long or use raw html">}} here {{</tooltip>}}( on mobile device click it)

## quote
code:

    {{ <quote from="Dead Poets Society (1989)">}}
    You must strive to find your own voice. Because the longer you wait to begin,
     the less likely you are to find it at all.
    {{  </quote>}}

result:

{{<quote from="Dead Poets Society (1989)">}}
You must strive to find your own voice. Because the longer you wait to begin,
 the less likely you are to find it at all.
{{</quote>}}


## tabs
code:

    {{ <tabs "one"
        "tab1" "tab2" "tab3"
        "tab1 **content** ---"
        "tab2 content +++"
        "tab3 content ***"
    > }}
    {{ <tabs "two"
       "tab4" "tab5" "tab6"
       "tab4 content ~~~"
       "tab5 content ==="
       "tab6 content ###"
    > }}


result:

{{<tabs "one"
    "tab1" "tab2" "tab3"
    "tab1 **content** ---"
    "tab2 content +++"
    "tab3 content **"
>}}
{{<tabs "two"
    "tab4" "tab5" "tab6"
    "tab4 content ~~~"
    "tab5 content ==="
    "tab6 content ###"
>}}

## fold
code:

    {{ <fold open="false" title="this ...">}}
    this fold is hidden by default, if open params is "false" or it absent.
    {{ </fold>}}

    {{ <fold open="true">}}
    this fold is open by default, cause the open params is "true"
    {{ </fold>}}

result:
{{<fold open="false" title="this ...">}}
this fold is hidden by default, if open params is "false" or it absent.
{{</fold>}}
{{<fold open="true">}}
this fold is open by default, cause the open params is "true"
{{</fold>}}

## timer
code:

    {{ <timer id="tick" time="2020/12/17 19:00" format=" %y %d %h:%m:%s.%e " interval="80">}}

result:

{{<timer id="tick" time="2020/12/17 19:00" format=" %y %d %h:%m:%s.%e " interval="80">}}

