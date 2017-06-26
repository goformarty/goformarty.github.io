---
layout: post
title: KISS DRY YAGNI
published: true
---
There are a lot of buzz words people throw around when talking about good practices in web and software development.

Let’s have a look at KISS, DRY and YAGNI.

### KISS
**Keep It Simple, Stupid**

This one is pretty self-explanatory. The simpler your code is, the easier it will be to maintain it in the future, avoid bugs, improve performance, add features - especially for people who were not working on this code before.

The KISS principle doesn’t mean that we cannot use complex solutions when solving complex problems. It means we should use the simplest solution that meets the requirements.

###DRY
**Don’t Repeat Yourself**

A little bit less self-explanatory than KISS, but still makes sense when clarified. The principle means we must try to maintain the behaviour of a functionality in a single piece of code. When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements.

But we should remember that duplicate code is not a problem if it serves different semantic.

###YAGNI
**You Aren't Gonna Need It**

Sometimes we try to think many steps ahead of the project coding and we add some extra features “just in case we need them” or “we will eventually need them”.

YAGNI principle means that even if we're totally, totally, totally sure that we'll need a feature later on, we shouldn’t implement it now. This doesn't mean we should avoid building flexibility, it means we shouldn't overengineer something based on what we think you might need later on.

Usually, it'll turn out either we don't need it after all, or what you actually need is quite different from what you foresaw needing earlier.
