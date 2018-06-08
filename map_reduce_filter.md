``` js
const animals = [
    {
        "name": "cat",
        "size": "small",
        "weight": 5
    },
    {
        "name": "dog",
        "size": "small",
        "weight": 10
    },
    {
        "name": "hedgehog",
        "size": "small",
        "weight": 3
    },
    {
        "name": "lion",
        "size": "medium",
        "weight": 150
    },
    {
        "name": "pig",
        "size": "medium",
        "weight": 150
    },
    {
        "name": "elephant",
        "size": "big",
        "weight": 5000
    }
]


// =============================================================================
// FOR LOOP
// =============================================================================

// ANIMAL NAMES

let animalNames = [];

for (let i = 0; i < animals.length; i++){
    animalNames.push(animals[i].name);
}
    console.log(animalNames);

// ---------------------------------------------

// SMALL ANIMALS

let smallAnimals = []

for (let i = 0; i < animals.length; i++) {
    if (animals[i].size === 'small') {
        smallAnimals.push(animals[i])
    }
}

console.log(smallAnimals);

// ---------------------------------------------

// TOTAL ANIMAL WEIGHT

let totalWeight = 0;

for (let i = 0; i < animals.length; i++){
    totalWeight += animals[i].weight;
}
console.log(totalWeight);

// =============================================================================
// MAP
// =============================================================================

/*
Parameters:
callback: Function that produces an element of the new Array, taking three arguments.
currentValue: The current element being processed in the array.
(optional) index: The index of the current element being processed in the array.
(optional) array: The array map was called upon.
(optional) thisArg: Value to use as this when executing callback.
*/

// The map() method creates a new array with the results of calling a provided function on every element in the calling array.

let animalNames = animals.map((animal, index, animals) =>{
    return animal.name;    //       ^       ^       ^ 
})                         //       |       |       |
//                         // Current Item  |       |
//                         //         Current Index |
//                         //                The Entire Array
//                         // Map returns the finished array, so we can simply assign it to a variable.
//                         // Use a return statement, otherwise your array will end up with all items as undefined.

// =============================================================================
// FILTER
// =============================================================================

/* 
The filter() method creates a new array with all elements that pass the test implemented by the provided function.

Parameters: 
    callback: Function is a predicate, to test each element of the array. Return true to keep the element, false otherwise, taking three arguments:
    element: The current element being processed in the array.
    (optional) index: The index of the current element being processed in the array.
    (optional) array: The array the filter was called upon.
    (optional) thisArg: A value to be used as this when executing callback.
*/

let smallAnimals = animals.filter((animal) => {
    return animal.size === 'small'
})

console.log(smallAnimals);

// =============================================================================
// REDUCE
// =============================================================================

let totalWeight = animals.reduce((weight, animal, index, animals) => {
    return weight += animal.weight
}, 0)
```

[Understanding map, filter and reduce in Javascript by Luuk Gruijs](https://hackernoon.com/understanding-map-filter-and-reduce-in-javascript-5df1c7eee464)