# Functional Programming

## Read Class 08

### Joshua McCluskey

- What is functional programming?
It is a style of building the structure and elements of computer programs. The approch is the evaluation fo mathematical functions and avoids chagning state and mutable data.

- What is a pure function and how do we know if something is a pure function?
It returns the same results when given the same arguments. And you don't see and side effects when observed

- What are the benefits of a pure function?
  THey are stable, consistent and predicatable. When given the same arguments they will always give the same results

- What is immutability?
  I. is unchanging over time or unable to be changed

- What is Referential transparency?
  When a functionsl consistently yeilds the same result for the same input, it is referentiallytrasnsparent

## Node JS

- What is a module?
  A piece of code that has defined function that can be called upon whenever you need to use it. It's in another js file.
  
- What does the word ‘require’ do?
  `require('./moduleNme')` in your App.js so you can use the moduel in your App.js file. basically imports the file into the file you want.

- How do we bring another module into the file the we are working in?
  `module.exports = functionName;`

- What do we have to do to make a module available?
  `var functionName = require('/mopduleName);`

#### Things I want to learn more about

Understanding the difference between modules and components. Is Node.js call these modules and React calles them componenets?

[<=== Back](../README.md)
