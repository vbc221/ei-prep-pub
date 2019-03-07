# Technical Evaluation Study Guide

To gain admission into Thinkful's Engineering Immersion or Engineering Nights & Weekends programs, you must pass a live, technical evaluation. The purpose of this evaluation is to ensure prospective students have a good understanding of JavaScript, HTML, CSS and GitHub/command line before entering the program. 

## How does this work?

The tech eval will be live, 1-hour in length, and conducted by a Thinkful mentor. You will schedule your technical evaluation directly on your dashboard once your previous goals have been marked complete. 

The format of the evaluation is broken into two sections: 

##### Verbal

In the first 10-15 minutes, you will answer questions about the topics covered in the curriculum: HTML/CSS, JavaScript, and GitHub/command line. You will not be permitted to look up information in this section. 

##### Live Coding

A majority of the time (45 minutes) will be spent on live JavaScript coding challenges. You will clone a GitHub repo, open files containing the challenges on your local editor, and modify the files with your solutions. Be sure to review the GitHub/command line lesson and practice this flow with your mentor. 

Note: this section is open resource -- you'll be able to look up documentation online. We expect you to verbalize your thought process you work through each challenge with your evaluator. To succeed in technical interviews, it's important to develop a consistent problem-solving process and effectively communicate your approach. 

# How should I prepare? 

[Watch Video: "How to Pass the Tech Eval"](https://www.useloom.com/share/70778ddd010e413baaeef45010b97cde)

In addition to reviewing the concepts in the curriculum, the best way to prepare for the technical evaluation is to practice for the specific format of the interview. 

During the verbal section, you might hear questions like "What's the difference betweeen X and Y?" or "Why is Z concept important?". Spend a minute explaining each high-level concept you've learned out loud. If you struggle to do this, go back and review the curriculum or watch one of several educational YouTube videos that explain the concept. We also recommend you practicing discussing technical concepts on Slack, in office hours, or with your mentor. 

To practice for the live coding section, you should simulate the specific environment blocking off 45 minutes at a time to work through live coding challenges, verbalize your thought process, and look up documentation when stuck. 

We require you spend at least 10 hours on the following live coding challenges:
* [JavaScript Classroom](https://repl.it/community/classrooms/20690) in Repl.it. This resource is our top recommendation. To access, sign into your Repl.it account and click on the community link in the menu. Then select the Auto-graded Javascript Exercises classroom, and click "Take This Classroom". You'll be asked to create a student profile, which is just your name and school. 
* [Free Code Camp - Basic JavaScript](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript)
* [Free Code Camp - Basic Data Structures](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)
* [Free Code Camp - Basic Algorithms](https://www.freecodecamp.org/challenges/get-set-for-our-algorithm-challenges)
* [Codewars](https://www.codewars.com/)

Note: If you have mentor sessions still available, ask your mentor to review the practice tech eval with you (they have access to this). It's a good idea to give them a heads up that you'll want to do this prior to your meeting so they can prepare. 

# What happens after the evaluation? 

After the tech eval, the evaluator will submit a feedback form for the Prep Program Manager team to review. If you pass (and have confirmed finances), you'll soon receive a formal acceptance email and enrollment link. 

If you do not pass, you'll be able to retake the tech eval. We encourage you to attempt the evaluation prior to the deadline to leave room for a possible retake. Your specific timeline for the retake will depend on your score and the cohort deadline. 
Reach out directly to your PM with any specific questions.


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

