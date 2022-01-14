# Putting it all together

## Read Class 05

### Joshua McCluskey

### Thinking in React

### What is the `single responsibility` principle and how does it apply to components?

Each componenet should only do one thing.

Tip: Draw boxes around eveything on your mockup or wireframe for compnent hierarchy

### What does it mean to build a ‘static’ version of your application?

Build everything and render it. DO NOT USE STATE FOR STATIC BUILD

### Once you have a static application, what do you need to add?

Make your app interactive and start thinking about state.

Tip: Make a TODO list and figure out which ones are need state.

### What are the three questions you can ask to determine if something is state?

- Is it passed as props from parent?
- Is it unchanged overtime?
- Can it be compute it based on othe state and or props in the compoenent?

### How can you identify where state needs to live?

Find the common owner to best determine where your state will live.

## What is a “higher-order function”?

Functions that operate on other functions passed as arguments or returning a function.

### Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

It is determing if me is greater if a number is greater than 10. Line two is invoiking the function to pass 10. When it is invoke again 10 will be compared.

### Explain how either map or reduce operates, with regards to higher-order functions

It transforms the an array by applying the function to its elements.

[<=== Back](../README.md)
