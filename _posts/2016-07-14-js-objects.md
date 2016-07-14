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

#### The _new_ keyword
As you can see, the object constructor is just a normal function. However, the important part is the _new_ keyword, used when creating a new object instance of the constructor, which then returns the instance. Without it, you'll have a normal function, which returns nothing (actually, _undefined_), and sets the constructor properties on the window object (overwriting any window property of the same name).
<script src="https://jsfiddle.net/lthr/cg4akrom/3/embed/js,result/"></script>

If you haven't included `'use strict'` in your file, you won't even get an error about this.

## Properties
A property on an object is more than just a name and a value. You can see those by using the property descriptor method.
<script src="https://jsfiddle.net/lthr/t5p3uus8/3/embed/js,result/"></script>

#### Writable
With `writable` you can set whether it's possible to change the initial value or not. You can define this with the define property method.
<script src="https://jsfiddle.net/lthr/7ze158dm/2/embed/js,result/"></script>

If you use `'use strict';` in your file, you'll get a `TypeError: Cannot assign to read only property 'name' of object` error on trying to change the name, otherwise silence.

#### Enumerable
With `enumerable` you can _hide_ the property from the object, which can be useful if you fx don't want to include it in a loop.
<script src="https://jsfiddle.net/lthr/v3Ldutwa/2/embed/js,result/"></script>
