---
layout: post
title: Use DOM to show full URL of all links
tags:
- dom
- jquery
---

From the browser, press F12. Go to the Console, paste below code:

## A jQuery page: 

```html
$('<style type="text/css">a:after{content: " ("attr(href)") ";}</style>').appendTo(document.head);
```
