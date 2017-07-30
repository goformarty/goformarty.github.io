---
layout: post
title: Detroit school TDD
published: true
---


Detroit school TDD (sometimes called Chicago TDD)

If you only hear of one kind of Test-Driven-Development, it is this one.

### Name
The name comes from the Extreme Programming community in Detroit that developed the main ideas and principles behind it.

It is also sometimes called “Chicago style” or “Classical”, “Traditional” because it laid the foundation of most of the core concepts of TDD and wields significant influence on the common wisdom, documentation, training, and tools that support TDD (and as a result, modern automated software testing).

### What is it?

What distinguishes this school is the emphasis on a technique called triangulation.

In Detroit-school TDD, a public API is first identified by writing a test against it, then each successive test is written as an example of its use, which drives out additional requirements. At its most simple, its workflow is:

1. Write a failing test
2. Change the implementation to make it pass (or change the message)
3. Refactor
4. Go to Step 1

### Example

When test-driving an implementation of a program that converts integers into roman numerals, we might start with the simplest test:
”roman numeral for 1 is I”

We write the failing test, requiring 1 to be converted to “I”.

The simplest solution might be to return the hardcoded literal value "I". Then we move on to the next easiest failing test.

Test round #1: 1 = I -> return "I"

Test round #2: 2 = II -> if integer = 1 return "I" else return "II"

Test round #3: 3 = III -> while(integer > 0) concatenate "I" to result and decrement integer.

### Benefits

There are numerous intended benefits of this approach, including:

- Working in very small increments
- Having the regression safety net of the previous tests when adding each requirement
- Freedom to aggressively refactor the implementation, since (ideally) the tests will have very little coupling to implementation details
- Resulting tests provide a complete (if highly redundant) regression test suite, if TDD is practiced universally
