---
layout: default
title: Daily
permalink: /daily/
published: true
---

## 100 Words Daily
100 words about what I've learned today

---

##### 29 June 2017
### What is Agile?

Agile is a time boxed, iterative approach to software delivery that builds software incrementally from the start of the project, instead of trying to deliver it all at once near the end.

It works by **breaking projects down** into little bits of user functionality called **user stories**, **prioritising** them, and then continuously delivering them in short two week cycles called **iterations**.

How Agile is different from the traditional approach?

1. Analysis, design, coding, and testing are continuous activities - as long as there are features to build, and the means to deliver them, these activities continue for the duration of the project.
2. Development is iterative - that means starting with something really simple, and adding to it incrementally over time.
3. Planning is adaptive - when reality disagrees with their plans, it can be easier to change plans than reality.
4. Roles blur - people pitch in and do whatever it takes to make the project successful—regardless of title or role.
5. Scope can vary - by fixing time, budget, and quality, and being flexible around scope, Agile team's maintain the integrity of their plans, work within their means, and avoid the burnout, drama, and dysfunction traditionally associated with our industry.
6. Requirements can change - Agile believes the cost of change can be relatively flat, accepts and embraces change even late in the delivery process.



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
