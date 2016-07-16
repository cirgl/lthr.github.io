---
layout: post
title: Embedding fiddles
tags:
- fiddles
---

This post is a guide in how to embed various fiddles into your GitHub Pages posts (and other pages).

## JS Bin
[JS Bin](http://jsbin.com) will only let you have one JavaScript, one HTML and one CSS editor window, unlike eg. Plunker which lets you have as many as you'd like. The embedded output options are quite easy though, just click the `share` button and set your options. Another useful thing is the option to choose console as one of the embedded view outputs.

```html
<a class="jsbin-embed"
  href="http://jsbin.com/yubiro/2/embed?js,console">
    Hello JS Bin! on jsbin.com
</a>
<script 
  src="http://static.jsbin.com/js/embed.min.js?3.37.0"></script>
```
<a class="jsbin-embed" href="http://jsbin.com/yubiro/2/embed?js,console">Hello JS Bin! on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.37.0"></script>

## Plunker
[Plunker](https://plnkr.co) stands out as one of the fiddle sites that let's you add more files, as well as having a zip download option. With various [parameters](https://ggoodman.gitbooks.io/plunker/content/embed.html) you can also define which content to see in the embedded view, though the console is not an option. The `deferRun` parameter however, is a very nice toggle, preventing preview panes from automatically running.

```html
<iframe style="width: 100%; height: 330px; border: 0;" 
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
```
<iframe style="width: 100%; height: 330px; border: 0;"
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
