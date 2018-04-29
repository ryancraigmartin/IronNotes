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