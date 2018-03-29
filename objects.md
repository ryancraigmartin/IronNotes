# Objects

An Object in JavaScript is a collection composed of key-value pairs.

The key is a string that identifies a property of an object.

- The value is the content associated to the indicated key. 
- The keys are also unique in an object, one key will always have just one value associated to it. This value could be any type of JavaScript value.

Objects are data models that allow us to combine properties and methods for a specific data set in a structured way. 

***Object*** - Course Data: 
  - title ---> Properties
  - instructor ---> Properties
  - level ---> Properties
  - published   ---> Properties
  - views ---> Properties

---

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