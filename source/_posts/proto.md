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
  SuperClass(this);
  this.otherValue = 'bar';
}

SubClass.prototype = Object.create(SuperClass.prototype);
SubClass.prototype.constructor = SubClass;

var a = new SuperClass();
var b = new SubClass();
~~~~

and you inspect the variable "b", you will find that it has \_\_proto\_\_ property that is an instance of Superclass. This is actually a reference to Subclass.prototype. 

~~~~
b.__proto__ === SubClass.prototype; //returns true
~~~~
Nearly everything in Javascript has a \_\_proto\_\_ property that allows you to access the prototype of its constructor.
<br>

A quick Google search of \_\_proto\_\_ brings us to a [MDN page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) with at least two scary-looking warnings about why we shouldn't be fiddling with \_\_proto\_\_, and that we would be better off using Object.getPrototypeOf() instead.

~~~
b.__proto__ === Object.getPrototypeOf(b); //returns true;
~~~
<br>


...
<br>



So what if we try b.\_\_proto\_\_.\_\_proto\_\_?

~~~~
b.__proto__.__proto__ === Object.prototype; //returns true

b.__proto__.__proto__ === Subclass.prototype.__proto__; //returns true too!
~~~~

We know that an object's \_\_proto\_\_ property is a reference to the prototype of its constructor. Moreover, in Javascript's implementation of prototypical inheritance, when you inherit the prototype of a superclass (line 10), you are creating an object
with a \_\_proto\_\_ property that references the superclass' prototype.

This is how a subclass is able to access the methods on its superclass' prototype!

This is especially useful if you are trying to find the methods on a Javascript class using Object.getOwnPropertyNames().

~~~~
//forgot which methods are available on a HTMLBodyElement?

document.getElementsByTagName('body')[0].__proto__; 

//returns the HTMLBodyElement prototype and its attributes
~~~~
<br>
In fact, \_\_proto\_\_ is just another method on a prototype. If you look at Object.prototype more closely,
~~~~
Object.getOwnPropertyNames(Object.prototype); //the __proto__ method lives here!
~~~~
you'll see that \_\_proto\_\_ is a property that is defined on Object.prototype, from which nearly everything in Javascript inherits.


