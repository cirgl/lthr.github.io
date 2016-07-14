---
layout: post
title: JavaScript Objects
tags:
- javascript
---

Some things about JavaScript objects.


## Basic objects
There are some different ways you can create JavaScript objects, each having their own purposes and benefits.
<script src="https://jsfiddle.net/lthr/6ppb41eq/1/embed/js,result/"></script>

## Object constructors
If we want to create multiple instances of an object, we can use object constructors to define a template. By convention, constructors are named with a capital letter.
<script src="https://jsfiddle.net/lthr/qz6dq6t2/5/embed/js,result/"></script>

### The _new_ keyword
As you can see, the object constructor is just a normal function. However, the important part is the _new_ keyword, used when creating a new object instance of the constructor, which then returns the instance. Without it, you'll have a normal function, which returns nothing (actually, _undefined_), and sets the constructor properties on the window object (overwriting any window property of the same name).
<script src="https://jsfiddle.net/lthr/cg4akrom/3/embed/js,result/"></script>

If you haven't included `'use strict'` in your file, you won't even get an error about this.

## Properties
