# HTML Links, CSS Layout, JS Functions

## Read 04

### Joshua McCluskey

#### Ch.3 Links

- Allow you to move to another web site, web page, section of page, links that open browser and email
- `<a>` link element
- `<a href="URL">Text</a>`
- link to other sites `<a href="website URL">Text</a>` This is an absolute url
- link to other pages `<a href="Page.html">Text</a>` This is a relative url
- Place pages into of different sections in their own folder for big websites
- top level folder is the root
- parent is top level and low level folders are childeren
- homepage always index.html
- URL Uniform Resource locator
- Each section or subdirectory should have it own index.html and pages associated with that section
- Relative URL Shorthand
```
<a href="file path">Text</a>`
```

Open link new window:

Add `target="_blank"` attribute

Linking ot specific part of the page use IDs

`<h1 id='up'>`

`<a href="#up">`

Add Ids to go to specific parts of other websited similar to above

### Layout

- positioning elements
- screen sizes
- fixed width and liquid layouts
- Grids for designing

- CSS treats everything in HTMl with its own box
  - Block level elements start a new line
  - Inline element internal , within, around, between text 

-Box on the outside is a containing element or parent element

#### Positioning 

- Normal flow - position static
- Relative Positioning - position relative
- Absolute Position - position abosolute
- Fixed Position - position fixed
- Floating elements - allows to go left or right tons of other specifcs you can do with float
- Overlapping elements - Zindex prevents overlapping of the elements


#### Screen Sizes

Different visitors will have different devices and different screen resolutions

Web designers tend to design at 960 - 1000 pixels


#### Fixed width layouts

Does not change the layout as window size is adjusted by the user

#### Liquid layouts 

Change size as windo is changed


#### CSS Frameworks

- Takes common taks and makes them easier to use
- saves time
- avoids browser bugs

### 960 Grid.GS

### import style sheets

`@import url("file name")`


### Ch.3 Functions, Methods, and Objects

- Functions are series of objects
- Methods are the same as functions but part of the object
- Objects are made of up of properties and methods or you can create your own
- Built in object- it introduces you to a number of objects

#### Functions
- a series of steps that allow you perform a task.
- reduces redudant code
- delclare the function `function name (){}`
- call the function `functionName ();`
- Parameteers are values needs for the function and return values is the value returned for it to work.

 ```
 function name (param1, param2){}
 ```

Arguments are values to provde to the function parameters

Functins can return a single value

`return`

functions can reutrn multiple values using an array

- Functions can be used based on scope
- Local scope it can't be used any where outside of where it was locally declared
- Global scope can call upan a function wherever.

- Global variables use more memory
- local variables make thing proccess faster due to short term memory usage
- avoid using the same letter more than once.

-
### Advantages of paired programming

- Greater efficency
- Engaged colloboration
- Learning from fellow students
- Social skills
- Job interview readiness
- Work environment readiness


[<== BACK](README.md)
