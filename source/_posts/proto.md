---
title: What is __proto__?
date: 2016-08-16 13:59:52
tags:
---

Javascript uses prototype chains to implement prototypical inheritance, and most Javascript examples that implement (psuedo)classical inheritance assign a class' prototype using Object.create(Super.prototype). 

If you run the following in the console:
~~~~
var SuperClass = function() {
  this.value = 'foo';
}

var SubClass = function() {
  Superclass(this);
  this.otherValue = 'bar';
}

SubClass.prototype = Object.create(SuperClass.prototype);
SubClass.prototype.constructor = SubClass;

var a = new SuperClass();
var b = new SubClass();
~~~~

If you inspect the variable 'b', you will find that it has '__proto__' property that is an instance of Superclass. This is actually a reference to Subclass.prototype.

~~~~
b === SubClass.prototype //returns true;
~~~~
