---
layout: post
title:  Markdown Example
subtitle: Each post also has a subtitle
categories: markdown
tags: 
    - markdown
    - example
---

This note demonstrates some of what [Markdown][1] is capable of doing.

You can write regular [markdown](https://markdowntutorial.com/) here and Jekyll will automatically convert it to a nice webpage.  I strongly encourage you to take 5 minutes to learn how to write in markdown- it'll teach you how to transform regular text into bold/italics/headings/tables/etc.


## An exhibit of Markdown


*Note: Feel free to play with this page. Unlike regular notes, this doesn't automatically save itself.*

## Basic formatting

Paragraphs can be written like so. A paragraph is the basic block of Markdown. A paragraph is what text will turn into when there is no reason it should become anything else.

Paragraphs must be separated by a blank line. Basic formatting of *italics* and **bold** is supported. This *can be **nested** like* so.


## Table

Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


## List

### Ordered list
1. Item 1
2. A second item
3. Number 3
4. Ⅳ

*Note: the fourth item uses the Unicode character for [Roman numeral four][2].*

### Unordered list

* An item
* Another item
* Yet another item
* And there's more...

## Paragraph modifiers

### Code block

    Code blocks are very useful for developers and other people who look at code or other things that are written in plain text. As you can see, it uses a fixed-width font.

You can also make `inline code` to add code into other things.




Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

```html
<html>
  <head> </head>
  <body>
    <p>Hello, World!</p>
  </body>
</html>
```

And here is the same code yet again but with line numbers:
{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}


### Quote

> Here is a quote. What this is should be self explanatory. Quotes are automatically indented when they are used.



## Headings

There are six levels of headings. They correspond with the six levels of HTML headings. You've probably noticed them already in the page. Each level down uses one more hash character.

### Headings *can* also contain **formatting**

### They can even contain `inline code`

Of course, demonstrating what headings look like messes up the structure of the page.

I don't recommend using more than three or four levels of headings here, because, when you're smallest heading isn't too small, and you're largest heading isn't too big, and you want each size up to look noticeably larger and more important, there there are only so many sizes that you can use.

## URLs

URLs can be made in a handful of ways:

* A named link to [MarkItDown][3]. The easiest way to do these is to select what you want to make a link and hit `Ctrl+L`.
* Another named link to [MarkItDown](https://www.markitdown.net/)
* Sometimes you just want a URL like <https://www.markitdown.net/>.


## Images
How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){.:block_center}

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be righted!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg#)

<div align=right>
<img src=https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg />
</div>


## Horizontal rule

A horizontal rule is a line that goes across the middle of the page.

---

It's sometimes handy for breaking things up.



## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

### Emoji

:+1:
:smile:

## Finally

There's actually a lot more to Markdown than this. See the official [introduction][4] and [syntax][5] for more information. However, be aware that this is not using the official implementation, and this might work subtly differently in some of the little things.

Put the math expression within <span>$</span>...\$:

\\(\LaTeX{}\\)

$\Pi$

$ a * b = c ^ b $

$ 2^{\frac{n-1}{3}} $

$ \int\_a^b f(x)\,dx. $

\\( \int\_a^b f(x)\,dx. \\)

$$
\begin{cases}
\text{if true}\ foo \\
\text{if false}\ bar
\end{cases}
$$

$ \rho {\rm{FOD}} = \sum\limits{\sigma ,i} {(\delta _1 - \delta _2 n_i^\sigma )|\phi _i^\sigma ({\bf{r}})|^2} $

$$ \rho {\rm{FOD}} = \sum\limits{\sigma ,i} {(\delta _1 - \delta _2 n_i^\sigma )|\phi _i^\sigma ({\bf{r}})|^2} $$


{{ "here is a liquid filter." | capitalize }}

{% capture test %}
\`escape inline code\`  
`inline code`  
Here is a **capture block**.
{% endcapture %}

{{ test | markdownify }}

{% assign x = 100 %} {% assign x = x | divided_by: 3 %}
100 / 3 = {{ x }}

:+1:
:bolivia:

\1. 21312  
\2. 21312  
\4. 4214  

{% highlight python wl linenos %}
import networkx as nx
from collections import Counter

diagrams = defaultdict(list)
particle_counts = defaultdict(Counter)

for (a, b), neighbors in common_neighbors.items():
    # Build up the graph of connections between the
    # common neighbors of a and b.
    g = nx.Graph()
    for i in neighbors:
        for j in set(nl.point_indices[
            nl.query_point_indices == i]).intersection(neighbors):
            g.add_edge(i, j)

    # Define the identifiers for a CNA diagram:
    # The first integer is 1 if the particles are bonded, otherwise 2
    # The second integer is the number of shared neighbors
    # The third integer is the number of bonds among shared neighbors
    # The fourth integer is an index, just to ensure uniqueness of diagrams
    diagram_type = 2-int(b in nl.point_indices[nl.query_point_indices == a])
    key = (diagram_type, len(neighbors), g.number_of_edges())
    # If we've seen any neighborhood graphs with this signature,
    # we explicitly check if the two graphs are identical to
    # determine whether to save this one. Otherwise, we add
    # the new graph immediately.
    if key in diagrams:
        isomorphs = [nx.is_isomorphic(g, h) for h in diagrams[key]]
        if any(isomorphs):
            idx = isomorphs.index(True)
        else:
            diagrams[key].append(g)
            idx = diagrams[key].index(g)
    else:
        diagrams[key].append(g)
        idx = diagrams[key].index(g)
    cna_signature = key + (idx,)
    particle_counts[a].update([cna_signature])
{% endhighlight %}

```cpp
void insert(const char* key) {
    if (*key == '\0') {
        finish = true;
    } else {
        int idx = *key - 'A';
        if (!next[idx])
            next[idx] = new Trie();
        next[idx]->insert(key + 1);
    }
}
```


``` diff
+        'user_exists' => 'SELECT EXISTS(SELECT 1 FROM table WHERE username = (:username || \'@sample'))',
+        'get_users' => 'SELECT split_part(username, \'@\', 1) FROM table WHERE (username ILIKE :search) OR (name ILIKE :search)',
+        'get_password_hash_for_user' => 'SELECT split_part(password, \'{CRYPT}\', 2) FROM table WHERE username = (:username || \'@sample\')',
+        'set_password_hash_for_user' => 'UPDATE table SET password =  \'{CRYPT}\' || :new_password_hash WHERE username = (:username || \'@sample\')',
```

Reload the Nginx:
``` console
$ sudo nginx -s reload
```

|:                        |:                  :|: $$O_3 + C_2H_2 \rightarrow $$         :|||:  $$O_3 + C_2H_4 \rightarrow $$ :|||:       :| 
|:  ^^ Method            :| ^^ $$\lambda^a$$  |    vdW |    TS |    cycloadd.           |  vdW  |  TS  |  cycloadd.           | ^^ MAE    |
|-------------------------|-------------------|--------|-------|------------------------|-------|------|----------------------|-----------|
| $$\lambda$$-tPBE        |   0.20            | -0.40  | 7.69  | -68.00                 | -1.86 | 4.87 | -57.57               | 1.29      |
|-------------------------|-------------------|--------|-------|------------------------|-------|------|----------------------|-----------|
| MC1H-PBE $$^b$$         |   0.25            | -1.08  | 3.66  | -70.97                 | -1.25 | 0.13 | -61.26               | 3.35      |
|-------------------------|-------------------|--------|-------|------------------------|-------|------|----------------------|-----------|
| Reference values $$^c$$ |   ---------       | -1.90  | 7.74  | -63.80                 | -1.94 | 3.37 | -57.15               | --------- |
|=========================|===================|========|=======|========================|=======|======|======================|===========|
| $$^a$$ The optimal mixing parameter.$$\~$$ $$^b$$ From Ref. .$$\~$$  $$^c$$ Best estimates from Ref. . ||||||||


|   1   |  2     |   3   |   4   |  5   |  6   |  7  |
| spancell1     ||   spancell2  || cell | spancell3 ||
|^^ spancell1   ||   spancell2  || cell | spancell3 ||
{:class="custom-table"}


Table header can be eliminated.

|--|--|--|--|--|--|--|--|
|♜ |  |♝ |♛ |♚ |♝ |♞ |♜ |
|  |♟ |♟ |♟ |  |♟ |♟ |♟ |
|♟ |  |♞ |  |  |  |  |  |
|  |♗ |  |  |♟ |  |  |  |
|  |  |  |  |♙ |  |  |  |
|  |  |  |  |  |♘ |  |  |
|♙ |♙ |♙ |♙ |  |♙ |♙ |♙ |
|♖ |♘ |♗ |♕ |♔ |  |  |♖ |


<script>
|:-----:|:-----:|:-----:|:-----:|
| (0,0) | (0,1) | (0,2) | (0,3) |
|     (1,0)    || ^^    | (1,3) |
</script>


|:-----:|:-----:|:-----:|:-----:| ---- |
| (0,0) | (0,1) | (0,2) | (0,3) |      |
|     (1,0)    || ^^    | (1,3) |      |


|:-----:|:-----:|:-----:|:-----:| ---- |
| (0,0) | (0,1) | (0,2) | (0,3) |      |
|     (1,0)           ||| (1,3)       ||


|:-----:|:-----:|:-----:|:-----:| ---- |
| (0,0) | (0,1) | (0,2) | (0,3) |      |
|     (1,0)           ||| ^^    |      |

|:-----:|:-----:|:-----:|:-----:| ---- |
| (0,0) | (0,1) | (0,2) | (0,3) |      \
|     (1,0)           ||| ^^    |      |


## Table

| Stage | Direct Products | ATP Yields |
| ----: | --------------: | ---------: |
|Glycolysis | 2 ATP                   ||
|^^         | 2 NADH      | 3--5 ATP   |
|Pyruvaye oxidation | 2 NADH | 5 ATP   |
|Citric acid cycle  | 2 ATP           ||
|^^                 | 6 NADH | 15 ATP  |
|^^                 | 2 FADH | 3 ATP   |
|                        30--32 ATP  |||


{:color-style: style="background: black;" }
{:color-style: style="color: white;" }
{:font-style: style="font-weight: 900; text-decoration: underline;" }

|:             Here's a Inline Attribute Lists example                 :||||
| ------- | ------------------------- | -------------------- | ----------- |
|:       :|:  <div style="color: red;"> &lt; Normal HTML Block > </div> :|||
| ^^      |   Red    {: .cls style="background: orange" }                |||
| ^^ IALs |   Green  {: #id style="background: green; color: white" }    |||
| ^^      |   Blue   {: style="background: blue; color: white" }         |||
| ^^      |   Black  {: color-style font-style}                          |||


[cell image]: https://jekyllrb.com/img/octojekyll.png "An exemplary image"

| Heading            | Column 1      | Column 2                           |
|--------------------|---------------|------------------------------------|
| Row 1              | Apple[^1]     | [Youtube (Home)]                   |
| Row 2              | Banana        | [Github][1]                        |
| Row 3 (merged)     | Blueberry     | [Google] *****  [Github]           |
| ^^         | [Plum](https://example.com) | Raspberry ![example][cell image]   |
| Row 4      | <https://www.google.com>    |  [test](https://www.google.com){:target="_blank"}                            |
|^^          |^^ <https://www.youtube.com> |                              |
| Row 5      | <https://www.google.com>                                  ||

[Youtube (Home)]: https://www.youtube.com
[Google]: https://www.google.com
[Github]: https://www.github.com
[1]: https://www.github.com
[^1]: Footnote

<https://www.google.com>

Not in table: `<Mail Gateway>`

In table:

Decision Point | Design Decision
--- | ---
Authoritative DNS MX Record | `<Mail Gateway>`

9 \* 9

| 1 \* 1 = 1 |
| 1 \* 2 = 2 | 2 \* 2 = 4 |
| 1 \* 3 = 3 | 2 \* 3 = 6 | 3 \* 3 = 9  |
| 1 \* 3 = 3 | 2 \* 3 = 6 | 3 \* 4 = 12 | 4 \* 4 = 16 |



## Mathjax

$\LaTeX{}$

## PlantUML

@startuml
Bob -> Alice : hello
@enduml

## Mermaid

```mermaid!
graph LR
  concurrent.futures --->| on top of | threading
  concurrent.futures --->| on top of | multiprocessing
  threading --->| on top of | \_thread
  click concurrent.futures "https://docs.python.org/3.9/library/concurrent.futures.html" _blank
