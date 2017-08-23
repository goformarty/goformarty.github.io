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
##### 22 August 2017
### Angular 2 Components: Inputs and Outputs


In Angular, a component can receive data from its parent as long as the receiving component has specifically said it is willing to receive data. Similarly, components can send data to their parents by trigger an event the parent listens for.

Angular passes the data to the @Component decorator to implement the downward and upward flow of data: “inputs” and “outputs.”

“Inputs” specifies which properties we can set on a component whereas “outputs” identifies the events a component can fire to send information up the hierarchy to its parent.

@Input() and @Output() is Angular’s syntax to to define input properties and output events in a component.

---

##### 21 August 2017
### What is the difference between private, public & protected inheritance?

when to use each of access modifiers

```
class Base {
    public:
        int publicMember;
    protected:
        int protectedMember;
    private:
        int privateMember;
};
```
- Everything that is aware of Base is also aware that Base contains publicMember.
- Only the children (and their children) are aware that Base contains protectedMember.
- No one but Base is aware of privateMember.
 The same happens with public, private and protected inheritance. Let's consider a class Base and a class Child that inherits from Base.

If the inheritance is public, everything that is aware of Base and Child is also aware that Child inherits from Base.
If the inheritance is protected, only Child, and its children, are aware that they inherit from Base.
If the inheritance is private, no one other than Child is aware of the inheritance.

---

##### 17-18 August 2017
### Object Oriented Programming vs Functional Programming

Both OOP and FP have the shared goal of creating understandable, flexible programs that are free of bugs. But they have two different approaches for how to best create those programs.

Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects", which are data structures that contain data, in the form of fields, often known as attributes; and code, in the form of procedures, often known as methods.

Functional programming is a programming paradigm, a style of building the structure and elements of computer programs, that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

In all programs, there are two primary components: the data and the behaviours. 
OOP says that bringing together data and its associated behaviour in a single location (called an “object”) makes it easier to understand how a program works. 

FP says that data and behaviour are distinctively different things and should be kept separate for clarity.

Object-oriented languages are good when we have a fixed set of operations on things, and as our code evolves, we primarily add new things. This can be accomplished by adding new classes which implement existing methods, and the existing classes are left alone.

Functional languages are good when we have a fixed set of things, and as our code evolves, we primarily add new operations on existing things. This can be accomplished by adding new functions which compute with existing data types and the existing functions are left alone.

---

##### 16 August 2017
### Why to use map, filter and reduce in Javascript?

In 2011, JavaScript introduced **map, reduce, and filter** as powerful alternatives when translating elements, finding cumulative values, or building subsets based on conditions.

##### Drawbacks of looping
```
for(let i = 0; i < array.length; i++) {
    if(array.indexOf(array[i]) === i) {
        models.push(array[i]);
    }
}
```

We needed to check **5 pieces of information** to determine what was going on. And this is a single for loop:
1. var i = 0
2. i < array.length
3. i++
4. array.indexOf(array[i]) === i
5. models.push(…)

##### A Functional Approach:
This same effect could be written using JavaScript’s built-in filter() method.
```
var uniqueProducts = array.filter(function(elem, i, array) {
        return array.indexOf(elem) === i;
    }
);
```

Compared to the looping approach above:
- Checking 1), 2), 3) is unnecessary because filter() does these automatically. - point 4) is the same but without the additional if(…) block
- point 5) - no need to check what our ***models*** even is, if it already has data or targets specific data types. Filter method solves this problem by not depending on code outside the callbacks, called side-effects

---

##### 15 August 2017
### Data types: JavaScript & Typescript


TypeScript is a language that adds object-oriented syntactical sugar to JavaScript.

In JavaScript we don't annotate types, and we can assign values of different types to the same variables through the lifetime of our program.

As far as we're concerned, if an object has the properties and methods we need it to, we don't care what the underlying type is. If it behaves properly, it's good enough. This is sometimes called duck-typing: If it walks like a duck, and it quacks like a duck, it's probably okay if we treat it like a duck.

Typescript however is  statically typed. In a statically typed language, variables, parameters, and members of objects (JavaScript calls them properties) have types that the compiler knows at compile time. The compiler can use that information to perform type checks and to optimize the compiled code.

In general, types are a way of classifying data structures based on the kind of information they can contain, and what you can do with it.

##### Types in JavaScript

In JavaScript, clause 6 of the ECMAScript specification defines the following types:

- Undefined;
- Null;
- Boolean;
- String;
- Symbol;
- Number;
- Object.

