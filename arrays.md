# Arrays

Arrays were one of the last things that I started learning when attempting to learn Java programming in college. 
Needless to say I only got a surface level understanding of what they are and what they are capable of. 

#### Lets see if we can break down arrays:

- [x] *Explain what an array is, and what it is used for.*

- [x] *Create an array in JavaScript.*

- [x] *Perform some simple operations on an array.*

- [x] *Add and remove elements from an array.*

### What is an Array?

An array is the first data structure that I've encountered.
Arrays and other data structures are widely used in almost every programming language.
An array is just a collection of anything. You can put anything in your list: `strings`, `numbers`, `objects`, and other data structures. You can even mix types in the same array.

An index in an array is a location in which data is being stored. These data segments are known as elements. 
Indexes start at 0. If an array has 3 elements, the index ‘2’ will be the last one. This is called Zero Base Numbering.

Now this begs the question, "What are the other data structures?"
I've come accross an [article from the FreeCodeCamp Medium](https://medium.freecodecamp.org/10-common-data-structures-explained-with-videos-exercises-aaff6c06fb2b) that does a great job of covering some more commonly used data structures and even gives some exercises to work through.

I'm sure each of those data structures will require their own note once I get to learning them, but for now that reference should be a good starting point.

&nbsp; Here is a simple example of an Array: 

``` js
var animalContainer= ["Dog", "Cat", "Fish"];

var myDog = animalContainer[0];
  console.log(myDog); // Prints out Dog

var myFish = animalContainer[2];
  console.log(myFish); // Prints out Fish
```

We can also find out the length of an Array by simply adding *.length* to the end of the name we gave our Array.

``` js
var animalContainer = ["Dog", "Cat", "Fish"]
console.log(animalContainer.length); // Prints out the number 3 which is how many elements are in our Array.
```

Since the numbers of an Array begin at 0 instead of 1, we will need to keep this in mind when looking for the idex of a specific element. 

&nbsp; Lets look for the last element using _.length_

``` js
var animalContainer = ["Dog", "Cat", "Fish"];
var lastIndex = animalContainer.length - 1;
var lastElement = animalContainer[lastIndex];
console.log(lastElement); // Prints out Fish
```

---

- [X] Add elements from the end of an Array.
- [X] Add elements to the beginning of an Array.
- [X] Add and Update elements at a specific position in an Array.
- [X] `Delete` and `Splice` elements from an Array.

---

### **Add** elements from the end of an Array.

&nbsp; The `push` method adds a new element to the **end** of your Array.

``` js
var boxOfToys = ["Cars", "Lego", "Dolls"]
console.log(boxOfToys); // Will print out [ 'Cars', 'Lego', 'Dolls' ]
boxOfToys.push("Heelys");
console.log(boxOfToys);  // Will print out [ 'Cars', 'Lego', 'Dolls', 'Heelys']
```

### **Add** elements to the beginning of an Array.

As we just learned, the `push` method will let us add an element to the end of our Array. In order to add an element to the beginning of the Array, we need to use the `unshift` method, similarly to how we previously used `push`.

``` js
var boxOfToys = ["Cars", "Lego", "Dolls", "Heelys"]
boxOfToys.unshift("Nintendo");
console.log(boxOfToys); // Prints out [ 'Nintendo', 'Cars', 'Lego', 'Dolls', 'Heelys' ]
```

### **Add / Update** elements at a specific position in an Array.

