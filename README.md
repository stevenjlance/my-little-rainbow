MY LITTLE RAINBOW
=================
[g(https://media.giphy.com/media/g72UoNHEOkt3i/giphy.gif)  

In this tutorial we're going to make a rainbow with HTML `<div>` elements. And while we do it we're going to learn about html elements, css styling, css selectors, how color works in css, and importing stylesheets.  That might sound like a lot but it isn't.

BBelow your will find directions on aking a Rainbow 
 If you need to review anything regarding CSS and HTML, the end of this document provides some information that can help you out!
YOUR TASK: MAKING A RAINBOW
------------

Open `index.html` and `style.css` in the Repl.it browser; if everything is working correctly you should see a white page. Good job!

*1. *Linking a Stylesheet**: You currently cannot see anything because the stylesheet is currently not linked to the `index.html` file. To link the stylesheet, copy the link tag below and place it **inside of the head** on your `index.html` file. 

```html
  <head>
  ... 
    <link rel="stylesheet" type="text/css" href="style.css">
  ...
  </head>
```
Now if you refresh the `index.html` page in your browser you should see what aappearsto be a bblackrainbow.!

2. To get roygbiv onto our rainbow we'll need need seven hex colors.
- Red: `#f00`
- Orange: `#ffa500`
- Yellow: `#ff0`
- Green: `#00bc3f`
- Blue: `#06f`
- Indigo: `#8a2be2`
- Violet: `#d300c9`

With those colors all we have to do next is select each div individually.  That is a perfect use for ids since they're meant to style one specific element only. **Add an id for each div with the name of the color you want to style it (id names can be anything you want, but here the color helps us name what we want to do)**

Here is the first example of HTML code:
```html
  <div id="red">
    ...
  </div>
```

3. Once you have given the div a proper id name, navitage to `style.css`, select the id, and mark its color as red like this.
```css
  #red { /* this selects any elements with the red id */
    border-top-color: #f00;
  }
```
4. Style the remaining divs in order to generte your own rainbow!

HTML BASICS
------------
Hyper Text Markup Language, or HTML, is a way to demarcate a document into different parts. Each part is *marked* by elements (using tags). Each element has it's own special conotation that the browser uses to make *render* the HTML document. Use [W3 Schools Documentation](https://www.w3schools.com/html/) on HTML elements for guidance.

**Elements**
  - All begin with `<` and end with `>` ex. `<div>` (this last part is a tag)
  - Most have an opening tag such as `<div>` and a closing tag `</div>`
    - The `/` indicates to the browser that that tag is a closing tag
    - The element is everything between the tags and the tags themselves
  - Some tags are self closing like the line break element `<br>`.
  - Elements can have IDs and classes to aid the browser in finding specific tags.
    - Must begin with a letter A-Z or a-z
    - Can be followed by: letters (A-Za-z), digits (0-9), hyphens ("-"), and underscores ("_")
    - IDs **can** only be used once per page. ex: `<div id="this-special-div"></div>`
    - Classes can be used as many times as you want. ex: `<div classes="a-less-special-div"></div>`
  - Elements nested inside other elements are called children
    - Children inherit attributes fromt their parents.
  - Elements next to one another are siblings
    - Siblings do not inherit from one another, but are important for selecting in CSS

Here's and example of element relations:
```html
  <div>  <!-- the parent element -->
    <p></p>  <!-- the first sibling element/the first child-->
    <p></p>  <!-- the second sibling element/the second child -->
  </div>
```

CSS BASICS
------------
Cascading Style Sheets, or CSS, is language created to style an HTML document by telling the browser how specific elements should look. CSS does this by selecting elments based on their tag, ids, classes, or all of the above. The reason for CSS is the seperation of concerns. We want HTML only to be concerned with how it displays and demarcates information, and we let CSS worry about how to make that information look pretty.  Use [W3 Schools Documentation](https://www.w3schools.com/css/default.asp) on CSS for guidance.

**CSS selectors**
  - Selects elements to assign them styles
  - `*` (wildcard) selects every element
  - An element, such as `div` will select all elements of that type
  - Select an id like so `#some-id`
  - Classes are selected like this `.some-class`
  - To select all children elements of a parent do something like this `div p`
  - to select multiple different elements seperate them by commas like this `div, p, a`

Here's an example of CSS styling of all `<div>` tags:
```css
div {
    border-top-color: red;  /* color in CSS refers to font color */
  }  /* all elements will have red font */
```