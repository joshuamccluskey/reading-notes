# Structure Web Pages with HTML

## Read 04

### Joshua McCluskey

#### Wireframe and Design

- Wireframes widely used by UX Designers based on user research
- Sounds like storyboarding in animation
- UX Designers define and plan the design of website, app, or product
- Software Invision or Balsamiq
- Paper and pencil good for the inital stages
- Paper prototypes can test at every stage of ideation and design
- Switiching to software in later stages
-
  - Wireframe > Interactive Prototype > Visual > Design
  - Sketch > Code
  - Sketch > Wireframe > Hi-Def Wireframe > Visual > Code
  - Sketch > Wireframe > Visual > Code

- Do your research
- Develop user personas
- Define Use Cases
- Industry and market research
- Make sure user flow is mapped out user flows or information archietechture
- Draft and Sketch
- Turn Wireframes into prototypes
- Good wireframe:
    1. Clarity
    2. Confidence
    3. Simplicty

#### Mozilla HTML Basics

- HTML is a markup language that deines the structure. HTML consists of a series of element.
- Enclosing tags have avariety of configurations

```
<p>My dog is fluffy</p>
```

- Openining tag = `<p>`
- Closing tag = `</p>`
- Content = My dog is fluffy
- Element = `<p>My dog is fluffy</p>`
- Attribute = `<p class="editor-note">My dog is fluffy</p>
- Nesting elements `<p>My dog is <strong>too</strong> fluffy.</p>`
- Empty elements like an img tag `<a href="https://imgur.com/ERXyM5D"><img src="https://i.imgur.com/ERXyM5D.jpg" title="source: imgur.com" /></a>`
- Anatomy of an HTML document:

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My page </title>
  </head>
  <body>
    <img src="https://i.imgur.com/ERXyM5D.jpg" title="source: imgur.com" />
  </body>
</html>
```

- Images `<img src="https://i.imgur.com/ERXyM5D.jpg" alt="My Photo title="source: imgur.com" />`

- Marking up text for headings `<h1></h1>` replace number for desired heading
- Paragraphs is for containing text. `<p>` This is a single paragraph</p>
`
- Lists- Unordered lists: `<ul>`Ordered Lists: `<ol>` List Item: `<li>`
- <a href="https://www.github.com">GitHub</a>

Href is hypertext reference

#### Semantics

- Semantics is the meaning of code.

Benefits of Semnatic Markup

- Search engines will consider its contents good for SEO Search Engine Optimization
- Screen Readers use it as guide for visually impaired
- Searching for specific blocks easiers than looking for `<div>`
- Suggest what the type of data will be used
- Semanitc naming proper naming of element
- There are roughly 100 Semantic element

[<== BACK](README.md)
