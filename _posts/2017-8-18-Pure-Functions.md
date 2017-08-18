---
layout: post
title: What are pure functions, side-causes and side-effects?
published: true
---


A function is a process which takes some **input**, called arguments, and produces some **output** called a return value. 

A **pure function** forms the foundation of functional programming.

A **pure function** is a function which:
- Given the same input, will **always return the same output**.
- Doesn’t depend on and doesn’t modify the states of variables out of its scope
- Relies on **no side-causes** - hidden inputs.
- Produces **no side effects** - hidden outputs.

### What are side-causes and side-effects?

Side-causes and side-effects are hidden inputs and hidden outputs. Let’s take a look at this example:

*Example 1*


```
arr = [];
let a = 2;
let b = 1;

function impureFunction () {
  a = a * b + 2;
	if(a > 3) {
		arr.push(a);
	}
}

impureFunction();

```

According to the syntax, this function **takes no inputs and returns no output**, and yet it’s obviously depending on something, and it’s obviously doing something. 

The fact is, it has a hidden set of inputs and outputs. 
The **hidden inputs** are variables a and b, and the **hidden output** is adding a new element to the end of the arr array.


Let’s have a look at another example:

*Example 2a*

```
function getCurrentProgram (guide, channel) {
  let schedule = guide.getSchedule(channel);

  let current = schedule.programAt(new Date());

  return current;
}

```
This function has a hidden input of the current time (new Date()). We can surface this complexity by just being honest about this extra input:

*Example 2b*
```
function getCurrentProgram (guide, channel, date) {
  let schedule = guide.getSchedule(channel);

  let current = schedule.programAt(date);

  return current;
}
```

This function now has no hidden inputs (or outputs).


##### What are the problems with side-causes/side-effects?


1. **TDD**

We cannot test impure function in isolation. We can’t just plug into its inputs and check its outputs. We have to break open the code, figure out its hidden causes and effects, and simulate the world it’s supposed to exist in.

*Example 2b* is much easier to test than *Example 2a*. 
Testing different times of day will all be straightforward,because we can pass in any time we like.

2. **Debugging**

This effect is amplified for debugging. If a function doesn’t allow side-effects (or side-causes), we can understand whether it’s correct just by giving it some inputs and checking the outputs. But a function with side-effects there’s no upper-limit to how many other parts of the system we’ll have to consider. When it’s allowed to depend on anything, and cause anything, then the bugs could be anywhere.


##### Why to use Pure Functions?

Pure functions are completely independent of outside state, and as such, they are immune to entire classes of bugs that have to do with shared mutable state. Their independent nature also makes them great candidates for parallel processing across many CPUs, and across entire distributed computing clusters, which makes them essential for many types of scientific and resource-intensive computing tasks.

Pure functions are also extremely independent — easy to move around, refactor, and reorganise in your code, making your programs more flexible and adaptable to future changes.

