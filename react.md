# Notes on React

Components take parameters aka props and returns views to display via the render method.

The render method returns a description of what to render and displays it on the screen.

A constructor can use the super() keyword to call the constructor of the super class.

When you want to aggregate data from multiple children or to have two child components communicate with each other, *move the state upwards so that it lives in the parent component.* The parent can then pass the state to it's children via `props` so that the child components are always in sync with each other as well as the parent component.

Component state is considered to be private.

There are generally two ways of changing data:

1. Mutate the data directly by changing the values of a variable.
2. Replace the dada with a new copy of thr object that includes desired changes.

Avoiding data mutation lets us keep old versions of that data to refer or switch back to when needed.