##### Basic Types in Typescript

TypeScript exposes nine types for us to work with. Whether you use them or not is up to you: Type annotations are always optional in TypeScript.

- Boolean;
- Number;
- String;
- Array;
- Tuple;
- Enum;
- Any;
- Void;
- Function.

---

##### 14 August 2017
### How to name variables, methods and classes?

The name of a variable, function, or class should explain **why it exists**, **what it does** and **how it is used**. If a name requires a comment to understand it, then the name does not reveal its intent and it should be changed.
```
const ms;
```

The name here reveals nothing, and it would be clearer to name our variable for example:
```
const metrePerSecond
```

##### Method names

- Methods should have verb or verb-phrase names, like deletePage or save.
Accessors and mutators, and their predicates, should be named according to JavaBean standards.

##### Class names
- Classes and objects should have noun or noun-phrase names, like Customer, WikiPage, Account and AddressParser.
- But avoid names like Manager, Processor, Data or Info in the name of a class.
- A class name should not be a verb.

---

##### 11 August 2017
### JavaScript static methods

##### Syntax:
```
static methodName() { ... }
```
The **static** keyword defines a static method for a class.

##### Description:
Static method calls are made directly on the class and are not callable on instances of the class. Static methods are often used to create utility functions.
- We define the function **directly on the object, not on its prototype**.
- We **never access** the **this** keyword inside the function.
- We **return a value** from the function.


##### Example:
```
class Double {
  static double(n) {
    if (n === undefined) {
      n = 1;
    }
    return n * 2;
  }
}

console.log(Double.double(5));        // 10

const anotherDouble = new Double();
console.log(anotherDouble.double());
// 'anotherDouble.double() is not a function’
```

---

##### 10 August 2017
### How to rename a local and remote branch in git


##### Step 1:
##### Rename your local branch

- If you are on the branch you want to rename: 
``` 
git branch -m new-name 
```

- If you are on a different branch:
``` 
git branch -m old-name new-name
```

The above command will change your branch name, but you have to be very careful using the renamed branch, because it will still refer to the old upstream branch associated with it, if any.

##### Step 2:
##### Delete the old-name remote branch and push the new-name local branch.
``` 
git push origin :old-name new-name
```

##### Step 3:
##### Reset the upstream branch for the new-name local branch.

Switch to the branch and run:
``` 
git push origin -u new-name
```

---

##### 9 August 2017
### What is a helper function?


We use helper functions to reduce the complexity within the other functions.



Essentially, there is little difference between the structure of a helper function and other functions, though they should be small and generic.

```
function isValid(number) {
	return (isWithinRange(number) && isEven(number));
}

// our two helper functions here:
function isWithinRange(number) {
return ((number > 0) && (number < 10));
}

function isEven(number) {
  return (number%2 === 0);
}

isValid(4); // true
isValid(0); // false
isValid(9); // false
```

---

##### 31 July 2017
### Git - how to fix the last commit message?


##### Scenario:
You've just ran:

```
git commit -m "Fixed logn ug #04"
```
Your last commit message says "Fixed logn ug #04". You haven't pushed it yet and you want to remove the typos.

##### How to undo?

```
git commit --ammend
```
or
```
git commit --ammend "Fixed login bug #04"
```

##### How it works?
**git commit - - ammend** updates and replaces the most recent commit with a new commit that combines any staged changes with the contents of the previous commit. And if nothing more has been staged yet, this just rewrites the previous commit message.

---


##### 21 July 2017
### Scrum events - part 5: Team review (show and tell)


The team review is a regular meeting which gives team members the opportunity to demonstrate their work. It can also be called a sprint review or a show and tell.

Stakeholders like directors or suppliers might be invited to this meeting to hear more about the completed user stories or other work that has beed done in the last sprint.

The purpose of the “show and tell” is to present the demo that lets different developers demonstrate features. A typical agenda for an individual developer presenting would include:
 - Describing the purpose of the feature. In terms of sprint goal, user stories, etc.
 - Showing how the system looks before the change.
 - Showing how the system looks after the change.


The “show and tell” meeting is a great opportunity for the Scrum team to shine together and showcase the results of their hard work.

---

##### 20 July 2017
### Scrum events - part 4: Sprint Retrospective

Retrospectives, sometimes called ‘retros’, are regular meetings where the whole team talks about what’s going well and what isn’t.

Teams usually hold retros at the end of an iteration (for example a sprint) and use them to talk about the work from that period of time.

The point of a retro is to fix any problems in the team and to make sure you keep doing the things that are working.

