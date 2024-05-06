---
layout: post
title: Markdown Example
subtitle: Each post also has a subtitle
categories: example
tags: 
    - markdown 
    - example
---

This note demonstrates some of what [Markdown][1] is capable of doing.
[1]: https://daringfireball.net/projects/markdown/


You can write regular [markdown](https://markdowntutorial.com/) here and Jekyll will automatically convert it to a nice webpage.  I strongly encourage you to take 5 minutes to learn how to write in markdown- it'll teach you how to transform regular text into bold/italics/headings/tables/etc.


## An exhibit of Markdown


*Note: Feel free to play with this page. Unlike regular notes, this doesn't automatically save itself.*

## Basic formatting

Paragraphs can be written like so. A paragraph is the basic block of Markdown. A paragraph is what text will turn into when there is no reason it should become anything else.

Paragraphs must be separated by a blank line. Basic formatting of *italics* and **bold** is supported. This *can be **nested** like* so.


### Emoji

:+1:
:smile:


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
[3]: https://www.markitdown.net/

## Images
How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){.:block_center}

It can also be centered!
<div align=right>
<img src=https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg />
</div>

## Horizontal rule

A horizontal rule is a line that goes across the middle of the page.

---

It's sometimes handy for breaking things up.


## Table

Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | :smile: | $^b$ |
| Ten[^footnote1] | Eleven | Nine |
| <https://www.google.com>   | Eight |  ![example][cell image]  |
| [Plum](https://example.com) | $\lambda^a$| $$O_3 + C_2H_2 \rightarrow $$ |

[cell image]: https://jekyllrb.com/img/octojekyll.png "An exemplary image"
[^footnote1]: Footnote content

<script>
|:-----:|:-----:|:-----:|:-----:|
| (0,0) | (0,1) | (0,2) | (0,3) |
|     (1,0)    || ^^    | (1,3) |
</script>



In table:

Decision Point | Design Decision
--- | ---
Authoritative DNS MX Record | `<Mail Gateway>`

## List

### Ordered list
1. Item 1
2. A second item
3. Number 3
4. Ⅳ

*Note: the fourth item uses the Unicode character for [Roman numeral four][2].*
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm

### Unordered list

* An item
* Another item
* Yet another item
* And there's more...




## Block

### Quote

> Here is a quote. What this is should be self explanatory. Quotes are automatically indented when they are used.


### Code

```
    Code blocks are very useful for developers and other people who look at code or other things that are written in plain text. As you can see, it uses a fixed-width font.
```

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


```html
<html>
  <head> </head>
  <body>
    <p>Hello, World!</p>
  </body>
</html>
```

Jekyll also offers powerful support for code snippets:

```Ruby
def print_hi(name)
puts "Hi, #{name}"
end
print_hi('Tom')  #=> prints 'Hi, Tom' to STDOUT.
```



{% highlight ruby %}
def print_hi(name)
puts "Hi, #{name}"
end
print_hi('Tom')  #=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}




And here is the same code yet again but with line numbers:
{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}



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




``` diff
+        'user_exists' => 'SELECT EXISTS(SELECT 1 FROM table ',
+        'get_users' => 'SELECT split_part(username, \'@\', 1) FROM tab',
+        'get_password_hash_for_user' => 'SELEC',
+        'set_password_hash_for_user' => 'UP',
```

Reload the Nginx:
``` console
$ sudo nginx -s reload
```





## Mathjax

`\LaTeX{}`

` a \* b = c ^ b `

`2^{\frac{n-1}{3}} `

$$ \int_a^b f(x)\,dx. $$

inline equation $a+b=c$ test。



## Video
<div align="center">
    <video width="320" height="240" controls autoplay>
        <source src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm" type="video/webm">
    </video>
</div>


<div align="center">
    <video width="500" height="350" controls autoplay>
        <source src="https://www.youtube.com/watch?v=Ptk_1Dc2iPY" >
    </video>
</div>





Local video file (".webm")
<div align="center">
    <video width="500" height="350" controls autoplay>
        <source src="/assets/videos/devstories.webm" >
    </video>
</div>


Video with custom thumbnail:
<div align="center">
    <video width="400" height="400" poster="https://i.imgur.com/bc9HOJU.png" controls>
            <source src="https://www.youtube.com/watch?v=kCHGDRHZ4eU" type="video/mp4">
        </video>
</div>





## Audio

HTML5 Audio Formats Test is [here](https://hpr.dogphilosophy.net/test/)


"MP3" file (".mp3") :
<audio controls>
  <source src="https://hpr.dogphilosophy.net/test/mp3.mp3" type="audio/mpeg">
</audio>

WebM Audio (".weba"):
<audio controls>
  <source src="https://hpr.dogphilosophy.net/test/weba.weba)">
</audio>


FLAC file (".flac") :
<audio controls>
  <source src="https://hpr.dogphilosophy.net/test/flac.flac">
</audio>




