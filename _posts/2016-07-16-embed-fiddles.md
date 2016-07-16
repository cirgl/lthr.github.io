---
layout: post
title: Embedding fiddles
tags:
- fiddles
---

This post is a guide in how to embed various fiddles into your GitHub Pages posts (and other pages).

## JS Bin
[JS Bin](http://jsbin.com) will only let you have one JavaScript, one HTML and one CSS editor window, unlike eg. [Plunker](https://plnkr.co) which lets you have as many as you'd like. The embedded output options are quite easy though, just click the `share` button and set your options. Another useful thing is the option to choose console as one of the embedded view outputs. Also, the embedded view output height is per default supposed to be set as the height of the content, which is quite nice.. if it worked. I'm having trouble with this on GitHub Pages though, as you can see below (seems like the default minimum height of 300 pixels is enforced). In any case, you can overwrite this width and height though, if you want to control it manually. There are also other useful [parameters](http://jsbin.com/help/how-can-i-embed-jsbin) as well.

```html
<a class="jsbin-embed"
  href="http://jsbin.com/yubiro/4/embed?js,console">
    Hello JS Bin! on jsbin.com
</a>
<script 
  src="http://static.jsbin.com/js/embed.min.js?3.37.0"></script>
```
<a class="jsbin-embed" href="http://jsbin.com/yubiro/4/embed?js,console">Hello JS Bin! on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.37.0"></script>

## Plunker
[Plunker](https://plnkr.co) stands out as one of the fiddle sites that let's you add more files, as well as having a zip download option. With various [parameters](https://ggoodman.gitbooks.io/plunker/content/embed.html) you can also define which content to see in the embedded view, though the console is not an option. The `deferRun` parameter however, is a very nice toggle, preventing preview panes from automatically running. Since it runs in an iframe, you need to specify the width and height of the embedded view yourself.

```html
<iframe style="width: 100%; height: 330px; border: 0;" 
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
```
<iframe style="width: 100%; height: 330px; border: 0;"
  src="https://embed.plnkr.co/do7qbv/?show=script.js,preview&deferRun"></iframe>
