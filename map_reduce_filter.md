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

---

``` js
age = [33, 12, 20, 16, 5, 54, 21, 44, 61, 13, 15, 45, 25, 64, 32];

const companies= [
        {name: "Company One", category: "Finance", start: 1981, end: 2004},
        {name: "Company Two", category: "Retail", start: 1992, end: 2008},
        {name: "Company Three", category: "Auto", start: 1999, end: 2007},
        {name: "Company Four", category: "Retail", start: 1989, end: 2010},
        {name: "Company Five", category: "Technology", start: 2009, end: 2014},
        {name: "Company Six", category: "Finance", start: 1987, end: 2010},
        {name: "Company Seven", category: "Auto", start: 1986, end: 1996},
        {name: "Company Eight", category: "Technology", start: 2011, end: 2016},
        {name: "Company Nine", category: "Retail", start: 1981, end: 1989}
    ];

// =========================================================================
//  FILTER
// =========================================================================

let canDrink = []
for (let i = 0; i < age.length; i++) {
    if (age[i] >= 21) {
        canDrink.push(age[i]);
    }
}
console.log(canDrink);

// -----------------------------------------------

// Using ES6 Arrow Functions
const canDrink = age.filter(age => age >= 21);
                // Parameter ---^

console.log(canDrink);

// -----------------------------------------------

// Filter the retail companies: 
const retailCompanies = companies.filter(company => company.category === 'Retail')

console.log(retailCompanies);

// -----------------------------------------------

// Filter the retail companies started in the 80s:
const retailCompaniesFrom80s = companies.filter(company => company.start >= 1980 && company.start <= 1990);

console.log(retailCompaniesFrom80s);

// -----------------------------------------------

// Filter the retail companies that lasted 10 years or more:
const retailCompaniesThatLasted= companies.filter(company => (company.end - company.start >= 10));

console.log(retailCompaniesThatLasted);

// =========================================================================
//  MAP
// =========================================================================

// Create array of company names without arrow functions.
const companyNames = companies.map(function(company) {
    return company.name;
});

console.log(companyNames);

// Create array of company names + start and end dates without arrow functions.
const companyNamesAndDates = companies.map(function(company) {
    return `${company.name} [${company.start} - ${company.end}]`;
});

console.log(companyNamesAndDates);

// Rewrite using arrow functions: 
const companyNamesAndDatesES6 = companies.map(company => `${ company.name } [${company.start} - ${company.end}]`);

console.log(companyNamesAndDatesES6);
// -----------------------------------------------

const ageSquare = age.map(age => Math.sqrt(age));

console.log(ageSquare);

// =============================================================================
// Reduce
// =============================================================================

// Done with a for loop.
let ageSum = 0;

for(let i=0; i < age.length; i++) {
    ageSum += age[i];
}

console.log('Sum of ages: ', ageSum);

// -----------------------------------------------

// Using Reduce
const ageSumReduce = age.reduce(function(total, age) {
    return total + age;
}, 0);

console.log('Sum of ages: ', ageSumReduce);

// -----------------------------------------------

// Using Reduce + ES6
const ageSumReduceES6 = age.reduce((total, age) => total + age, 0);

console.log('Sum of ages: ', ageSumReduceES6);

// -----------------------------------------------

// Get total years for all of the comapnies
const totalYears = companies.reduce(function(total, company) { 
    return total + (company.end - company.start);
}, 0)

console.log(totalYears);

// -----------------------------------------------

// Get total years for all of the comapnies using ES6
const totalYearsES6 = companies.reduce((total, company) => total + (company.end - company.start), 0);

console.log(totalYearsES6);
```

[JavaScript Higher Order Functions & Arrays by Traversy Media](https://www.youtube.com/watch?v=rRgD1yVwIvE&t=484s)