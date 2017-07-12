---
layout: post
title: How to write good README?
published: true
---

A README is the first file a person should read when encountering a source tree, and it should be written as a very brief, very basic introduction to the software. 

#### Format
A form of documentation, it is usually a simple plain text file called READ.ME, README.TXT, README.md (for a text file using markdown markup), README.1ST – or simply README.

#### Use capital letters
The file's name is generally always written in upper case. On Unix-like systems in particular this makes it easily noticed – both because lower case filenames are more usual, and because traditionally the ls command sorts and displays files in ASCIIbetical ordering, so that upper-case filenames appear first.

#### What should be included in README?

- **Table of Content** is **optional**, but appreciated for lengthy README files:
```
CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Requirements
 * Recommended modules
 * Installation
 * Configuration
 * Troubleshooting
 * FAQ
 * Maintainers
```

- Introduction
The introduction should consist of a brief paragraph or two that summarises the purpose and function of this project.

- Requirements
The requirements section should make it clear whether this project requires anything to work (modules, libraries, etc). List all requirements here, including those that follow indirectly from another module, etc. The idea is to inform the users about what is required, so that everything they need can be procured and included in advance of attempting to install the module. If there are no requirements, write "No special requirements".

    — **name** of the **projects** and all **sub-modules and libraries**;
    — **descriptions** of all the project, and all sub-modules and libraries;
    — 5-line code snippet on how its used (if it's a library) **copyright and licensing** information;
