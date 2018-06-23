# ES6

## var, let & const

**const** = `Constant` variable. Value *cannot be changed* once defined.

**let** = `Block Scope` variable. Has an even smaller scope than a `var`.

**cont** = default.

**let** = When rebinding is needed.

**const** cant be updated after declaration, but properties of a **const** can be updated.

**IFEE** - Immediately Invoked Function Expressions - Functions that run themselves and create a scope were nothing will leak into the parent scope

**Temporal Dead Zone**: You cannot access a variable before it is defined. When using var, the value will be undefined. When using let and const, it will give you an error.

**Default function arguments:** If nothing is passed into a function you can set defaults for the arguments.
EX: 
``` js
function calculateBill(total, tax = .13, tip = .15)
```

## Arrow Functions

3 main benefits:

1. Can be more concise than normal function.
2. Implicit returns. Great for writing one-liners.
3. Doesn't rebind the value of this when using an Arrow Function inside another function.

**Arrow Functions** are always anonymous functions but can be set to a variable for referencing and identification.

When NOT to use Arrow Functions:

1. When you really need to use *this*.
2. When you need a method to bind to an object.
3. When you need to add a prototype method.
4. When you need access to the arguments object.