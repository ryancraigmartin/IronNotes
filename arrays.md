

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

Now this begs the question, "What are the other data structures?"
I've come accross an [article from the FreeCodeCamp Medium](https://medium.freecodecamp.org/10-common-data-structures-explained-with-videos-exercises-aaff6c06fb2b) that does a great job of covering some more commonly used data structures.

I'm sure each of those data structures will require their own note once I get to learning them, but for now that referance should be a good starting point.



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

- [X] Add / Remove elements from the end of an Array.
- [ ] Add / Remove elements at the beginning of the Array.
- [ ] Add / Update elements at a specific position in the Array.

---

### Add elements from the end of an Array.

&nbsp; The `push` method adds a new element to the **end** of your Array.

``` js
var boxOfToys = ["Cars", "Legos", "Dolls"]
console.log(boxOfToys); // Will print out [ 'Cars', 'Legos', 'Dolls' ]
boxOfToys.push("Heelys");
console.log(boxOfToys);  // Will print out [ 'Cars', 'Legos', 'Dolls', 'Heelys']
```


### Add / Remove elements at the beginning of the Array.

As we just learned, the `push` method will let us add an element to the end of our Array. In order to add an element to the beginning of the Array, we need to use the `unshift` method, similarly to how we previously used `push`.

``` js
var boxOfToys = ["Cars", "Legos", "Dolls", "Heelys"]

boxOfToys.unshift("Nintendo");

console.log(boxOfToys); // Prints out [ 'Nintendo', 'Cars', 'Legos', 'Dolls', 'Heelys' ]

```




### Add / Update elements at a specific position in the Array.

Adding new elements into the Array is simple. We just need to specify the index where the new element should be in the order of our Array. **However,** if we specify an index number beyond the amount of elements we already have, JavaScript will automatically fill in any empty indexes with `undefined` which show up as empty strings. 

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Legos", "Dolls", "Heelys"]
console.log("Before changes:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Legos', 'Dolls', "Heelys" ]

boxOfToys[5] = "Nintendo";
console.log("After adding element:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Legos', 'Dolls', 'Heelys', , 'Nintendo' ]
```
**Notice:** Index [4] is now an empty string because there were only 4 elements in the Array and we wanted to add one at index 5.

Similarly, we can update any elements that are in our Array by simply specifying the index and deciding what new data needs to replace the current element. 

&nbsp; Example:

``` js
var boxOfToys = ["Cars", "Legos", "Dolls", "Heelys"]
console.log("Before changes:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Legos', 'Dolls', "Heelys" ]

boxOfToys[2] = "Nintendo";
console.log("After updating element:" + boxOfToys); // Will print out Before changes: [ 'Cars', 'Nintendo', 'Dolls', 'Heelys']
```

