# HTML Table; JS Constructor Functions

## Read 07

### Joshua McCluskey

#### Domain Modeling

- Domain modeling is creating a solution for a specific problem
- Object-Oriented Model: Store data in properties and has behavior as methods
- Articel say  to write out the code in article see link for reference and citations the follwoing code is not mine
[Reference link] (https://github.com/codefellows/domain_modeling#domain-modeling)

  ```
  // Article says to write out the code in article see link for reference and citations the follwoing code is not mine
  // https://github.com/codefellows/domain_modeling#domain-modeling
  
  var EpicFailVideo =  fucntion(epicRating, hasAnimals) {
    this.epicRating = epicRating;
    this.hasAnimals = hasAnimals;

  }
var parkourFail = new EpicFailVideo(7, false);
var corgiFail - new EpicFailVideo(4, true);

console.log(parhourFail);
console.log(corgiFail);

```

- The top line is a contructor finction
- Stroing data within properties allows us to call on it later in the next lines
- Using new **Instanitates** or creates
- Using contructor function **initalized**  by call the constructor fucntion.
- 
```
 // Article says to write out the code in article see link for reference and citations the follwoing code is not mine
  // https://github.com/codefellows/domain_modeling#domain-modeling

Epic Fail Video.prototype.gnerateRandom = function (min,max) {
  return Math.floor(Math.random() * (max-min +1)) + min;
}

```

- Use prototype when using a method with a construtor fucntion


```
 // Article says to write out the code in article see link for reference and citations the follwoing code is not mine
  // https://github.com/codefellows/domain_modeling#domain-modeling
EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}
```


```
 // Article says to write out the code in article see link for reference and citations the follwoing code is not mine
  // https://github.com/codefellows/domain_modeling#domain-modeling

EpicFailVideo.prototype.weeklyLikes = function() {
  var total = 0;

  for (var i = 0; i < 7; i++) {
    total += this.dailyLikes();
  }

  return total;
}
```

- Create an instance using new keyword and call constructor fucntion
- Use this vaiable to acce object properties and methods



#### Ch. 6 Tables 

Like Excel and Google Sheets

- Table is a grid format that organizes information.
- `<table>` 
- `<tr>` table row
- `<td>` table data or cell
- `<th>` table headings
- `colspan` used it need data across columns
- `rowspan` used across rows
- `<theads>` column headds use this
- `<tbody>` main area
- `<tfoot>` bottom maybe for like a total result

#### Ch. 3 Functions, Method, and Objects


 function that can be set up with multiple objects to call upon, I see this useful when a for is being submitted

syntax of creating an instance
` let variable = new constructorFunction (arguments)`

- Consrtuctor syntax

``` 
let variable = new Object();
variable.name
varibale.age
variable.hobbies

variable.functionName = function( {
  return this.name;
})
```

use `delete` to remove property

Literal notation using a the same template and re writing it

Object constructor notaton creationg variables that can be arugments foe the function.

`this` is used a with inside functions and objects

Data is represented by name value pairs

- Arrays are objects
- Arrays of objects and objects in arrays
- Bulit in objects are in browsers
  - Browser Object Model : window object
  - Document Object Model: DOM mainpulating content on page or retrieveing info
  - Global JS Objects: built into JS
  - Math Objects for math functions and random numbers
  - Create instance of a date using date object time day 

-You can pretty much figure out how to do something with built in methods and if you can't find one, you can build a method to complete the task.
