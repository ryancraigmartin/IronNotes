# Q & A

## What does it mean to be Asynchronous?

By default, many frameworks and runtime environments are `blocking`. This, at a very simple level, means you can only complete one instruction at a time, and cannot continue to the next instruction until the previous is done.

Javascript code runs on a single thread which means that it can only do one thing at a time.

Asynchronous code means that a programming language can complete instructions in a different order than they are written.

In Asynchronous code, requests are handed off to another thread so that the "code thread" can continue to move on to the next code block.

Once the data is retrieved the callback function from the request is adding on to the end of the thread at the end of the queue.

Synchronous code waits for one action to complete before moving on to the next. This delays the rest of the code.

When we looked at JavaScript, we learned that code executes from top to bottom, instruction by instruction sequentially. We can add loops and conditionals to construct the logic of our algorithms,but in the end, it’s just one instruction after another