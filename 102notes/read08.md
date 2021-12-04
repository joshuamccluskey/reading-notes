# Operators and Loops

## Read 08

### Joshua McCluskey


### Loops and iteration 

- Loops are used to repeat something
- Reapeat an action for nubmer specified
- Zero can be a number in the loop


#### Types of JavaScript loop statements

##### `for` statement

`for` statements run until condition is false. Similar to Java and C `for` loops.

```
for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement
```

##### `do...while` statement

Repeats until condition is false

```
do
  statement
while (condition);
```
Example:

"i" initializes and is given a value of 0 

```
let i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

### Do NOT execute an infinite loop

```
// Infinite loops are bad!
while (true) {
  console.log('Hello, world!');
}
```

##### `labeled` statement

It allows you to put an idenitfier on a loop to call it in other parts of program

##### `break` statement

It is used to terminate a statement. Using break without the labwl it terminates the inner most loop.
If used with the the label, it terminates the specified label.


```
break;
break [label];
```

Example

```
for (let i = 0; i < a.length; i++) {
  if (a[i] === theValue) {
    break;
  }
}

```
labelCancelLoops: while (true) {
  console.log('Outer loops: ' + x);
  x += 1;
  z = 1;
  while (true) {
    console.log('Inner loops: ' + z);
    z += 1;
    if (z === 10 && x === 10) {
      break labelCancelLoops;
    ```


#### `continue` statement

Used to restart

```
continue [label];
```

##### `for...in` statement

```
for (variable in object)
  statement
```

#### USE `for` statement for iterating over arrays


#### `for of`

for iterable objects Array Map Set
arguements

```
for (variable of object)
  statement
```
`for..in` iterates over property names
`for...of` iterates over property  values

### Expressions

- Any unit of code that comes to a value
- Every syntactically valid expression resolves to a value
- Two types: 
    - With Side effects assigning a value
    - Evaluate and resolve a value

#### Types of expressions

- Arithmitic
- String
- Logical
- Primary Expressions
- Lefthand side expressions

### Primary expressions 

- `this` refers to current project or calling object in method
- `()` grouping operator to overrride precedence in order
- `new` left hand side expression create instance of user defined object type
- `super` call object parent.

[<=== BACK](reading-notes/README.md)
