---
layout: post
title: How to write good README?
published: true
---

A README is the first file a person should read when encountering a source tree, and it should be written as a very brief, very basic introduction to the software.

### Text file
A form of documentation, it is usually a simple plain text file called READ.ME, README.TXT, README.md (for a text file using markdown markup), README.1ST – or simply README.

### Use capital letters
The file's name is generally always written in upper case. On Unix-like systems in particular this makes it easily noticed – both because lower case filenames are more usual, and because traditionally the ls command sorts and displays files in ASCIIbetical ordering, so that upper-case filenames appear first.

### What should be included in README?

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
  — 5-line code snippet on how its used (if it's a library);


- Installation

The installation section should make it clear how to install the module. However, if the steps to install the module follow the standard instructions - simply provide a link and explain in detail any steps that may diverge from these steps.

Consider replacing this section with a standalone INSTALL.txt file if your installation instructions are especially complex.

	— instructions to grab the **documentation**;
	— instructions to **install, configure, and to run the programs**;

- Configuration

The configuration section is necessary even when little configuration is required. Use this section to list special notes about the configuration of this module – including but not limited to permissions.

If the module has little or no configuration, you should use this space to explain how enabling/disabling the module will affect the site.


- Troubleshooting & FAQ

These sections are optional. If present, they should address questions that are asked frequently in the issue queue (this will save you time in the future). Outline common problems that people encounter along with solutions (links are okay if the steps are long, but it is often helpful to provide a summary since links sometimes go stale).

- Bugs
Instructions to submit bugs, feature requests, submit patches, join mailing list, get announcements, or join the user or dev community in other forms.

- Copying/license
The section with all the legal notices, **copyright and licensing** information.



### On Github

On GitHub, if a Git repository has a README file in its main (top-level) directory and presented on the main web page.

README.md is used to generate the html summary you see at the bottom of projects. Github has their own flavour of Markdown. If there are two files named README and README.md, the file named README.md is preferred, and it will be used to generate github's html summary.
