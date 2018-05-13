# What is Node.js?

Node is a JavaScript runtime environment which allows us to run JavaScript anywhere.

## What is a runtime enviroment? 

A runtime environment is an environment which includes all of the tools and features needed to run a specific program. Node.js translates the JavaScript programs into `bytecode` which is machine code that can be read by the host operating system.

## More on Node

Node is not a framework (there are frameworks built on top of Node.js though).

Node is not a programming language (the language is still JavaScript).

Node has a strong and growing ecosystem. This includes packages created by the community, and continuing open source development on the runtime itself.

npm is the package manager for Node. This means that you and other coders can share your JavaScript code easily, using a command line tool.

Modules are bundles of reusable code that are packaged with any of the code they depend on (dependencies). The benefits of modules are endless, and we will discuss them shortly.

To install packages for use in a program of ours, first we must define our **manifest file**. A manifest file is a file that lists out all the packages our program depends on to function. With npm,this file is going to be called `package.json.` This is a JSON formatted file that specifies all of the modules your project will use.

`npm install` without any modifying arguments will always install the Node modules locally in the node_modules folder of the current directory. This is generally the desired behavior; however, some modules can be run directly from the command line. Think of these global modules as new commands that are written using Node and JavaScript. These kinds of modules are ones that you might want to use outside of a particular project and have access to them globally.

running `npm install` will look for a package.json file and install the packages listed there. The node_modules folder is where `npm install`s local modules. This is also the first place Node looks when you require a module.

`version`: The version of the package expressed as major.minor.patch. This is known as semantic versioning, and it is recommended to start with version 1.0.0.

Run `npm init` in the terminal and it will guide you through a series of prompts. This will generate a simple package.json file that’s in line with the community standard and the latest specification from npm. `npm init` is pretty self-explanatory about what each of the fields means. The one exception is the main value. main should be the filename or path to the JavaScript that should be used when a user requires your module. In general, the default value of index.js is fine.

The require function is specific to Node and is unavailable to web browsers. At its core, all require does is execute JavaScript based on the supplied argument. When you require a module, you execute the JavaScript code that makes up the specified module. Node then returns an object that has function and values attached to it, just like any other JavaScript object.

The ability to point require at any arbitrary files allows developers to break their applications down into smaller parts and keep logic housed in single modules. In any web server, there is going to be boilerplate initialization logic. Instead of being forced to have this logic in the main application code, it can be housed in a separate file and executed with require once in the main application startup. If you create several applications that all share some boilerplate code, this small JavaScript file could even be shared across multiple projects.

The most important concept to understand about JavaScript, and Node by extension, is that it is single-threaded. *This means that JavaScript applications can only perform one task at a time.* They can, however, give the illusion of being multi-threaded through the use of an event loop. Essentially, the JavaScript engine maintains several queues of unhandled tasks. These queues include things such as events, timers, intervals, and immediates. Each execution of the event loop, known as a cycle, causes one or more tasks to be dequeued and executed. As these tasks execute, they can add more tasks to the internal queues. Each cycle is made up of smaller steps, known as ticks.

To avoid the performance penalties associated with blocking I/O, Node.js almost exclusively uses asynchronous non-blocking I/O.

Excertps from - [Full Stack JavaScript Development With MEAN - MongoDB, Express, AngularJS, and Node.JS 1st Edition](https://www.sitepoint.com/premium/books/full-stack-javascript-development-with-mean) by Colin J. Ihrig & Adam Bretz