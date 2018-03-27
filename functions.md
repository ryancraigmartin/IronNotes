# Functions

- [X] Creating a function.
- [ ] Use `return` values in a function.
- [ ] Understand `arguments`.
- [ ] Understand `function scope`.

Generally speaking, a function is a “mini-program” that can be called by code external to the function. Like the program itself, a function is composed of a sequence of statements called the function body. 

To help structure our code and make common operations reusable, we create functions and objects. In this chapter, we'll look at both of these in detail. Functions are mini programs inside our scripts. They can be used to segment off sections of our code to make it easier to manage, or to run repeated operations, or both. Functions wrap around code blocks, which contain the actual statements to be run, and typically include some combination of variable assignments, operations, and conditions.

Values can be passed to a function, and the function will return a value. Functions are one of the fundamental building blocks in JavaScript. A function is a set of statements that performs a particular task of the program. This task could be just a little part, or even the whole program.

***Abstraction*** works by separating **what** a `function` does and **how** it does it.

In Javascript we work with three types of functions.

1. **Named Functions** - Executed when called by name.
2. **Anonymous Functions** - Don't have a name. Are run once they are triggered by an event. 
3. **Immediately invoked function expressions** - Run as soon as the browser encounters them.

### Creating a function
This will be the preferred way to *create functions*.

    function functionName(argument1, argument2,...)
    {
      // Instruction 1
      // Instruction 2
      // ...
    }

You can create *anonymous functions* and associate it to the values of a variable:

    var functionName = function (argument1, argument2,...) 
    {
      // Instruction 1
      // Instruction 2
      // ...
    }

After you declare the function, you can call (execute) the function by using its name, followed by parantheses.

``` js
function sayHello()
{
  console.log("Hello! I'm Ryan.");
}
sayHello(); // Hello I'm Ryan.
```

&nbsp; Here is a more detailed example. 

``` js
function findBiggestFraction()
{
  a > b ? console.log("a: ", a) : console.log("b: ", b);
}
var a = 3/4;
var b = 5/7;
findBiggestFraction(); // Calls the function.
```

## `Arguments`

Sometimes your functions need information from the outside to execute their code.
You can pass `arguments` to your function to pass dynamic (changing or variable) data to the function. Pass the values you want to use between the parentheses, separated by commas.
First, you must define the name of the `arguments`. It can be anything you want. The names are just placeholders for actual values.

``` js
function sumNumbers(numberOne, numberTwo) // numberOne & numberTwo are arguments.
{
  return numberOne + numberTwo;
}
var result = sumNumbers(2,2);
console.log("The result is " + result);
```
`Arguments` can contain any type: arrays, numbers, strings, etc.
You can pass as many `arguments` as you’d like, but as a guideline you’re going to want to keep it under 4.

``` js 
var animalArray = ["Dog", "Fish", "Cat"];
function printLength(arrayToCount)
{
  var theLength = arrayToCount.length;
  console.log("The length of your array is " + theLength);
}
printLength(animalArray);
```

&nbsp; Lets do more with the fraction example by using arguments. 

``` js
function findBiggestFraction(a,b)
{
  a > b ? console.log("a: ", a) : console.log("b: ", b);
}

var firstFraction = 3/4;
var secondFraction = 5/7;

findBiggestFraction(firstFraction,secondFraction); // Call the function.
findBiggestFraction(7/16, 13/25); // Call the function with argument
// Result is that b is the larger fraction -> 0.52
```
&nbsp; Lets expand a little further. 
``` js 
function findBiggestFraction(a,b) 
{
  var result;
  a > b ? result = ["firstFraction", a] : result = ["secondFraction", b];
  return result;
}

var firstFraction = 3/4;
var secondFraction = 5/7;

var fractionResult = findBiggestFraction(firstFraction,secondFraction);

console.log("First fraction result: ", firstFraction);
console.log("Second fraction result: ", secondFraction);
console.log("Fraction " + fractionResult[0] + " with a value of " + fractionResult[1] + " is the biggest!");
// First fraction result:  0.75
// Second fraction result:  0.7142857142857143
// Fraction firstFraction with a value of 0.75 is the biggest!
```

&nbsp; Now lets rewrite the same function as an anonymous function. 

``` js
var theBiggest = function(a,b) 
{
  var result;
  a > b ? result = ["a", a] : result = ["b", b];
  return result;
}
console.log(theBiggest(10,100)); // These numbers are being passed as (a,b).
// The result is ["b", 3]
```

### Using `return` values.

To return a value you use the keyword `return`. Simple enough!
A function can only have one return value, but it can be any type of value.
***Beware,*** `return` ends the function immediately. Only use it when you want to return a value and end the function.

---





