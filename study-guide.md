What is the purpose of the doctype command? (Lesson 1.1)
Doctype is a command for the browser. The purpose of doctype is to make sure the browser is parsing on the most recent version of html. 

What is a <head> element? (Lesson 1.1)
A head element is where we put document metadata.
  
What is semantic HTML, and why is it important? (Lesson 1.2)
Semantic HTML is important so that visually imparred users can access websites using screenreaders. It is also important so that when you are working with other developers, they know whats going on. 

What is the difference between classes and IDs in HTML and CSS? (Lesson 1.3)
The difference between an ID and a class is that an ID can be used to identify one element, whereas a class can be used to identify more than one.

What does * { box-sizing: border-box; } do? What are its advantages? (Lesson 1.3)
Border and padding are included in the width and height. It helps make responsive layouts more managable.

How is an inline element different from a block level element? (Lesson 1.4)
An inline element – for example, a, strong, em, or span – doesn't start on a new line and usually does not contain additional elements, but instead just contains text. You can't explicitly set the width, height, margin, or padding of an inline element; instead, its dimensions are determined by how much space its contents require.A block-level element has the opposite qualities. It gets displayed on a new line (and takes up the whole available line), may contain additional block-level or inline elements, and its height and width can be explicitly set.

What's an example of a situation where you would use a <form> element? (Lesson 1.5)
 
  
What are media queries? (Lesson 1.6)
Media queries are a tool that CSS gives us to apply blocks of CSS rules to only certain viewports. So on a single stylesheet, we can specify how things should look at one viewport size and specify a different layout and appearance at a different viewport size.

Why are grids valuable? (Lesson 1.6)


What is a function? (Lesson 2.2)
A function describes a repeatable process or behavior


## HTML

### Create valid, semantic, accessible HTML

Note in particular the use of semantic elements like `header`, `section`, and `footer`, and the use of the `lang` and `role` attributes, which are accessibility must haves.

Setting this value to en tells the browser that the main language for the document is English so screen readers will choose the appropriate voice when reading it aloud.
Roles tell a browser, "This is the kind of job my content is supposed to do." They make it easier for screen reader users to understand what is on the page and how to use it.

```html
<!DOCTYPE html>
<html lang="en">
  <head><title>My Awesome Page</title></head>
  <body>
    <header role="banner">
      <h1>Welcome to Thinkful!</h1>
    </header>
    <section>
      <h2>This is a section header!</h2>
      <p>Your lorum ipsum text copy goes here. Your lorum ipsum text copy goes here. Your lorum ipsum text copy goes here.</p>
      <p>More lorum ipsum goes here. More lorum ipsum goes here. More lorum ipsum goes here. More lorum ipsum goes here.</p>
    </section>
    <footer role="contentinfo">
      <p>This is where my contact links and copyright info go.</p>
    </footer>
  </body>
</html>

```

### Link to an external CSS file in your HTML

```html
<html lang="en">
  <head>
    <title>My Awesome Page</title>
  <link rel="stylesheet" type="text/css" href="./main.css">
  </head>
  <!-- other stuff -->
```


## CSS

### Select a CSS id

```css
#main-form {
  color: #3c3c3c;
}
```

### Select a CSS class

```css
.special {
  color: #red;
  font-size: 1.2em;
}
```

### Center a block level element

```css
.centered-block {
  margin-left: auto;
  margin-right: auto;
}
```

### Center an inline element

```css
.centered-inline {
  text-align: center;
}
```

### Use the display property

Be able to explain and demonstrate the following values for the `display` property:

* `inline`
An inline element – for example, a, strong, em, or span – doesn't start on a new line and usually does not contain additional elements, but instead just contains text. You can't explicitly set the width, height, margin, or padding of an inline element; instead, its dimensions are determined by how much space its contents require.
p {
  max-width: 450px;
}

* `block`
A block-level element has the opposite qualities. It gets displayed on a new line (and takes up the whole available line), may contain additional block-level or inline elements, and its height and width can be explicitly set. 

.inner-one {
   height: 100px;
   background-color: blue;
}

.inner-two {
  width: 50%;
  height: 100px;
  background-color: green;
}

* `inline-block`
An inline-block element displays inline like a span or a element, but you can give it an explicit width, height, margin, and padding. 
.inner {
  height: 100px;
  width: 25%;
  display: inline-block;
}


### Use the position property

Be able to explain and demonstrate the following values for the position property:

* `static`
Any HTML element with the position: static will have what is called normal flow. Normal flow refers to the default way browsers render content. Under normal flow, block-level elements get rendered in the same order that they appear in the HTML markup, one on top of another, starting from the top left corner of the document, and inline elements stretch as wide as their inside content (usually text).position: static – or rather, not setting any value for position on an element – is often the behavior we want. Unless you have a specific reason to choose one of the other possible values discussed below, then don't explicitly set position.


* `absolute`
Like fixed elements, absolute elements are outside the normal flow and can be offset, but unlike fixed elements, they are offset in relation to the first parent container with a non-static position.

nav {
  padding-top: 10px;
  padding-right: 10px;
  border: 1px solid black;
  text-align: right;
  position: relative;
  height: 50px;
}

* `relative`
When an element's position property is set to relative, it is still in the normal flow (in other words, relatively positioned elements are rendered in the order they appear in HTML), but unlike with static elements, we can use offset properties (left, right, top, bottom) with relative elements.

