# Tech Eval Study Guide

In addition to reviewing your work in the prep course, use this guide to prepare for the Tech Eval. Additionally, if you have any mentor sessions still available, ask your mentor to review the practice tech eval with you (they have access to this) and/or practice living coding drills. It's a good idea to give them a heads up that you'll want to do this prior to your meeting so they can prepare. 

## Practice Live Coding

We require that you spend at least 10 hours on the following live coding challenges:
* [Free Code Camp - Basic JavaScript](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript)
* [Free Code Camp - Basic Data Structures](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)
* [Free Code Camp - Basic Algorithms](https://www.freecodecamp.org/challenges/get-set-for-our-algorithm-challenges)
* [JavaScript Classroom](https://repl.it/community/classrooms/20690) in Repl.it -- To access, sign into your Repl.it account and click on the community link in the menu. Then select the Auto-graded Javascript Exercises classroom, and click "Take This Classroom". You'll be asked to create a student profile, which is just your name and school. You will need to successfully complete drills like these in the Tech Eval.

If you want even more practice:
* [Codewars](https://www.codewars.com/)

## What to Expect

The Tech Eval will be 1 hour. Remember that all other goals must be completed and approved on your dashboard prior to scheduling the eval. The Tech Eval is split into two sections:

##### Verbal
The first 10-15 minutes will test your understanding of technical terminology that was explained in the Prep materials. You are not permitted to look up information in this portion.

##### Live Coding
The last, most crucial, 45 minutes will be spent on live coding challenges where you'll be expected to write functions and communicate your problem solving skills. Taking the test requires cloning a Git repo and editing code directly in a code editor on your machine. Make sure you practice this process with your mentor! This section is open resource -- this means you can look up documentation and resources, but how you research is part of your evaluation and you should be able to explain your thought process to your evaluator. 

You can take the Tech Eval up to 2 times while enrolled in Prep. This is why we also recommend to take the first test prior to the deadline to leave room for a possible retake. Reach out to your PM if you have additional questions.

[Watch Video: "How to Pass the Tech Eval"](https://www.useloom.com/share/70778ddd010e413baaeef45010b97cde)

## HTML

### Create valid, semantic, accessible HTML

Note in particular the use of semantic elements like `header`, `section`, and `footer`, and the use of the `lang` and `role` attributes, which are accessibility must haves.

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
* `block`
* `inline-block`


### Use the position property

Be able to explain and demonstrate the following values for the position property:

* `static`
* `absolute`
* `relative`
* `fixed`


### Use the float property

Be able to explain and demonstrate the `float` property, and relatedly the `clear` property. Specifically:

* `float: left`
* `float: right`
* `clear: left`
* `clear: right`


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
!==
<=
>=
||
&&
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

## Command Line

* `cd`: Change directory
* `pwd`: Print working directory
* `ls`: List files of current directory
* `mkdir`: Make a new directory
* `touch`: Create a file
* `rm`: Remove a file
* `rmdir`: Remove a directory
* `mv`: Move a file
* `cp`: Copy a file

## Git

* `git init`: Initialize a new git repository
* `git add`: Stage a file for changes (watch these files for changes)
* `git commit`: Commit a set of changes (take a snapshot of the code as it is right now)
* `git status`: Shows the current status of a git repository
* `git diff`: Shows the differences between commits
* `git checkout`: Switch branches
* `git reset`: Reset to a previous state
* `git branch`: List, create, or delete branches
* `git merge`: Join two or more branches
* `git push`: Update remote repository

