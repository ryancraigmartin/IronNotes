# Q & A

## What does it mean to be Asynchronous?

By default, many frameworks and runtime environments are `blocking`. This, at a very simple level, means you can only complete one instruction at a time, and cannot continue to the next instruction until the previous is done.

Javascript code runs on a single thread which means that it can only do one thing at a time.

Asynchronous code means that a programming language can complete instructions in a different order than they are written.

In Asynchronous code, requests are handed off to another thread so that the "code thread" can continue to move on to the next code block.

Once the data is retrieved the callback function from the request is adding on to the end of the thread at the end of the queue.

Synchronous code waits for one action to complete before moving on to the next. This delays the rest of the code.

When we looked at JavaScript, we learned that code executes from top to bottom, instruction by instruction sequentially. We can add loops and conditionals to construct the logic of our algorithms,but in the end, it’s just one instruction after another

---

## Framework vs. Toolkit vs. Library

The most important difference, and in fact the defining difference between a library and a framework is Inversion of Control.

What does this mean? Well, it means that when you call a library, you are in control. But with a framework, the control is inverted: the framework calls you. (This is called the Hollywood Principle: Don't call Us, We'll call You.) This is pretty much the definition of a framework. If it doesn't have Inversion of Control, it's not a framework. (I'm looking at you, .NET!)

Basically, all the control flow is already in the framework, and there's just a bunch of predefined white spots that you can fill out with your code.

A library on the other hand is a collection of functionality that you can call.

I don't know if the term toolkit is really well defined. Just the word "kit" seems to suggest some kind of modularity, i.e. a set of independent libraries that you can pick and choose from. What, then, makes a toolkit different from just a bunch of independent libraries? Integration: if you just have a bunch of independent libraries, there is no guarantee that they will work well together, whereas the libraries in a toolkit have been designed to work well together – you just don't have to use all of them.

But that's really just my interpretation of the term. Unlike library and framework, which are well-defined, I don't think that there is a widely accepted definition of toolkit.

**Martin Fowler** discusses the difference between a library and a framework in his article on Inversion of Control:

Inversion of Control is a key part of what makes a framework different to a library. A library is essentially a set of functions that you can call, these days usually organized into classes. Each call does some work and returns control to the client.

A framework embodies some abstract design, with more behavior built in. In order to use it you need to insert your behavior into various places in the framework either by subclassing or by plugging in your own classes. The framework's code then calls your code at these points.

To summarize: your code calls a library but a framework calls your code.

[StackOverflow Link](https://stackoverflow.com/questions/3057526/framework-vs-toolkit-vs-library)

---