```

## Video

![Flower](https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm)

![](//www.youtube.com/watch?v=Ptk_1Dc2iPY)

![](https://avatars3.githubusercontent.com/hubot?v=3&amp;s=40)

[\[video link\]](//www.youtube.com/watch?v=Ptk_1Dc2iPY)

## Audio

[HTML5 Audio Formats Test](https://hpr.dogphilosophy.net/test/)

Opus Audio (".opus"):

![1](https://hpr.dogphilosophy.net/test/opus.opus)
"MP3" file (".mp3") :
![2](https://hpr.dogphilosophy.net/test/mp3.mp3)

WebM Audio (".weba"):
![3](https://hpr.dogphilosophy.net/test/weba.weba)

WebMv2 Audio (".webm"):

![](https://hpr.dogphilosophy.net/test/webmv2.webm)

Ogg Vorbis (".ogg") :

![](https://hpr.dogphilosophy.net/test/ogg.ogg)

"wave" file(".wav") :

![](https://hpr.dogphilosophy.net/test/wav.wav)

FLAC file (".flac") :

![](https://hpr.dogphilosophy.net/test/flac.flac)

CAF file (".caf") :

![](https://hpr.dogphilosophy.net/test/cafopus.caf)

Spotify Podcast:

![](https://open.spotify.com/episode/2sXXGexCXPhGsdf9l99Q73?si=717c6671590745b3)

## Special media links

Local video file (".webm"):

![]({{ "/assets/videos/devstories.webm" | relative_url }})

Video with custom thumbnail:

[![w:1100](https://i.imgur.com/bc9HOJU.png)](https://www.youtube.com/watch?v=kCHGDRHZ4eU)

Tips:
* Use pipes {% raw %}(`|`){% endraw %} to delineate columns, and dashes to delineate the header row from the rest of the table.
* Spacing doesn't matter to the markdown processor, any extra white space is removed, but it can really help with readability.
The two markdown examples below both create this table.

Use pipes `{% raw %}(`|`){% endraw %}` to delineate columns, and dashes to delineate the header row from the rest of the table.


[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
