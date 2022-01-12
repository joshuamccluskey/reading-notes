# Passing Functions as Props

## Read Class 03

### Joshua McCluskey

## Lists and Keys

- What does .map() return?
  It returns an array and in React we can return a list of elements.

- If I want to loop through an array and display each value in JSX, how do I do that in React?
  You can use JavaScripts map().

- Each list item needs a unique __Key__.
  
- What is the purpose of a key?
  It helps react find items when they have been changes, added, or removed. Best to use unique stable IDs that are strings if possible and don't reccomend using index.

## Spread Operator

- What is the spread operator?
  It is an ES6 operator  `...` that expand an object into a list of arguments

- List 4 things that the spread operator can do
  1. It can spread an array into seperate arguments.
  2. Helps in copying an arrray
  3. helps in concanting arrays
  4. Helps in adding a state in React

- Give an example of using the spread operator to combine two arrays
  Concanting array: syntax : `let combinedArr = [...arr1,...arr2] ; console.log(...combinedArr)`

- Give an example of using the spread operator to add a new item to an array.
  Adding new item: syntrax : `let newItems = [item1, item2,...arr1]`

- Give an example of using the spread operator to combine two objects into one.
  Examople of combining objects syntax:

  ```javascript
  let obj1 = {obj1: 1}
  let obj2 = {obj2: 2}
  let obj3 = {...obj1, ...obj2, obj3: 3}
  let obj4 = {...obj1, ...obj2, obj3: () => {console.log(3.repeat(8))}}
  obj4.obj3()
  ```

## Video

- In the video, what is the first step that the developer does to pass functions between components?
  Create the fucntion in the state that you want to change. example `increment()`
  
- In your own words, what does the increment function do?
  It is a loop for objects within react.
  
- How can you pass a method from a parent component into a child component?
  Example in the parent compnent add the method and in the object `method1={this.method1}`
  
- How does the child component invoke a method that was passed to it from a parent component?
  In the child component invoke method example `this.props.method1()`
  In handeler example `OnClick={thos.method1()}`

[<=== Back](../README.md)
