---
layout: post
title: Code Snippets
tags:
- code
- fun
---

Here's some code snippets I've run into.


##### Uppercase spacing, just to differentiate
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

##### What's that smell?
```
  // group by ISIN only when it is defined.
  // use a random value otherwise to avoid different
  // declared assets aggregation, for which ISIN is undefined.
  return sh.instrument.isin || Math.random();
```

  
