# JS Object Literals

## READ 06

### Joshua McCluskey

#### Understanding The Problem Domain Is The Hardest Part Of Programming

More questions as to what a problem domain is after reading this article. Writer needs more clarity to convey point or maybe that was the pont the problem domain is not clear. Will do more research.

Problem Domain is like  if you were building a website on a team and you were in charge of figuring out a paticular feature or set of features. In charge of a websites log in and prblem domain would be authentication. 

#### What's the difference between primitive values and object rederence in JavaScrip?

###### 8 data types

- boolean
- null
- undefined
- number
- BigInt
- string
- symbol
- objects

##### Value vs Reference:

Value is directly assigned to the variable 

Where as a reference is a vairable is connected to an object instead of a value.


##### Immutable vs Mutable Data

Primiative vaules are immutable

Object references are mutable

Trying to change letter in a string in a immutable value cannot be done/ 

If values are in an array as an object they can be changed and are mutable.

Basically an object arrray can be changed mutable but it has an object on the value of the array ex. `[name: 'Josh']` instead of just `['Josh']` and the value cannot be changed in  is immutable `let name = 'Josh'`

#### Ch 3. Object Literal

- In an object variables become known as a property 

- In an object variables become known as methods

prperties are like variables with one value

methods are like functions with an object assigned to it.

```

let accountInfo = {
  userName: Joe123
  firstName: Joe
  lastName: Doe
  age: 25
  passcode: 1234
  accountProfile: function(){
    return this.userName;
  }
}
```

Dot notation allows you to call upon a method

example:

`let logIn = accountInfo.userInfo;`

`let logIn = accountInfo.accountProfile();`

- You can also replace dot notation with brackets

`let logIn = accountInfo[userInfo];` 

used when a name usually has special characters like a dash. Shouldn't write like this all the time.

#### Ch. 5 Document Object Model 

It specifies how a browser should create an HTML to be displayed

DOM are stored in the browsers memory and have 4 nodes.

- Document Node
- Element Node
- Attribut Node
- Text Nodes


Accessing the elements:

- `getElementbyId();`
- `queryselector();`

- `parentNode`

DOM queries may return an element or a NodeList.


- `getElementbyId();`
- `queryselector();`

Above can both search a document and return a single element

You can do this with all elements, attributes, classes, css selectors

You can loop through a node list and traverse through a node.

You can go through parent, sibling and childe 


You can update element content like a text node.

You can add remove HTML content

You can `createElement()` as a form of DOM manipulation or remove elements


### Be aware of XSS corss site scripting

- A hacker can access your accounts.


- Protect by validating input in the server

- make sure they can input certain characters and limit visibility on the page.

[<== BACK](../README.md)