Adding new elements into the Array is simple. We just need to specify the index where the new element should be in the order of our Array. **However,** if we specify an index number beyond the amount of elements we already have, JavaScript will automatically fill in any empty indexes with `undefined` which show up as empty strings. 

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Lego", "Dolls", "Heelys"]
console.log("Before changes:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Lego', 'Dolls', "Heelys" ]

boxOfToys[5] = "Nintendo";
console.log("After adding element:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Lego', 'Dolls', 'Heelys', , 'Nintendo' ]
```
**Notice:** Index [4] is now an *empty string* because there were only 4 elements in the Array and we wanted to add one at index 5.

Similarly, we can **update** any elements that are in our Array by simply specifying the index and deciding what new data needs to replace the current element. 

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Lego", "Dolls", "Heelys"]
console.log("Before changes:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Lego', 'Dolls', "Heelys" ]

boxOfToys[2] = "Nintendo";
console.log("After updating element:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Nintendo', 'Dolls', 'Heelys']
```

### **Delete** elements from an Array.
In order to remove an element from an Array we need to specify the index and use the `delete` method. 
This will replace the element from the Array with an *empty string* / `undefined`.

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Lego", "Dolls", "Heelys"];
delete boxOfToys[0];
console.log(boxOfToys); 
```
---

`splice` is a method that we can use when we want to remove an item and shift the indexes of our elements so that there are no *empty strings.*

`splice` receives two arguments:

  - The first defines the index you want to delete.
  - The second defines how many items will be deleted from this position.

If we pass a third argument, it is inserted as a replacement.

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Lego", "Dolls", "Heelys"];
boxOfToys.splice(1,1); // Splices one element at index[1]
console.log(boxOfToys); 
// Prints out [ 'Cars', 'Dolls', 'Heelys' ]
```

---
Let’s perform a few operations on the array below.

1) Add two of your favorite animals to the end of the array.
2) Remove the first two elements of the array.
3) Replace the last element in the array with the word “last”.

``` js
var animalArray = ["Dog", "Cat", "Fish", "Lizard", "Whale", "Cheetah"];
console.log("Original: " + animalArray);
console.log("------");

// "From the first element, remove one going forward"
animalArray.splice(0, 1);
console.log(animalArray);

//  "From the second element, remove two going forward"
animalArray = ["Dog", "Cat", "Fish", "Lizard", "Whale", "Cheetah"];
animalArray.splice(2, 2);
console.log(animalArray);

// If we pass a third argument
// It is inserted as the replacement
animalArray = ["Dog", "Cat", "Fish", "Lizard", "Whale", "Cheetah"];
animalArray.splice(0, 1, "Something else");
console.log(animalArray);
```

### Solutions

1. ` animalArray.push("Wolf", "Tiger");`

Result: Dog,Cat,Fish,Lizard,Whale,Cheetah,Wolf,Tiger

2. ` delete animalArray[0];
     delete animalArray[1];`

Result: ,,Fish,Lizard,Whale,Cheetah,Wolf,Tiger

  or

2.   ` animalArray.splice(0,2); `

Result: Fish,Lizard,Whale,Cheetah,Wolf,Tiger
   
3. `animalArray[7] = "Last";`

Result: [ 'Dog', 'Cat', 'Fish', 'Lizard', 'Whale', 'Cheetah', 'Wolf', 'Last' ]

---

### Array Iteration

One of the most common uses of a loop is iterate over an array. This simply means going through each element of an array.

Any loop can be used to iterate through an array, but some are preferable because they are simpler and generally look better.

#### FOR Loop Example
For this example, we will create a counter `i` to increment starting at 0 and keep looping until `i` reaches the length of the array.

``` js
var computerParts = ["CPU","GPU","RAM"]
for (var i = 0; i < computerParts.length; i++){
  console.log(computerParts[i]); // Prints out CPU GPU RAM in the same order. 
}
```

#### WHILE Loop Example
Just like the for loop, you start a counter, in our case `i`, at 0, and count until it reaches the end of the array.

``` js
var i = 0; // Serves as our counter
var computerParts = ["CPU","GPU","RAM"]
while (i < computerParts.length)
{
  console.log(computerParts[i]); 
  i++;
}
```

#### forEach Method
The forEach is an array method that iterates through each element of the array for you.

``` js
var computerParts = ["CPU","GPU","RAM"];
computerParts.forEach(function(part){
  console.log(part);
});
```
As you may have noticed, you’re passing to forEach a function as a parameter. This is called a callback function. 

##### forEach Exercises

1. Create an array with 6 of your favorite foods.
``` js
var favoriteFoods = ["Shrimp","Steak","Scallops","Crab","Lobster","Chicken"];
```

2. With the loop of your choice, iterate through the array, but only print out the foods with an even index.

``` js
var favoriteFoods =   
[
	'Shrimp', 'Steak', 'Scallops',
	'Crab', 'Lobster', 'Chicken',
];

for (var i = 0; i <= favoriteFoods.length; i++) 
{
  if (i % 2 === 0 )
  {
	  console.log(favoriteFoods[i]);
  }
}
```

## Extra Notes:

***Properties***: Meta information about the object.

***Methods***: Functions that belong to the object.



Single and Double LinkLists
ArrayLists
Stacks and Queues 
