# Lightbulb Selector Template
A foundational component of all modern web browsers is interactivity based around user inputs (e.g. clicks, key strokes, hovering over an icon, etc.). **How do we design pages that respond to user inputs?** 

## JavaScript
**JavaScript** is a  programming language used both on the client-side and server-side that allows you to make web pages interactive. Whereas HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user. When a webpage responds to something you do, chances are JavaScript is the reason for this response.

## Event Listeners and the DOM
**GOAL**: Today we are going to add event listeners to our web pages.

HTML events are **"things"** that happen to HTML elements. Events are things like click, a page has loaded, or a certain key is pressed. When JavaScript is used in HTML pages, JavaScript can **"react"** on these events. [A full list of HTML events can be found here.](https://www.w3schools.com/jsref/dom_obj_event.asp)

When a web page is loaded, the browser creates a **D**ocument **O**bject **M**odel of the page.

The HTML DOM model is constructed as a tree of Objects:
![](/DOM.png)


```javascript
.addEventListener()
```