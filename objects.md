# Objects

The simple types of JavaScript are numbers, strings, booleans, null, and undefined. All other values are objects. Arrays, functions, regular expressions, and objects of course are all objects.

An object property value can be any value except for undefined.

An Object in JavaScript is a collection composed of key-value pairs.

The key is a string that identifies a property of an object.

- The value is the content associated to the indicated key.
- The keys are also unique in an object, one key will always have just one value associated to it. This value could be any type of JavaScript value.

Objects are data models that allow us to combine properties and methods for a specific data set in a structured way. 

If I was an object I would have properties like:
- Name: Ryan
- Hair: Brown
- Height: 5'11

console.log(); - Can be broken down into an Object and a Method.

***Object*** - Course Data:
- title ---> Properties
- instructor ---> Properties
- level ---> Properties
- published   ---> Properties
- views ---> Properties

---

Remember that keys can’t have spaces like my key, and they should be camelCase. You have to separate the keys values with a comma after each value, otherwise it will give you an error.


## Defining an Object

``` js
var course = new Object(); // Defines a new object

// Object properties
course.title = "JavaScript Essentials" 
course.instructor = "Ryan Martin"
course.level = 1;
course.published = true;
course.views = 0
console.log(course);
```
&nbsp; This can also be written like this:

``` js
var course = new Object();

var course = {
title: "JavaScript Essentials",
instructor: "Ryan Martin",
level: 1,
published:  true,
views: 0,
}
console.log(course);
```

### Dot & Bracket Notation to Access Values

&nbsp; Accessing values with dot notation

`olympicRecords.athletics100Men // => "Justin Gatlin"`

&nbsp; Accessing values with brackets notation

`olympicRecords["athletics100Men"] // => "Justin Gatlin"`

It’s best practice to use dot notation as much as you can though because it’s shorter and cleaner.


&nbsp; Adding / Updating Properties With Dot Notation

``` js
var olympicRecords = {
  athletics100Men: "Justin Gatlin",
  athleticsLongJumpMen: "Mike Powel",
}

olympicRecords.swimming200Men = "Michael Phelps";
```
&nbsp; Adding / Updating Properties With Bracket Notation
``` js
var olympicRecords = {
  athletics100Men: "Justin Gatlin",
  athleticsLongJumpMen: "Mike Powel",
  swimming200Men: "Michael Phelps"
}
olympicRecords["swimming400Women"] = "Katie Ledecky";

```
Object.keys() will help you to list all the properties of the object.

`for..in` is a loop specifically designed for iterating over objects.
``` js
for (var recordName in olympicRecords){
  // recordName is a **key** in the object
  console.log("recordName: " + recordName);
}
```