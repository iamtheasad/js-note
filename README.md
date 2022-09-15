# js-note

## js Basic

### Home

- JavaScript is the world's most popular programming language.
- JavaScript is the programming language of the Web.
- JavaScript is easy to learn.
- This tutorial will teach you JavaScript from basic to advanced.
- This tutorial covers every version of JavaScript:
  - The Original JavaScript ES1 ES2 ES3 (1997-1999)
  - The First Main Revision ES5 (2009)
  - The Second Revision ES6 (2015)
  - The Yearly Additions (2016, 2017, 2018)
- Why Study JavaScript?
- Commonly Asked Questions
  - How do I get JavaScript?
  - Where can I download JavaScript?
  - Is JavaScript Free?
- This tutorial covers every version of JavaScript:
  - The Original JavaScript ES1 ES2 ES3 (1997-1999)
  - The First Main Revision ES5 (2009)
  - The Second Revision ES6 (2015)
  - The Yearly Additions (2016, 2017, 2018)
- Learning Speed

### **JavaScript Introduction**

- JavaScript Can Change HTML Content
- JavaScript Can Change HTML Attribute Values
- JavaScript Can Change HTML Styles (CSS)
- JavaScript Can Hide HTML Elements
- JavaScript Can Show HTML Elements

### **JavaScript Where To**

- The \<script> Tag
- JavaScript in \<head> or \<body>
  - Placing scripts at the bottom of the \<body> element improves the display speed, because script interpretation slows down the display.
- External JavaScript
- External JavaScript Advantages
  - It separates HTML and code
  - It makes HTML and JavaScript easier to read and maintain
  - Cached JavaScript files can speed up page loads

### **JavaScript Output**

- JavaScript Display Possibilities
  - Writing into an HTML element, using `innerHTML`.
  - Writing into the HTML output using `document.write()`.
  - Writing into an alert box, using `window.alert()`.
  - Writing into the browser console, using `console.log()`.

### **JavaScript Statements**

- JavaScript Programs
- JavaScript Statements
- Semicolons ;
- JavaScript White Space
- JavaScript Line Length and Line Breaks
- JavaScript Code Blocks
- JavaScript Keywords

### **JavaScript Syntax**

- JavaScript Variables
- JavaScript Operators
- JavaScript Expressions
- JavaScript Keywords
- JavaScript Comments
  - Single line Comments
  - Multi line Comments
- JavaScript Identifiers / Names
  - A JavaScript name must begin with:
  - A letter (A-Z or a-z)
  - A dollar sign ($)
  - Or an underscore (\\\_)
- JavaScript is Case Sensitive
- JavaScript and Camel Case
  - Underscore
  - Upper Camel Case (Pascal Case)
  - Lower Camel Case
- JavaScript Character Set

### **Object Oriented Programming**

2 Types of class:

1. Factory Pattern Class

```
var factoryClass = function (width, height) {
  return {
    width: width,
    height: height,
    draw: function () {
      console.log('This rectangle');
      this.printProperties();
    },

    printProperties: function () {
      console.log('My width is' + this.width);
      console.log('My Height is' + this.height);
    },
  };
};

let rect1 = factoryClass(20, 30);
rect1.draw();
```

2. Constructor Pattern

```
var ConstructorClass = function (width, height) {
    this.width: width
    this.height: height
    this.draw: function () {
      console.log('This rectangle');
      this.printProperties();
    }

    this.printProperties: function () {
      console.log('My width is' + this.width);
      console.log('My Height is' + this.height);
    }
};

let rect2 = ConstructorClass(20, 30);
rect2.draw();
```

- **new** operator create an empty object that associate with function

```
function myFunce(){
    console.log(this);
}

var newResult = new myFunction();
newResult();
```

here **new** operator create a new empty object that associate with **_myFunc()_**

- Pass by value and pass by reference

Premetive data pass by value:

```
var n = 10;

function myFunc(n) {
  n = n + 100;
  console.log(n);
}

myFunc(n);
console.log(n);
```

Object data pass by reference:

```
var n = 10;

function myFunc(n) {
  n = n + 100;
  console.log(n);
}

myFunc(n);
console.log(n);
```

var ConstructorClass = function (width, height) {
this.width: width
this.height: height
var print = printProperties: function () {
console.log('My width is' + this.width);
console.log('My Height is' + this.height);
}
this.draw: function () {
console.log('This rectangle');
printProperties();
}
};

- Hide private properties in from class
  We should use variabble to hide object properties from any class from end user

```
var ConstructorClass = function (width, height) {
    this.width: width
    this.height: height
   var print = printProperties: function () {
      console.log('My width is' + this.width);
      console.log('My Height is' + this.height);
    }
    this.draw: function () {
      console.log('This rectangle');
      printProperties();
    }
};

let rect2 = ConstructorClass(20, 30);
rect2.draw();
```
