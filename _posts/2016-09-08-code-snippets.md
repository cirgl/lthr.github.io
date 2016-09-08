---
layout: post
title: Code Snippets
tags:
- code
- fun
---

Here's some code snippets I've run into.


##### Uppercase spacing, just to be sure
```
  name: key.toUpperCase().replace(' ', '_')
```

##### If true then true, otherwise.. false
```
  this.isCustomerLookedUp = this.customerId && this.countryCode ? true : false;
```

##### Typo that passed code reviews
```
  <span ng-show="a.foreignCurrency" class="badge foreign-furrency" ng-bind="a.foreignCurrency"></span>
```
  
