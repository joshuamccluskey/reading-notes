# Design Web Pages with CSS

## Read 05

### Joshua McCluskey

#### What is CSS?

- CSS Casacading Style Sheets makes everything look good
- Browser defaults will style HTML documents via internal stylesheets

#### What is CSS for?

- A document is has markup language on it mostly HTML also SVG and XML
- Presenting Browsers desinged to visually display for audience
- User agent can be a browser 
- CSS used to change color and size of headings and 
- CSS can mmake a layout
- CSS can animate

#### CSS Syntax

- CSS is a rule based language
- Selector selects which HTML element to style
- `{}` contain declarations = property and value pairs
- Before `:` = Proerty
- After `:` = value
- Color Values
- font-size

#### How to add CSS

External CSS

Use a .css  file 

```
body {
  background-color: green;
}

h1 {
  color: Yellow;
  margin-left: 10px;
}
```
-

#### Internal CSS

Within your HTML file
```
<style>
body {
  background-color: green;
}

h1 {
  color: Yellow;
  margin-left: 10px;
}
</style>
```

#### Inline CSS

Withion your HTML  tags

```
<h1 style="color:blue;text-align:center;">This is a heading</h1>
```

### Multiple Style Sheets and Cascading Order

- For multiple  sheets value from last read style sheet will be read.
- Cascading ordrerwill be used for priority of being read  depending on method
    - Inline Syle
    - External Style
    - Browser Default

#### CSS Color

- CSS color syntax `color: color|initial|inherit;`

Examples of formats:

- HEX Value `body {color: #99999;}`
- RGB `body {color(0,0,0);}`
- RGBA `body {color(0,0,0,0);}`
- HSL `body {color(0%,0%,0%);}`
- HSLA `body {color(0%,0%,0%,0.0);}`

[<=== BACK](reading-notes/README.md)
