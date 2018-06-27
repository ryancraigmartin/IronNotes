# Prep

* JavaScript is a multi paradigm language. A paradigm is a way of thinking about software construction based off of fundamental design principles. JavaScript supports imperative / procedural programming along with OOP, and functional programming. JS supports OOP with prototypal inheritance where app state is shared and colocated with methods in objects.

* What is *functional programming?*: One of the two pillars of JavaScript. Produces programs by composing mathematical functions, avoids `shared state` and mutable data. Focuses on function purity, avoiding side effects, simple function composition, & first class functions. FP is declarative rather than imperative, and app state flows through pure functions.

* What is a *promise?*: A promise is a placeholder for computation that hasn't happened/finished yet. The then()function accepts 2 functions as parameters: a function to be executed when the promise is fulfilled, and a function to be executed when the promise is rejected.

> Kyle Simpson: "Think of a promise as being like a meal receipt at a fast-food restaurant. You order your meal and pay for it, and the clerk gives you a number that you need to claim the food when it is done. When the food comes out, the clerk calls your number and you exchange the receipt for the food. Promises work the same way. You've called a function, passed it some data, and received a promise in return. When the "food" is done, the function resolves the promise (calls your number) and passes you the result. Attaching a callback to the promise is your way of handing back the receipt."Why not just use a callback?" you may ask. Well, promises offer some control flow advantages that are kind of cumbersome to do with callbacks, but the real advantage is that the promise acts as a data escrow. A promise can never be resolved multiple times, will always be resolved asynchronously, bubbles up any errors that occur, and ensure that the code you're calling can't accidentally hang on to your calling context and create a memory leak. Callbacks have none of these abilities and can actually be dangerous for your application if a third party library handles them wrong."

* What is *async*/*await*?: Async Await was added to JavaScript to make working with asynchronous functions more enjoyable and easy to understand. It's built on top of promises and is compatible with existing Promise-based APIs. 
* 
`Async` - declares an asynchronous function `(async function someName(){...})`.
- Automatically transforms a regular function into a Promise.
- When called async functions resolve with whatever is returned in their body.
- Async functions enable the use of await.

`Await` - pauses the execution of async functions. `(var result = await someAsyncCall();)`.
- When placed in front of a Promise call, await forces the rest of the code to wait until that Promise finishes and returns a result.
- Await works only with Promises, it does not work with callbacks.
- Await can only be used inside async functions.