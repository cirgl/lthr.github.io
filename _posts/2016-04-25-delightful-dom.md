---
layout: post
title: Delightful DOM
tags:
- dom
---

## Show links with full URL (on a jQuery page)

From the browser, open the developer tools (press <kbd>Command</kbd>+<kbd>Alt</kbd>+<kbd>J</kbd> (Mac) or <kbd>F12</kbd> (Windows)). Go to the Console, paste below code:

```html
$('<style type="text/css">a:after{content:" ("attr(href)") ";}</style>').appendTo(document.head);
```
