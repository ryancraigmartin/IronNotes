# Functions

- [X] Creating a function.
- [ ] Use `return` values in a function.
- [ ] Understand `arguments`.
- [ ] Understand `function scope`.

Generally speaking, a function is a “subprogram” that can be called by code external to the function. Like the program itself, a function is composed of a sequence of statements called the function body. 

Values can be passed to a function, and the function will return a value. Functions are one of the fundamental building blocks in JavaScript. A function is a set of statements that performs a particular task of the program. This task could be just a little part, or even the whole program.

***Abstraction*** works by separating **what** a `function` does and **how** it does it.

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

### Using `return` values.

To return a value you use the keyword `return`. Simple enough!
A function can only have one return value, but it can be any type of value.
***Beware,*** `return` ends the function immediately. Only use it when you want to return a value and end the function.


---

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


