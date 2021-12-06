# Introductory HTML and Javascript

## Read 01

### Joshua McCluskey

#### Introduction to HTML CSS

- People access the web via a browsers like Chrome, Edge, Safari, Firefox
- Web servers host the websites
- Web hosting is a company that charges a fee to host a website.
- People access the web via moobile, laptop, desktop.
- Screen Readers are programs that read the contents on the screen
- Websiteas are created with HTML and CSS.
- Larger webistes are createdwith PHP, .ASP.Net, Java, and Ruby

#### Ch.1 Structure 

- We look through digital documents everyday and see how they are structured.
- Think of the news articles online and ssee how they are structured 
- Word documents have headings and sub headings
- HTML is the structures of web pages with *elements* and *tags*
- Elements have opening and closing tags that do things with certain information.
- Opening tag has the element `<p>` and closing has a slash `</p>`
- Attributes tells us more about the tag with a *name* and *value*
- `<body>` Is the main element that shows everything in the browser
- `<head>` tells all the information about the page not shown in the body
- `<title>` tells the inforamtion of website in the url location or the tab
- content management system is something that you can manage a website by accessing for control.
- Access view source to see how other sites are built

#### Ch.8 Extra Markup

- There are several versions of HTML over the years.
- Current version is HTML 5
- `<!DOCTYPE html>` tells browser to render in HTML 
- `<!-- comment -->` is how you can write a comment in your HTML
- ID attributes allow you to call sepcific element in HTML
- Class attributes allow you to call multiple elemetns in HTML
- Block level elements start a new line in the display on the browser
- Inline elements are embedded within other elements
- Grouping elements in a block use `<div>`
- `<span>` is an inline element that works like `<div>`
- `<iframe>` is an element to add a window like a google map 
- `<meta>` is an empty element that tells information that is not seen and is read by search engines
- descriptions are 155 words used by search engines
- keywords are user comma sperated words to find your web site
- pragma is used to help ~~not~~ save cache info locally to ease loading of the website.
- expires detaisl when a website is no longer cached. Data must be formmateed as it is shown.

- escape code must be used for certain chracters like copyright, ampersand, currency symbols, quotations, multiply and and divide

#### Ch.17 HTML 5 Layout

- legacy version divided page using `<div>`
- HTML 5 now has elements like `<header>` `<footer>` `<nav>` `<aside>` `<article>`
- `<header>` `<footer>` appear at top and bottom of page
- `<nav>`contains the major navigational block of the sit with a unordered list `<ul>`
- `<article>` used for independent sections. example a page with multiple articles each article will be contained with its own `<article>`
- `<aside>` used like a glossary for an article.
- `<section>` groups related elements together
- `<hgroup>`  groups a related group of example h1 or like h2
- `<figure>` can contain any content referenced from the main flow 
- `<div>` is still used to group elements
- `<a>` in HTML 5 can link an enitre block
- to help older browsers that can't read HTML 5 include the following

CSS:

    ```
    header. section. footer. aside. nav. article. figure. figcaption {display: block;}

    ```

HTML:

```
<!--[if lt IE9]>
    <script src="http://htmlshiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
```


#### Ch.18 Proccess and Design

- Who are you targeting as audience
- Why do they visit your website
- What are they trying to do
- What do they need
- Will they visit often or not
- Organize your site map
- Develop wireframes for rough design layouts
- Using effective design to ensure effective information
- visual hirarchy size, color, style
- navigation design keep it concise and simple

#### Introduction JavaScript Jquery

- Javascript allows to make websites more interactive and accessibile

#### Ch.1 The ABCs of Prgramming 

- Script is a set of instructions
- State goal and write out tasks
- Define
- Design
- Code
- Can use a flowchart to define
- Write out the steps
- Objects are things
- Types are variants of the object
- Events are specific moments that computers pay attention to 
- Methods contains steps or instructions
- You script with HTML CSS and JavaScript for a website
- They all can be added several ways

[<== BACK](reading-notes/README.md)