A basic retro could follow these steps:

1. The host explains the questions at the beginning and sticks a post-it note to the wall for each question.
2. Each team member writes down one or more answers for each question on post-it notes and sticks them to the right part of the wall.
3. The group discusses issues as they come up, or at the end.
4. The host decides on actions to fix any problems raised, and assigns them to members of the team.

---

##### 19 July 2017
### Scrum events - part 3: Sprint Review

At the end of each sprint a Sprint Review meeting is held. During this meeting the Scrum Team shows which Scrum Product Backlog items they completed (according to the Definition of Done) during the sprint. This might take place in the form of a demo of the new features.

It is important to notice that Backlog items that are not completed shall not be demonstrated. Otherwise this might suggest that these items are finished as well. Instead incomplete items/remaining activities shall be taken back into the Scrum Product Backlog, re-estimated and completed in one of the following sprints.

Participants in the sprint review typically include the Scrum Product Owner, the Scrum Team and the Scrum Master. Additionally management, customers, and developers from other projects might participate as well.

---

##### 18 July 2017
### Scrum events - part 2: Sprint planning


At a sprint planning meeting, the team decides what to work on next and how they’ll do it. This plan is created by the collaborative work of the entire Scrum Team.

#### Topic One: What can be done this Sprint?
The Development Team works to forecast the functionality that will be developed during the Sprint. . The number of items selected from the Product Backlog for the Sprint is solely up to the Development Team. Only the Development Team can assess what it can accomplish over the upcoming Sprint.

#### Topic Two: how will the chosen work get done?
Work planned for the first days of the Sprint by the Development Team is decomposed by the end of this meeting, often to units of one day or less.
The Product Backlog items selected for this Sprint plus the plan for delivering them is called the Sprint Backlog.


#### Sprint Goal
Sprint Goal is created during the Sprint Planning meeting. It is an objective set for the Sprint that can be met through the implementation of Product Backlog.

---

##### 17 July 2017
### Scrum events - part 1: Sprint

The Sprint is the heart of Scrum. It is a short, consistent cycle no longer than four weeks. The goal is to have an iteration short enough to keep the team focused but long enough to deliver a meaningful increment of work. The iterations enable the team to quickly gather feedback and continue to adapt and improve over time.

During the Sprint a short daily Standup-Meeting (Daily Scrum Meeting) is held to update the status of the items and to help self-organisation of the team.

Sprints begin and end on fixed dates and changes can be made to the Sprint Backlog that would endanger the Sprint Goal. No additional work should be brought into the Sprint unless the Sprint Goal has been reached or a feature emerges of such high value it must be brought into Sprint.

---

##### 13-14 July 2017
### How to reduce global variables in JavaSctipt?

1) One way to reduce global variables is to use the YUI module pattern. The basic idea is to wrap all your code in a function that returns an object which contains functions that needs to be accessed outside your module and assign the return value to a single global variable.

```
var FOO = (function() {
    var my_var = 10; //shared variable available only inside your module

    function bar() { // this function not available outside your module
        alert(my_var); // this function can access my_var
    }

    return {
        a_func: function() {
            alert(my_var); // this function can access my_var
        },
        b_func: function() {
            alert(my_var); // this function can also access my_var
        }
    };

})();

```

Now to use functions in your module elsewhere, use FOO.a_func(). This way to resolve global namespace conflicts you only need to change the name of FOO.

2) We can also start with one global: myApp = {}; Everything should be in that. The only exception would be our AJAX library (there are some extreme exceptions like working with JSONP callbacks).

There should be very few properties in myApp. We'll want to hold our application properties in containers such as config or settings.

```
myApp = {
    config:{
        prop:1
    },
    settings:{
        prop:2
    },
    widgets:{
        List: function(props){},
        Item: function(props){}
    }
}

```


---

##### 12 July 2017
### When not to use global variables in JavaScript?

Global variables can work just fine as long as we are writing all the code ourself, and only for ourself.

But they can pose a problem when we want to make things modular and future-proof.

The primary reason why global variables are discouraged in JavaScript is because in Javascript all code shares a single global namespace, also JavaScript has implied global variables ie. variables which are not explicitly declared in local scope are automatically added to global namespace.

In web pages there are very often more than one script used. If they use global variables, they can conflict with each other. The less they add to the global namespace, the smaller the risk is to conflict with other scripts.


---

##### 11 July 2017
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
TClass expressions also suffer from the same hoisting issues mentioned for Class declarations.