div {
  position: relative;
}

* `fixed`
When an element's position is set to fixed, it will stay in place even when the user scrolls. Fixed elements are taken out of the normal flow, and other elements will position themselves as if the fixed element does not exist. 
.foo {
  width: 100px;
  height: 100px;
  position: fixed;
  background-color: blue;
  left: 0;
  top: 0;
}


### Use the float property

Be able to explain and demonstrate the `float` property, and relatedly the `clear` property. Specifically:

* `float: left`
float: left; on the .left class and applied that class to the three image elements. By doing so, we've taken the images out of the normal flow, and pushed them to the left. 

.left {
  float: left;
  margin-right: 15px;
}

* `float: right`
Note that if we set float: right; instead, the images would move to the right of the page, and the text would wrap on the left.

.right {
  float: right;
  margin-left: 15px;
}


* `clear: left`


* `clear: right`
In this instance, we set it to clear: right in order to make div.foo aware of the right floated elements and move to the next line.

.foo {
  width: 75px;
  height: 75px;
  background-color: red;
  clear: right; 
}


## JavaScript

### Variables

For a list of JavaScript data types check [the MDN site here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Data_types)

Take care to avoid JavaScript reserved keywords when creating variables. You can find a [list of them here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords).

You should be able to explain the difference between `let` and `const`, and `let` and `var`,

#### Create a variable with `let`

```javascript
let message = "Hello World"; //string variable
let isAwesome = true; //boolean variable
let numCookies = 900; //number variable
```

#### Create a constant with `const`

```javascript
const answerToUniverse = 42;
const adminEmail = "admin@foobar.com";
```

#### Create a variable with `var`

```javascript
var message = "Hello World"; //string variable
var isAwesome = true; //boolean variable
var numCookies = 900; //number variable
```


### Application Logic

#### Logical operators

```javascript
== vs. ===
simple equality vs strict equality.The strict equality operator === first compares data type of the 2 items being compared, and if they're not the same data type (as in this case), it returns false. If they are the same type, it then checks to see if they have the same value. The == operator in JavaScript has a looser notion of equality. When it compares 2 items, if it finds that the 2 values are not of the same type, it coerces (or converts) one of the value types to the type of the other. So true == 1 evaluates to true because when you have a boolean and a number, the number gets converted to a boolean
!== not equal
<=
>=
|| or
&& and
```


#### Control flow with conditionals

Be able to explain and use `if`, `else`, and `else if`

```javascript

if (x === 1) {
  // do things here
} else if (x === 2) {
  // do some other things here
} else {
  // do this
}
```


### Loops

**for loops**: Create a `for` loop and print something to the console.

```
for (let i = 0; i < 10; i++) {
  console.log(`i is ${i}`);
}
```

**while loops**: Create a `while` loop and print something to the console.

```javascript
let i = 0;

while (i < 10) {
  console.log(`i is: ${i}`);
  i++;
}
```


### Functions

#### Create a function that returns a string, invoke the function, and print the result to the console.

```javascript
function helloWorld() {
  return "Hello World";
}

const greeting = helloWorld();
console.log(greeting);  // => "Hello World"
```

#### Create a function that takes a number argument and returns the value plus 5. Print the result to console.

```javascript
function addFive(number) {
  return number + 5;
}

const result = addFive(10);
console.log(result);   // => 15
```


### Arrays

#### Create an array

```javascript
const myArray = ["apple", "orange", "pear"];
```

#### Loop through a JavaScript array and print the array index and value to the console

```javascript
const myArray = [
  "hockey",
  "lacrosse",
  "curling"
];

for (let i = 0; i < myArray.length; i++) {
  console.log(`element ${i}: ${myArray[i]}`);
}

// alternatively, and even better!

myArray.forEach((element, index) => console.log(`element ${index}: ${element}`));
```


### Objects

#### Create a JavaScript object

```javascript
const myObj = {
  fruit: "apple",
  drink: "water",
  dessert: "cookie"
};
```

#### Access the value in an object

```javascript
myObj.fruit
myObj["fruit"]
```

Be able to explain when or why you would use dot notation vs. bracket notation



#### Loop through a JavaScript object and print the key and value to the console

```javascript
const myObj = {
  fruit: "apple",
  drink: "water",
  dessert: "cookie"
};

for (const key in myObj) {
  console.log(`${key}: ${myObj[key]}`);
}

// alternatively, and even better
Object.keys(myObj).forEach(key => console.log(`${key}: ${myObj[key]}`));
```

### Advanced JavaScript

While it might be a stretch for you right now, you should be well on your way to understanding and writing code similar to the following.

#### Write a function that accepts a "searchName" argument. Loop through an array of objects and return the object that matches against the "name" key. 
```
const myData = [
  {
    name: "Tom",
    age: 22,
    favoriteFood: "pizza"
  },
  {
    name: "Jane",
    age: 42,
    favoriteFood: "sushi"
  },
  {
    name: "Fred",
    age: 34,
    favoriteFood: "lettuce"
  }
];

function findByName(searchName) {
  for (let i = 0; i < myData.length; i++) {
    if (myData[i].name === searchName) {
      return myData[i];
    }
  }
}

const person = findByName('Jane');
console.log(person);  // => { name: "Jane", age: 42, favoriteFood: "sushi" }
```

