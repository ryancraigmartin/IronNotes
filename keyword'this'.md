# The `this` Keyword

## What is the Keyword `this`?

`this` is a reserved keyword in JavaScript whose value is determined at execution.

`Execution context` is how a function is called.

## 4 Ways to figure out what the value of `this` is

If you understand the following four rules you will be able to determine what the value of `this` is within an execution context. 

- **global** - When `this` is not inside of a declared object. (There has not been an object defined which contains the keyword this.)
    - In the browser, the global value of `this` is the window object.

- **object/implicit** - When this is inside of a declared object the value of the keyword will always be the closest **parent** object.

- **explicit binding**- `call`, `apply`, and `bind` functions allow us to quickly determine what the value of `this` is. `call`, `apply`, and `bind` can only be used by functions.
    -  thisArg = What we want the value of `this` to be.
        - **call**: thisArg, a, b, c - Immediately invoked.
        - **apply**: thisArg, [a, b, c] - Array of arguments to pass to the function to change the value of this. Immediately invoked.
        - **bind**: thisArg, a, b, c - Like `call`, except `bind` returns a new function definition.
            - We can save fucntions with a different this value.
            - A building block for more advanced programming techniques.

- **new** - A new object is created. The keyword this will refer to the new object that is created.

A function call with a **new** operator in front of it turns into a constructor call. When the function is invoked as a constructor, a new object is created which is used as the this binding for the function call.

---

If we are not in Strict Mode, a plain function call sets this to the *global object*.
If we are in Strict Mode, a plain function call sets this to *undefined*. This depends only if the function is written in strict mode.