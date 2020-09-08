# Lightbulb Selector Template
A foundational component of all modern web browsers is interactivity based around user inputs (e.g. clicks, key strokes, hovering over an icon, etc.). **How do we design pages that respond to user inputs?** 

## JavaScript
**JavaScript** is a  programming language used both on the client-side and server-side that allows you to make web pages interactive. Whereas HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user. When a webpage responds to something you do, chances are JavaScript is the reason for this response.

## Event Listeners and the DOM
**GOAL**: Today we are going to add event listeners to our web pages.

HTML events are **"things"** that happen to HTML elements. Events are things like click, a page has loaded, or a certain key is pressed. When JavaScript is used in HTML pages, JavaScript can **"react"** on these events. [A full list of HTML events can be found here.](https://www.w3schools.com/jsref/dom_obj_event.asp)

When a web page is loaded, the browser creates a **D**ocument **O**bject **M**odel of the page otherwise known as the DOM.

The HTML DOM model is constructed as a tree of Objects. Here is an example of the DOM for a basic webpage:
![](https://github.com/stevenjlance/Lightbulb/blob/master/DOM.png?raw=true)

## How to Add Event Listeners
To attach an event listener, we need to do two steps.  
1. First, we need to select the HTML element using `document.querySelector()`. Inside of the paentheses we put the element name, class, or id that we wish to select for. For example, if we wanted to select for the following HTML element:
```html
<h2 id="myHeader">Click Me</h2>
```
We would do the following:
```javascript
// Must say var. The name header can be whatever name you want. Inside the parentheses goes the ID name.
var header = document.querySelector('#myHeader');`
```
**NOTE**: To select for a class we would use .name-of-class and to select for html elements we would just use the name of the element (e.g. h2).  
2. Once we have selected for the HTML element, we attach an event listener by doing the following:
```javascript
header.addEventListener("click", function() {
  console.log("Clicked");
})
```
This code attaches an event listener to the h2 HTML that we selected for with the query selector. 

3. When this code is run, the message "Clicked" would be logged in the JavaScript console everytime that this h2 header is clicked.

## Update classList
For this lab, we will be updating the classes that are attached to the element. If you open the `index.html` file you will see that the first lightbulb has a class of active whereas bulbs 2 and 3 do not have this class of active. If you add active to the other bulbs, you'll see they now have the "on" effect due to the CSS style rules that have already been written.

**classList**: Edit the `script.js` file to add these two new outputs underneath our first selected element. 
```javascript
var firstBulb = document.querySelector('#lightbulb1') // Get the bulb using the same selector syntax we use for CSS selectors.
console.log(firstBulb) // Make sure you got the bulb.
console.log(firstBulb.id) // Read the ID property - proves that there's more to the object than just the HTML
console.log(firstBulb.classList) // Examine the list of classes assigned to the first bulb
```
You'll see in the console that the classes attached to bulb 1 and the ID have printed. We can use this to either add or remove classes!

**REMOVE A CLASS**: To remove a class, we would do the following
```javascript
var light1 = document.querySelector("#lightbulb1);
light1.addEventListener("click",function() {
  light1.classList.remove('active')
})
```

**ADD A CLASS**: To add a class, we would do the following
```javascript
var light1 = document.querySelector("#lightbulb1);
light1.addEventListener("click",function() {
  light1.classList.remove('active');
})
```

**TOGGLE A CLASS**: The functionality you built out is awesome! But what if we want to alternate between on and off? There's a third method related to `.add()` and `.remove()` that makes it a LOT easier to add if a class is missing and remove the class if it is present. The method `.toggle()` means flip this thing on or off, like a switch.
```javascript
var light1 = document.querySelector("#lightbulb1);
light1.addEventListener("click",function() {
  light1.classList.toggle('active');
})
```
When executed, this code will either add active to the lightbulb if it does not have class of active or remove the class if it does have a class of active currently.

## Extensions!
- Get all three bulbs to turn on and off when clicked!
- Switch the three-bulb setup to tacos, burgers, pizza, and any other emoji, and refactor the code to match.
- Look up other event listeners. Rewrite this code to make any object active if your mouse has entered the object. Then add functionality for if your mouse exits the object.
- **CHALLENGE PUZZLE**: Add more bulbs to the page and get one bulb to turn off multiple bulbs. E.g. if you click bulb 1 it alters the class of bulbs 1, 2, and 5.
