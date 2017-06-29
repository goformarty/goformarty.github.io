---
layout: default
title: Daily
permalink: /daily/
published: true
---

## 100 words daily


##### 26-27 June
### JavaScript classes

JavaScript classes introduced in ECMAScript 2015 are primarily syntactical sugar over JavaScript's existing prototype-based inheritance. They simply offer a much nicer, cleaner and clearer syntax for creating these objects and dealing with inheritance.

Classes (as shipped in Chrome) support prototype-based inheritance, constructors, super calls, instance and static methods.

The class syntax has two components: class expressions and class declarations.

Class declarations: To declare a class, you use the class keyword with the name of the class  
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

! NOTE: Hoisting

An important difference between function declarations and class declarations is that function declarations are hoisted and class declarations are not.

var p = new Persone(); // ReferenceError

class Person {}

2. Class expressions
Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body.

// unnamed
var Person = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

// named
var Person = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

! NOTE: Class expressions also suffer from the same hoisting issues mentioned for Class declarations.
