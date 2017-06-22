---
layout: post
title: BDD with Karma and Jasmine
published: true
---

**Karma** is a type of **test runner** that creates a fake server, and then spins up tests in various browsers using data derived from that fake server.

Karma is only a test runner, and requires a **testing framework** such as **Jasmine** to plug into it in order to actually run tests.

### Installation
Karma runs on Node.js and requires Node.js with NPM to be installed prior to installing Karma.
[Installing Node.js and updating npm](https://docs.npmjs.com/getting-started/installing-node)


The recommended approach is to install Karma as an NPM package locally in the project's directory:

```
# Install Karma:
$ npm install karma --save-dev

# Install plugins that your project needs:
$ npm install karma-jasmine karma-chrome-launcher jasmine-core --save-dev
```

This will install **karma, karma-jasmine, karma-chrome-launcher and jasmine-core packages** into node_modules in your current working directory and also save these as **devDependencies** in package.json.

Now any other developer working on the project will only have to do npm install in order to get all these dependencies installed.

```
# Run Karma:
$ ./node_modules/karma/bin/karma start
```
##### Commandline Interface
It can be useful to install karma-cli globally:
```
$ npm install -g karma-cli
````


Now instead of writing whole *./node_modules/karma/bin/karma start* Karma can be run simply by writing
```
$ karma
````
in command line from anywhere and it will always run the local version.


### Configuration
In order to serve you well, Karma needs to know about your project in order to test it and this is done via a configuration file.

The configuration file can be generated using karma init file_name :
```
$ karma init my.conf.js
```

This will open configuration options for e.g. specifying browsers to be checked, source files to run tests on, and testing framework - Jasmine is one of the options here.

### Starting Karma
When starting Karma, the configuration file path can be passed in as the first argument.
````
$ karma start my.conf.js
```
### Adding tests
