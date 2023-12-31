---
layout: post
parent: Markdown
title: Testing markdown bibliography and link references
date: 2023-06-18
last_modified_date: 2023-06-18
nav_order: 1
---

I am very familiar with listing references throughout an article. Then it is easy to refer to the same source, if needed. What are the options here? Let's experiment.

# Version 1 markdown: proper bibliography

```
Main text: [^1] ... [^2] ... and so on
Bottom: 
[^1]: Source 1 text and links
[^2]: Source 2
```

A reference is created if I type `[^1]` in the main text as a link to the bibliography list at the bottom. There, the reference as `[^1]: Source`. I don't have to keep track of the number sequence, markdown function will figure out the list at the end.

The cool thing about this is that the bibliography has an arrow at the end of each reference pointing back to main text where it was used (first?). Pretty convenient for long documents to avoid all that scrolling back and forth.

Example: in the main text my reference [^2] and reference [^1]. The page will number all references and produce a list at the end.

# Version 2 with just links - not for bibliography, just convenience

Does it work as the example in the [markdown guide](https://www.markdownguide.org/basic-syntax/#reference-style-links)?

Main text reference: `[hobbit hole][2]`. And that becomes: [hobbit hole][2]. But now that `[2]` can be any string, as long as at the bottom I include just the link, with maybe a title so it looks like `[2]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles I"`. Now the `[hobbit hole]` above becomes a link to wikipedia.

Or I could skip the two parts and just type `[hobbit hole]` by itself in main text. Then on the bottom define it as `[hobbit hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles II"`. That works, too: renders as [hobbit hole] and works as a link.

**Note**: the "title" above just means that text will pop up when hovering over the link. It can be added to the inline regular link as well: `[link with title](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles III")`. Rendered look: [link with title](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles III"). 

[2]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles I"

[hobbit hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles II"

# Reference list from version 1 at page bottom

[^1]: After a colon and a space, the reference text and/or link goes here. (becomes ref 1 - used first in main text). Source for this: [kramdon](https://kramdown.gettalong.org/quickref.html#footnotes).
[^2]: After a colon and a space, the reference text and/or link goes here. (becomes ref 1 - used first in main text)

