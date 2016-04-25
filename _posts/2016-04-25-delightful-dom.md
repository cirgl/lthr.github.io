---
layout: post
title: Delightful DOM
tags:
- dom
---

## Show links with full URL

From the browser, open the developer tools (press <kbd>Command</kbd>+<kbd>Alt</kbd>+<kbd>J</kbd> (Mac) or <kbd>F12</kbd> (Windows)). Go to the Console, paste below code:

### Show links with full URL on a page with jQuery

```javascript
$('<style type="text/css">a:after{content:" ("attr(href)") "}</style>').appendTo(document.head);
```

### Show links with full URL on a page without jQuery

```javascript
var css = 'a:after{content:" ("attr(href)") "}',
    head = document.head || document.getElementsByTagName('head')[0],
    style = document.createElement('style');
style.type = 'text/css';
if (style.styleSheet){
  style.styleSheet.cssText = css;
} else {
  style.appendChild(document.createTextNode(css));
}
head.appendChild(style);
```