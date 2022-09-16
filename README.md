# GD3 Coding tutorials 2022-2023

Over the course of the 16-week semester, there will be 4 remote code tutorials to help you develop your interface for the assignment *An Atlas on the web*. Each of these 4 tutorials will focus on a different topic and will be punctuated with exercises to allow you to implement the skills you have learned.

## Table of contents

- [Schedule](#schedule)
- [Learning Javascript](#learning-javascript)
	- [Functions](#functions)
	- [Events](#events)
	- [Variables](#variables)
	- [Selectors](#selectors)
	- [Properties and methods](#properties-and-methods)
	- [Conditions](#conditions)

## Schedule

### Tutorials #1

https://github.com/quentin-f451/gd3-coding-tutorials-1

- **Dates:** 15.09.2022 (Sem 1) / 16.02.2023 (Sem 2)
- **Keywords:** Git, HTML, CSS, Javascript, Functions, Events
We will go back to the basics of the web, learn how to create a clean coding environment in HTML/CSS/JS using Github as our versioning tool and start with the basics of Javascript.

### Tutorials #2

- **Dates:** 29.09.2022 (Sem 1) / 09.03.2023 (Sem 2)
- **Keywords:** Javascript, Objects, Arrays, JSON, API, Fetch

We will explore how to use Javascript and JSON as a tool to store, retrieve and process data on the web.

### Tutorials #3

- **Dates:** 10.11.2022 (Sem 1) / 13.04.2023 (Sem 2)
- **Keywords:** Javascript, Bundling, Preprocessing, Server/Client
We will explore how to use Javascript as a tool to create HTML and understand how we can work with it to enhance our development tools.

### Tutorials #4

- **Dates:** 24.11.2022 (Sem 1) / 11.05.2023 (Sem 2)
- **Keywords:** CSS, Media queries, CSS-to-print

We will explore how we can use CSS to adjust and transform a web interface into a _ready-to-print_ file.

***

## Learning Javascript

JavaScript (JS) is a programming language. It is built on the relationship between events and functions. A function only works as it is connected to an event.

> ⚠️ Every bit of code in this tutorial is written in *Javascript ES6*, a contemporary version of Javascript. You might find on the web other ways to do the same things, either with older versions of JS or in JQuery for example, but I would advise to stick to plain Javascript for the Coding lesson.

### Some advices to start

- Always write what you want to achieve in English before you write things in JS.
- Try to divide your code as much as possible in order to make it more readable and easier to reuse.
- Name things with accuracy, you're not limited with length when you create a variable or a function.
- DRY principle: Don't Repeat Yourself. Where you repeat things, there's a function to create.

***

### Functions

#### Create a simple function

```js
const nameOfMyFunction = () => {
  // Content of my function
}
```

#### Create a function with parameters

```js
const nameOfMyFunction = (parameter1, parameter2) => {
  // Content of my function
};
```

#### Call a function that should be triggered when the page is loaded

```js
// Complete version
window.addEventListener('DOMContentLoaded', () => {
  nameOfMyFunction();
});

// Shortcut
nameOfMyFunction();
```

#### Trigger a function with arguments

```js
nameOfMyFunction(10, 20);
```

#### Return a result from a function

```js
const sum = sumOfTwoNumbers(10, 20);
const sumOfTwoNumbers = (a, b) => {
  return a + b;
}
```

***

### Events

You can find a complete list of events [here](https://developer.mozilla.org/en-US/docs/Web/API/Element#events).

#### List of events (interesting for you)

- On `document` : `dragend`, `dragenter`, `dragleave`, `dragover`, `dragstart`, `drag`, `drop`, `keypress`, `keydown`, `keyup`, `scroll`, `wheel`
- On `window` : `DOMContentLoaded`, `resize`
- On any element: `blur`, `click`, `dblclick`, `focus`, `mousedown`, `mouseenter`, `mouseleave`, `mousemove`, `mouseup`, `scroll`, `select`

#### Setup an event listener

```js
document.addEventListener('scroll', () => {
  // Content of my function
});
```

***

### Variables

#### Create a variable

```js
// For a constant variable (that doesn’t change)
const myVariable = 'value';

// For a changing variable (that can change)
let myVariable = 'value';
```

#### Modify a variable

```js
myVariable = 'new value';
```

#### The 5 types of variables

```js
const string = 'Text'; // String (a text)
const number = 10; // Number or Integer (a non-decimal number)
const float = 1.5; // Float (a decimal number)
const boolean = true; // Boolean (can be true or false)
const array = [10, 20, 30, 40, 50]; // Array (a list or a table)
```

#### Show a variable in the console

```js
console.log(myVariable)
```

> ⚠️ Open the console with `Cmd` + `Alt` + `I` or `Ctrl` + `Alt` + `I`

***

### Selectors

#### Get a single element from the document

```js
const div = document.querySelector('div'); // With a tag
const title = document.querySelector('.title'); // With a class
const item = document.querySelector('#item'); // With an ID
const text = document.querySelector('.title + .text'); // With a CSS selector
```

#### Get multiple elements from the document

```js
const items = document.querySelectorAll('.item');
```

> ⚠️ You can’t apply a function or an event to multiple elements at a time. You need to loop through the array of items to apply it to each element.

```js
const items = document.querySelectorAll('.item');
items.forEach((item) => {
  item.style.color = 'red';
});
```

***

### Properties and methods

You can find a complete list of properties and methods [here](https://developer.mozilla.org/en-US/docs/Web/API/Element#properties).

#### Standard properties

```js
const item = document.querySelector('.item');
const text = item.innerHTML; // Read the property
item.innerHTML = 'Text'; // Write the property
```

#### Methods

```js
const item = document.querySelector('.item');
item.remove();
```

#### Read-only properties

```js
const item = document.querySelector('.item');
const classes = item.classList; // Read the property
```

> ⚠️ You can only read a read-only property. To write it, you’ll need to use methods.

```js
item.classList.add('active'); // Add a class
item.classList.remove('active'); // Remove a class
item.classList.toggle('active'); // Toggle a class
item.classList.replace('active', 'inactive'); // Replace a class
```

***

### Conditions

#### Create a simple conditional statement

```js
const number = 3;

if (number > 4) {
  console.log('The number is bigger than 4.');
}
```

#### Create a conditional statement with else

```js
const number = 3;

if (number > 4) {
  console.log('The number is bigger than 4.');
} else {
  console.log('The number is not bigger than 4.');
}
```

#### Create a conditional statement with else if

```js
const number = 3;

if (number > 4) {
  console.log('The number is bigger than 4.');
} else if (number < 4) {
  console.log('The number is smaller than 4.');
} else if (number == 4) {
  console.log('The number is equal to 4.');
}
```

#### Check that multiple conditions are true

```js
const number = 6;

if (number > 4 && number <= 10) {
  console.log('The number is bigger than 4 and smaller than or equal to 10.');
}
```

#### Check that one of the conditions is true

```js
const number = 6;

if (number < 2 || number > 10) {
  console.log('The number is smaller than 2 or bigger than 10.');
}
```

#### Check that the condition is false

```js
var number = 6;

if (!number < 4) {
  console.log('The number is not smaller than 4');
}
```
