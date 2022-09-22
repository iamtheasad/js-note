```
/*
  ## **Prototype** // Title
  ### Home // Sub Title
  <h4><strong><u>Rest Oeprator</u></strong> </h4> // Sub Title descriptor
*/
```


## Javascript Basic

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

## **Object Oriented Programming**

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
    this.width = width
    this.height = height
    this.draw = function () {
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
var ConstructorClass = function (width, height) {
  this.width = width;
  this.height = height;
  var print = (printProperties = function () {
    console.log('My width is' + this.width);
    console.log('My Height is' + this.height);
  });
  this.draw = function () {
    console.log('This rectangle');
    printProperties();
  };
};
```

- Hide private properties in from class

  We should use variabble to hide object properties from any class from end user.

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

## **Prototype**

- Protoype is a parent class of any js class
- Every object have a prototype object

```
function Square (width){
// It's call : instance member
  this.width = width
  this.getWidth = function(){
    console.log('Width is = ' + this.width);
    // Getting access of prototype member
    this.draw();
  }
}

Square.prototype = {
// It's call : prototype member
  draw: function(){
    console.log('Draw');
  },

  toString: function(){
  // Getting access of instance member
    return 'My width is = ' + this.width
  }
}

var sqr1 = new Square(10);
var sqr2 = new Square(4);
var sqr1.toString();
```

- Get instance members

```
console.log(Object.keys(sqr1));
```

- Get instance members and prototype members

```
for(var i in sqr1){
  console.log(i);
}
```

- Extends function to reduce repeating code
- Method overriding in javascript
- Polymorphism in javascript
- To avoide compelxity in hirarchy we should use object composition.
- We should use Inheritance for 2 layers max 3 layers and Composition for more than 2 layers
- Inheritence and Composition mixing together

## **ES6**

- Template string

```
`I am template string ${here we can use variable, function call, ternary operator, any js statement. It should be single line code not multiline code}`
```

### var, let, const :

- Assign value with **var** can access outside of it's block of code

```
for(var i = 0; i < 5; i++){

}
console.log(i)
// result = 5
```

- If we assign value in **let** we can't access value outside of it's block.
- **let** keyword create a block, just like function.

```
for(let i = 0; i < 5; i++){

}
console.log(i)
// result = i is not defined
```

- If we assign value in **var** it can change letter

```
var a = 'Rana';
a = 'Asad';

console.log(a);
// result = Asad
```

- Don't use **var** keyword as variable to prevent memory leaks.
- **const** keyword use as variable if you don't want to change the value of it.
- Can't change **const** variable value after assign

```
const a = 'Rana';
a = 'Asad';

console.log(a);
// result = a is read only
```

### **Arrow Function**

```
let add = (a, b) => {
  return a + b;
}
console.log(add(10, 5));
```

- Added implicite return here

```
let add = (a, b) => a + b; // Before a + b js engine implicitly added return keyword, it only work for single line code
console.log(add(10, 5));
```

- Single paremeter without parenthesis

```
let sqr = x => x * x;
console.log(sqr(5));
```

- Don't use arrow function as object's method
- Always use arrow function in the method, arrow function's **this** always return of this parent object

```
let obj = {
  name: 'Rana',
  print: function(){
    setTimeout(() => {
      console.log(`My name is ${this.name}`);
    }, 1000);
  }
}

obj.print();
```

- If you want to use default parameter don't pass undefine or null as argument it cause an error.

```
function greet(msg="Hello", name="Md Rana"){
  console.log(name.length); // It will show an error
  console.log(`${name}` ! ${msg});
}

greet(null, 'Asad');
```

### **Rest and Spread Operator**

<h4><strong><u>Rest Oeprator</u></strong> </h4>

- **rest** operator only use in function as paremerter
- **rest** operator use in paremeter as last item of paremeter
- **rest** operator return an array

```
function sum(...rest){
  return rest.reduce((a, b) => a + b);
}

console.log(sum(1,2,3,4,5));
```

```
function multiply(multiplier, ...theArgs) {
  return theArgs.map((value) => {
    return multiplier * value;
  });
}

let arr = multiply(2, 1, 2, 3);
console.log(arr);
```

<h4><strong><u>Spread Oeprator</u></strong> </h4>

- To get singular data from array we use **spread** operator

```
let n = [1, 2, 3, 4, 5];

function sum(...rest) {
  return rest.reduce((a, b) => a + b);
}

// Here we pass argument n as singular data to sum function though it was array it converts array into singular data
console.log(sum(...n));

console.log(...n); // It will return singular data not whole array
console.log(n); // It will return whole array
```

- To get a copy of an object we use **spread** operator

```
let obj = {
  a: 10,
  b: 20,
};

let obj2 = {
  ...obj,
};

console.log(obj2);
```

- Copy arrays with **spread** operator

```
let arr = [1, 2, 3];
let arr2 = [...arr]; // like arr.slice()
arr2.push(4);
console.log(arr);
console.log(arr2);
```

- Concatening two array with **spread** operator also we can add new array elements here

```
var arr = [1, 2, 3];
var arr2 = [4, 5];
// arr.concat(arr2); // we can also concat array with concat method
arr = [...arr, 'freeCodeCamp', ...arr2];
console.log(arr);
```

### Object shorthand in es6

- Object shorthand in es6 for key and values
```
let a = 10, b = 20, c = 30;
let obj = {
  a, //  If key and value are same instead of **a = a** we can assign only a as variable and value
  b,
  c
}
```
- Object shorthand in es6 for Method
```
let obj = {
  // es6
  print(){
    console.log(this);  
  }
  
  // es5
  print: function(){
    console.log(this);
  }
}
```

### Destructuring

- Object Destructuring

```
let person = {
  name: 'Md. Rana',
  email: 'rana@gmail.com',
  address: {
    city: 'Dhaka',
    country: 'Bangladesh',
  },
};

let {
  name,
  email,
  address: { city, country },
} = person;

console.log(name, email, city, country);
```

- Array Destructuring

```
let a, b, rest;
[a, b] = [10, 20];

console.log(a);
// expected output: 10

console.log(b);
// expected output: 20

[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(rest);
// expected output: Array [30,40,50]
```

### Object fromEntries method

- **entries** method make new array from an object

```
let obj = {
  a: 10,
  b: 20,
};

console.log(obj);
let en = Object.entries(obj);
console.log(en);
```
- **fromEntries** method make new object from an array

```
let arr = [
  ['ab', 1],
  ['bb', 2],
];

console.log(Object.fromEntries(arr));

```

### Javascript Symbol

- The JavaScript ES6 introduced a new primitive data type called Symbol. Symbols are immutable (cannot be changed) and are unique. For example
- Create unique identifier

```
// two symbols with the same description

const value1 = Symbol('hello');
const value2 = Symbol('hello');

console.log(value1 === value2); // false
```
- Though **value1** and **value2** both contain the same description, they are different.

### Iterator

- Any iterable object will be iterate
- Object, object literal, constructor pattern, factory pattern will be iterate 
- Every time it will give one array item value
- Previous value can't call here
- Every time get value from closure

- This function will only iterate array of collection

- es5 / manual implementation of array iteration

```
let arr = [1, 2, 3];

function createIterator(collection) {
  let i = 0;
  return {
    next() {
      return {
        done: (i) => collection.length,
        value: collection[i++]
      };
    }
  };
}

console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
```

- es6 built in method for array iteration

```
let arr = [1, 2, 3];
let iterate = arr[Symbol.iterator](); 

console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
```

- es6 built in method for string iteration

```
let str = 'text';
let iterate = str[Symbol.iterator]();

console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
console.log(iterate.next());
```

<h4><strong><u>Generator for iterator</u></strong> </h4>

- Generator make object iterable
- Generator function declaration require * sign after function word

```
let arr = [1, 2, 3];

function* generate(collection) {
  for (let i = 0; i <= collection.length; i++) {
    yield collection[i];
  }
}

let it = generate(arr);

console.log(it.next());
console.log(it.next());
console.log(it.next());
console.log(it.next());
console.log(it.next());
```
