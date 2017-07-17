---
layout: default
title: Daily
permalink: /daily/
published: true
---

## 100 Words Daily
100 words about what I've learned today

---

---


##### 13 July 2017
### When not to use global variables in JavaScript?

Global variables can work just fine as long as we are writing all the code ourself, and only for ourself.

But they can pose a problem when we want to make things modular and future-proof.

The primary reason why global variables are discouraged in JavaScript is because in Javascript all code share a single global namespace, also JavaScript has implied global variables ie. variables which are not explicitly declared in local scope are automatically added to global namespace.

In web pages there are very often more than one script used. If they use global variables, they can conflict with each other. The less they add to the global namespace, the smaller the risk is to conflict with other scripts.


---

##### 12 July 2017
### Readme Driven Development

Writing a Readme is absolutely essential to writing good software. By writing your Readme first you give yourself some pretty significant advantages:

- you’re giving yourself a chance to think through the project without the overhead of having to change code every time you change your mind about how something should be organized or what should be included in the Public API;
- you’ll also find that it’s much easier to write this document at the beginning of the project when your excitement and motivation are at their highest;
- if you’re working with a team of developers and everyone else on the team has access to this information before you’ve completed the project, then they can confidently start work on other projects that will interface with your code;

---

##### 10 July 2017
### JavaScript: multiple cases in Switch statement.

The switch statement evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case.

```
switch (expression) {
  case 'A':
    console.log(‘Great job!’);
    break;
  case 'B':
    console.log(‘Pretty good!’);
    break;
  case 'C':
    console.log(‘It’s OK, but you can do better’);
    break;
  case 'D':
    console.log(‘Not good');
    break;
  default:
    console.log(‘Sorry, we don’t have your results!’);
}
```

In JavaScript to assign multiple cases in Switch statement we have to define different case without the break. A matched case will run until a break (or the end of the switch statement) is found.
```
switch (expression)
{
   case "A":
   case "B":
   case "C":
       console.log(‘Test passed!’);
       break;

   default:
       alert(‘Test failed');
}
```

---

##### 5 July 2017
### Why to use Virtual Machine?

Why would you want to run a virtual machine on your computer? Plenty of reasons:

- Web sites that don't play nice with the operating system you're running;
- You like using one OS, but need just an app or two from another running in their natural environments, a light-on-resources game, or maybe even some uber-cool Linux app;
- You want to try out some new software, but would rather not chance it mucking up the pretty decent system you've got right now;
- You're intrigued at the idea of trying out a Linux desktop, but the word "partitioning" doesn't sound like how you want to spend a Saturday afternoon;

---



##### 4 July 2017
### What's virtualisation software?

Virtualisation software allows a single host computer to create and run one or more virtual environments.

The entire operating system (the "guest") runs on another OS (the "Host"), whether in a container window, or full-screen, or in what's sometimes called a "seamless" mode, where just one application is run from the "guest".

We can host of multiple virtualised environments within a single OS instance.

Virtual machines do not require specialised, hypervisor-specific hardware. Virtualisation does, however, require more bandwidth, storage and processing capacity than a traditional server or desktop if the physical hardware is going to host multiple running virtual machines. Because VMs on a physical host can consume unequal resource quantities - one may hog the available physical storage, while another stores little - we must balance VMs with available resources.

---


##### 3 July 2017
### Why use MAMP?

MAMP has many uses and benefits. It allows you to:

- Develop and design your site locally—no need to worry about “breaking” the live site by testing out a few changes;
- Build sites you don’t want the world to see (since search engines can’t index your local site);
- Work in a faster development environment (because it doesn’t rely on an internet connection and communicating with a web server);
- Work offline (great for trips on airplanes);
- Use the local install as a partial backup of your existing site;
- Develop sites in a secure environment (again, because MAMP sites are not online, it makes it basically impossible to be hacked or have some other kind of security breach);

---


##### 30 June 2017
### What is MAMP?

**MAMP** stands for **Macintosh, Apache, MySQL and PHP**. Basically, it is a free application you can install on your Mac laptop or desktop computer that gives you access to a local Apache server.

Here is a breakdown of the four components of MAMP:

**Macintosh**: an operating system
**Apache**: an open source web server
**MySQL**: most widely available relational database in the world (all WordPress sites use MySQL databases)
**PHP**: server-side scripting language (which WordPress sites run on)

When these four components come together, they create a local web server on your computer only. That means you can build entire websites and see what they would look like online without being connected to the Internet.


---

##### 29 June 2017
### What is Agile?

Agile is a time boxed, iterative approach to software delivery that builds software incrementally from the start of the project, instead of trying to deliver it all at once near the end.

It works by **breaking projects down** into little bits of user functionality called **user stories**, **prioritising** them, and then continuously delivering them in short two week cycles called **iterations**.

How Agile is different from the traditional approach?

1. **Analysis, design, coding, and testing are continuous activities** - as long as there are features to build, and the means to deliver them, these activities continue for the duration of the project.
2. **Development is iterative** - that means starting with something really simple, and adding to it incrementally over time.
3. **Planning is adaptive** - when reality disagrees with their plans, it can be easier to change plans than reality.
4. **Roles blur** - people pitch in and do whatever it takes to make the project successful—regardless of title or role.
5. **Scope can vary** - by fixing time, budget, and quality, and being flexible around scope, Agile team's maintain the integrity of their plans, work within their means, and avoid the burnout, drama, and dysfunction traditionally associated with our industry.
6. **Requirements can change** - Agile believes the cost of change can be relatively flat, accepts and embraces change even late in the delivery process.



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
