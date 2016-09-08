---
layout: post
title: Real World Code Snippets
tags:
- code
- fun
---

Here's some real world code snippets I've ran across.


#### Uppercase spacing
```javascript
  name: key.toUpperCase().replace(' ', '_')
```

#### If `true` then `true`
```javascript
  this.isCustomerLookedUp = this.customerId && this.countryCode ? true : false;
```
