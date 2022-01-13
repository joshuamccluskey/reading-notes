# React and Forms

## Read Class 04

### Joshua McCluskey

### Forms

#### What is a ‘Controlled Component’?

An input form's value controlled by React. Mutable states is updated with `setState()`

#### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why

The displayed value or input is `this.state.value` and `handleChange` runs on every key stroke it will update the React state. When the user enters a value React state will be updated.

#### How do we target what the user is entering if we have an event handler on an input field?

Have the handler function based on the input's name and perform actions based on `event.target.name`.

### Ternary Operator FTW

#### Why would we use a ternary operator?

It is a conditional statement with a true false outcome.
__WTF__ syntax: **W**hat's the condition `?` **T**rue output `:` **F**alse output `;`

#### Rewrite the following statement using a ternary statement

```Javascript
//Refactor the following into ternary
if(x===y){
  console.log(true);
} else {
  console.log(false);
}

```

```Javascript
//Ternary Operator
x===y ? true : false;

```

[<=== Back](../README.md)
