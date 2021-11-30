# HTML Text, CSS Introduction, and Basic JavaScript Instructions

## Read 02

### Joshua McCluskey

#### Ch.2 Text

- Stuctural markup - describe both headings and paragraphs

- Semantic markup - extra info like quotes, acronyms, and more

##### Headings and paragraphs

- `<h1>` used a main heading
- `<h2>` subheading
- `<h3>` `<h4>` `<h5>` `<h6>` keep going to smaller headings as needed up to `<h6>`

- `<p>` each new paragraph element will have new line and space between it
- `<b></b>` bold
- `<i></i>` itlaics
- `<sup></sup>`superscripts like 4th or power of numbers or exponents
- `<sub></sub>` sub script is under the like footnotes or in H2O
- Whitespace collasping browser will only show one space
- `<br />` line break
- `<hr />` line break between themes
- Visual editors are like word processors
- Code views show you the code of your formatting in the visual editor similar to WordPress sites you write and design visually and then can see the code view to see the backend


##### Bold and Italic , Empahsis

- `<em>` emphasis is made shows in itlaics
- `<blockquote>` is an element that quotes of an enitre block
- mostly used in identfying sections when a screen reader is being used
- `<q>` used for small qoteds
- with quote elements, you can use the cite attribute with link to original source
- `<strong>` is to show strong importance

- `<abbr>` let the reader know that something is an abbriviation and tells the user what it means

- `<cite>` When referencing something in your work can indicate where from legacy use in adding names to citation from HTML 4

- `<dfn>` Whenever a definition is being explained

- `<address>` Can contain any contact informatione
- `<ins>`  insert words with underline

- `<del>` strike through
- `<s>` the actual strike through


### Ch.3 Introducing CSS

- Imagine every element has a box around it.
- CSS the rules to the looks
- Associate elements to the style
- It affects how the elememts are displayed
- You can do multiple elements with the same style seperate with comma
- `<link>` style pages referenced for webpage to refer to are written in head like using Google Fonts. Many things specify the type.

- Internal CSS uses `<style>` element

### Different types of selectors in CSS

- Universal: applies to all elements
- Type: Matches element name
- Class: Matches class value
- ID: Maches ID attribute value
- Child: Matches a direct chold value
- Decendant: Matches decendant of another element
- Adjacent: Matches elments next to specific elements
- General Sibling - Matches element of sibling of another


### CSS Cascades!!!

- Priority given to nearest the top
- You can add `!important;` to over ride order.
- Inherited values save time for child elements 

- External Style Sheets easier to link other pages and use 
0
- There are different versions of CSS
- Tests site on all browsers 
- CSS bug or browser quirk if website is not supported fully



### Ch.2 Basic JavaScript Instructions

- Statements in JS end with `;`
- Code block are contained within curly brackets `{}`
- JS is **Case Sensitive**
- Statements are instructions with its own line and end in semi colon
- `;` indicate a step over for the computer to go to next line of code
- Code blocks help organize numerouse statements

#### **COMMENT**

- it allows others and remind yourself of what the code is doing on a revist.
- `/* Comment here */` Put your comment using this for multiple lines and blocks of code
- `//` single line 

#### Variables

- Allow us to store bits of information and recall it
- The data in variable can change everytime a script runs.
- Variables represent values that can be calculated and computed
- Variables can represent any kind of data type

- `let` for dynamic variables
- `const` for non chaing variables
- `var` legacy 
- write in camelCase
- `=` is an assignment operator


#### Datatypes

- numeric
- string : letters and characters
- boolean : true or false || 0 or 1
- store strings with quotes 
- You could use double quotes and use single quotes withing double quotes
- use `\` back slash to **escape** character in order to use a quote within a quote

#### JS shorthand in variables

```

let name1, name2, name3,;
name1 = "Joe";
name2 = "Jan";
name3 = "Jon";

______________________________

let name1 = "Joe", name2 = "Jan", name3 = "Jon"; 


```

Rules of Naming Variable 

- You can't use numbers in the beggining of name
- case sensitive 
- Name supposed to describe the variable
- camelCase your name







[<== BACK](README.md)
