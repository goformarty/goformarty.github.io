---
layout: default
title: Daily
permalink: /daily/
published: true
---

## 100 Words Daily
100 words about what I've learned today

---
##### 28 June 2017
### Class body and method definitions

- The body of the class is the part that is in curly brackets { … } . This is where we define class members, such as **methods** or **constructor**.
- Class body is executed in **strict mode**.
- The **constructor** method is a special method for creating and initialising an object created with a class. There can only be **one** special method with the name "constructor" in a class.
- A constructor can use the **super** keyword to call the constructor of a parent class.

```
class Cat {
  constructor(name, colour) {
    this.name = name;
    this.colour = colour;
  }
```

---

##### 26-27 June 2017
### JavaScript classes

JavaScript classes (introduced in ECMAScript 2015) are primarily syntactical sugar over JavaScript's existing prototype-based inheritance. They simply offer a much nicer, cleaner and clearer syntax for creating these objects and dealing with inheritance.

Classes (as shipped in Chrome) support prototype-based inheritance, constructors, super calls, instance and static methods.

The class syntax has two components: **class expressions** and **class declarations**.

#### 1. Class declarations:
To declare a class, you use the class keyword with the name of the class  
```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
```

**NOTE:**
An important difference between function declarations and class declarations is that function declarations are hoisted and class declarations are not.
```
var p = new Persone(); // ReferenceError
class Person {}
```

#### 2. Class expressions
Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body.
```
// unnamed
var Person = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};
```
```
// named
var Person = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};
```
**NOTE:**
Class expressions also suffer from the same hoisting issues mentioned for Class declarations.
