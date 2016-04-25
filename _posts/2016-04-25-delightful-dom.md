---
layout: post
title: Delightful DOM
tags:
- dom
- jquery
---

## Show links with full URL (on a jQuery page)

From the browser, press F12. Go to the Console, paste below code:

```html
$('<style type="text/css">a:after{content:" ("attr(href)") ";}</style>').appendTo(document.head);
```
