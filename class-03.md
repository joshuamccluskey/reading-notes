# HTML Lists, CSS Boxes, JS Control Flow

## Read 03

### Joshua McCluskey

#### Ch.3 Lists

##### Ordered Lists

- When every item is numbered in the list
- `<ol>` element for ordered lists
- `<li>` elemen for numbered lists

##### Unordered Lists

- When every item has a bullet point
- `<ul>` element for unordered lists
- `<li>` element for bulleted items

##### Definition lists

- When you have short terms and a definiton
- `<dl>` definition list element where everything will be contained
- `<dt>` is for definition term term being defined
- `<dd>` contains the definintino

#### Nested lists

- A list within a list. Start another list within another list for it to be nested within the list.

- for unordered lists its another item idented under your original list item. It will appear to be white bullet instead of a black bullet

- ordered list instead of a number for the nested list, it will most likely be like a letter

#### Ch.13 Boxes

##### Box Dimensions

- It defaults to size just big enough
- Width and height
- You can specify size with pixels. percentages, and ems

##### Limiting width

- Defning a minimum and maximum width is needed to accomadate different browsers
- It limits how narrow left and right is

##### Limiting Height and Overflowing content

- The same as width but limiting the verticle
- `overflow: hidden;` hides any content that doesn't fit the box
- `overflow: scroll:` allows the user to scrool through the content hidden

##### Border

- every box has one but may not be visible seperates one edge of the box from the other

##### Margin

- margin sit outside the edge of the border. It creates a gap between two boxes

##### Padding

- The space between the content and the border

##### White space

- Important to have space between boxes not to have borders touching

##### Border width and Style

- You can size it as thin, medium, or thick

- Can't use percentages with borders

- Border width can used to make thick but use pixels

##### Border Style  

- `solid`
- `dotted`
- `dashed`
- `double`
- `groove`
- `ridge`
- `outseet`
- `hidden` or `none`

- change for specific size see below

```
border-top-style
border-left-style
border-right-style
border-bottom-style
```

For bordercolor use the following or for specific sides:

```
border-color
border-top-color
border-bottom-color
border-right-color
border-left-color

border: 'n' pixels dotted bluel
```

##### Padding

- Allows to add more space between the content

Use the following to get specific padding

```
padding-top
padding-right
padding-bottom
padding-left
```

##### Margin

- margin and padding
- show and hide boxes

```

margin-top
margin-right
margin-bottom
marign-left

```

These are useful because it will help in the alignment of boxes by definin the margin.

#### Centering content

Try

```

left-margin: auto;
right-margin: auto;

```

- Establish a wdith for the box so it doesn't take the width of the page.

- `text-align: center;` can also set it to center

##### Change Inline/Block

```
display: inline;
display: block;
dispalay: inline-block;
display: none;
```

- Technique to use none is for creating site navigation. It hides the li element so it doesn't shwo the bullets next to it.

#### Hidden Boxes

- `visitbility` hides boxes from the user
- leaves a space, if you don't need a space then use `none

#### Border iamge

- border images

example

```
border-image: url("put URL here
```

#### Rounded Corners

```
border-radius: 5px;
-moz-border-radius: 5px;
-webkit-border-radius: 5px;
```

- you could go even further to create more complex rounded shapes by adding more parameters to the above

#### Review Arrays

- Arrays is a variable with a list of values that are related to each other
- It's advantage is when you don't know how long th list will be

An array literal
```

let food;
food = ['bread', 'milk', 'eggs'];
```

Array constructor is another method

```

let food;
food = ('bread', 
        'milk', 
        'eggs');
```

- Arrays can contain all the data types: numbers, strings, and booleans

#### Changing a value in the array 

```
// Array
let food;
food = ['bread', 'milk', 'eggs'];

// updating the first item
food[0] = 'cheese';

//
let getEl = document.getElementById('food');

getEl.textContent = food[0];
```

#### Ch.4 Descision Loops

- starts with variable called a switich value

- if a switch statement matches then code runs and breaks to stoop from rinning

#### If vs. S

##### If Statements

- Don't need else for it to work
- All of statements have to be checked
- Performance is slower

##### Switch

- Need a default option is nothing matches to switch statement
- Better performance than the if statement
- If it matches, it doesn't need to run anymore

- Using seitch statements think of like levels in a game or gated system where you can't move on till the level they are on is completed.


#### Type Corcion

JS won't output an error instead it will try to make sense of the data type.

` '2' > 1`

Since 2 was a string it turned it into a number

- JS is a weak typing language where a variable doesn't have to declare the data type
- Hard typing languages are languages like C and C# where variables have to denote the data type
- NaN is a number when no number is present

#### Falsy and Truthy statements

- Falsy statement have a false value `false, 0, '', NaN, no assigned value`
- Truthy statements have a true value all strings are true even `0`

#### Checking Equality and Exisitence 

- urnary operator returns one operand
- `false, 0, ''` Can be considered when not using a strict operator
- `null and undefined can be considered when not using a strict operator
- NaN is always flase.

#### Short Circut Values

- Logical operators operate left to right
- They stop once they know if the value is ture or false
- Put code most likely to return true first in `||`
- Put code most likely to return false in `&&`
- Put options with higher processing power last


### Loops

Loops check for true and run again until it is false.

- For loop runs based on a counter for amount of time to run

- While loop best used when you don't know how many times you want it to run until it is false

- Do While is like while but will run the condition at least once and then go until it is false


##### For Loop

Best for looping through an array

Inialization - `let i = 0;`

Condition - `i < 2`

Update - `i++`


- common to see `break` and `continue`

- loops are great for arrays 
- Avoid INFINITE ERRORS

 define the size of the array

```
let counter = [3,2,1];
let arrayLength = counter.length;
```

##### While Loop

- Best for unkonwn amount the loop should run

###### Do While loop

- Best for wanting code to run at least once them repeat until false.




[<== BACK](README.md)
