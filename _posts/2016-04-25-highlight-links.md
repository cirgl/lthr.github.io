---
layout: post
title: Add URL from links to links on a jQuery page
tags:
- dom
- jquery
---

From the browser, press F12. Go to the Console, paste below code:

```html
$('<style type="text/css">a:after{content: " ("attr(href)") ";}</style>').appendTo(document.head);
```
