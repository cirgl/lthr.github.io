---
layout: post
title: Embed fiddles in Github Pages
tags:
- fiddles
---

How to embed various fiddles in your GitHub Pages.


## Plunker
[Plunker](https://plnkr.co) stands out as one of the fiddle sites that let's you add more files, as well as having a zip download option. With various [parameters](https://ggoodman.gitbooks.io/plunker/content/embed.html) you can also define which content to see in the embedded view, though the console is not an option. The `deferRun` parameter however, is a very nice toggle, preventing preview panes from automatically running.

```html
<iframe style="width: 100%; height: 330px; border: 0;" 
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
```
<iframe style="width: 100%; height: 330px; border: 0;"
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
