```
  // Title
  ## Prototype

  // Sub Title
  ### Home

  // Sub Title descriptor
  <h4> Rest Oeprator </h4>

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

<h4>Rest Oeprator </h4>

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

<h4> Spread Oeprator </h4>

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
- If any objec is iterable that mean's we can use **for of** loop here.
- **for of** loop only can use in iterable object

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

- Iterable checking with function

```
function isIterable(obj) {
  return typeof obj[Symbol.iterator] == 'function';
}

let set = new Set([1, 2, 3]);

set.add(5);
set.add(6);
set.add(1);
set.add(2);

console.log(isIterable(set));
```

<h4>Generator for iterator </h4>

- If a function return an iterator that's call generator
- Generator make object iterable
- Generator function declaration require \* sign after function word

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

### Set & Map data structure

- **set** & **map** is a js default data structure provide by js
- To keep data in a organized way we use set & map data structure

<h4>Set Collection </h4>

```
let set = new Set([1, 2, 3]);

set.add(5);
set.add(6);
set.add(1);
set.add(2);
// console.log(set);
// console.log(set.size);

let keyIterate = set.keys();

console.log(keyIterate.next());
console.log(keyIterate.next());
console.log(keyIterate.next());
console.log(keyIterate.next());
console.log(keyIterate.next());
console.log(keyIterate.next());
console.log(keyIterate.next());

```

<h4>Map Collection </h4>

- Map is a js data structure
- We can use keys and values here as an array
- **set** & **Map** both are same except in map **object** can be use as an key
- **object** can be use as an array key

```
let map = new Map([
  ['a', 10],
  ['b', 30],
]);

map.set('c', 40);
map.set({ name: 'Md Rana' }, 27); //  **object** can be use as key

console.log(map);
```

<h4> Weak Set </h4>

- WeakSet is a garbage collector
- For garbage clean use WeakSet
- Prevent memory leak
- It's clean previous value from memory
- WeakSet have add, delete, has method

```
// Memory leaking
let a = {a: 10}, b = {b: 20}

let set = new Set([a, b]);

a = null
console.log(set);

// Preventing memory leak

 let a = {a: 10}, b = {b: 20}
 let weakSet = new WeakSet([a, b]);

 a = null

 console.log(weakSet.has(a));
```

<h4> Weak Map </h4>

- WeapSet and WeakMap both are same
- WeakMap is a garbage collector
- For garbage clean use WeakMap
- Prevent memory leak
- It's clean previous value from memory

```
// Preventing memory leak

let weakMap = new WeakMap([
  ['a', 10],
  ['b', 30],
]);

a = null

console.log(weakMap.get(a));
```

### Class in es6

```
class Rectangle {
  // Passing parameter in constructor function
  constructor(width, height) {
    this.width = width;
    this.height = height;
    // It will add on parameter
    this.another = function () {
      console.log('Drawing...');
    };
  }
  // It will add on property. It's added on js in es2022 version
  test2 = function () {
    console.log('test2');
  };

  // We can assign a property value here. It's added on js in es2022 version
  name = 'rana';

  // This function will add to prototype
  draw() {
    console.log('Drawing...');
  }
}

let rect1 = new Rectangle(4, 5);
console.log(rect1);

```

<h4> ES6 Static Method </h4>

- Without calling Person class we can call a method from outside fo the clas
- This method should not have any side effec
- We can provide data from outside of the class

```
// Static method in class
class Person {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }

  print() {
    console.log(this.width, this.height);
  }

  static myStatic(str) {
    let user = JSON.parse(str);
    return new Person(user.name, user.email);
  }
}

let str = '{"name": "Md Rana","email": "rana@gmail.com"}';
let p1 = Person.myStatic(str);
console.log(p1);
```

<h4> this Keyword Behaviour in Class </h4>

- If we assign a method in another variable that variable became a function and that fucntion always refer to it's parent window object, to prevent this behaviour use 'use strict' in top of js document
- Now **anotherDraw** is a function
- This function will refer window object
- If we use 'use strict' in top of the document it will refer own object instead of window object

```
function Shape() {
  this.draw = function () {
    console.log(this);
  };
}

let s1 = new Shape();
s1.draw();

let anotherDraw = s1.draw;

anotherDraw();

```

- But in es6 class **this** keyword always refer to it's own object

```
class Person {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }

  print() {
    console.log(this.width, this.height);
  }

  test() {
    console.log(this);
  }

  static myStatic(str) {
    let user = JSON.parse(str);
    return new Person(user.name, user.email);
  }
}

let str = '{"name": "Md Rana","email": "rana@gmail.com"}';
let p1 = Person.myStatic(str);

let testing = p1.test;
testing();
```

<h4> Data, Method Hide With Symbol Method </h4>

- Variable or name define with underscore(\_) means it hidden from class, you can't access it outside of the class
- Symbole() create unique identifier

```
const _radius = Symbol();
const _name = Symbol();
const _draw = Symbol();

class Circle {
  constructor(radius, name) {
    this[_radius] = radius;
    this[_name] = name;
  }

  [_draw]() {
    console.log('Drawing...');
  }

  test() {
    console.log('Drawing...');
  }
}

let c1 = new Circle(2, 'CRED');
console.log(c1);
```

<h4> Data, Method Hide With WeakMap Method </h4>

```
const _radius = new WeakMap();
const _name = new WeakMap();
const _resize = new WeakMap();

class Circle {
  constructor(radius, name) {
    this.size = 100;
    _radius.set(this, radius);
    _name.set(this, name);
    _resize.set(this, () => {
      console.log(this.size);
    });
  }

  draw() {
    console.log('Drawing...');
    console.log(this._radius, this._name);
    _resize.get(this)();
  }
}

let c1 = new Circle(2, 'CRED');
c1.draw();
```

<h4> Getter and Setter Private Data, Method from Class </h4>

```
const _radius = new WeakMap();
const _name = new WeakMap();
const _resize = new WeakMap();

class Circle {
  constructor(radius, name) {
    this.size = 100;
    _radius.set(this, radius);
    _name.set(this, name);
    _resize.set(this, () => {
      console.log(this.size);
    });
  }

  get radius() {
    return _radius.get(this);
  }

  set radius(v) {
    return _radius.set(this, v);
  }

  draw() {
    console.log('Drawing...');
    console.log(this._radius, this._name);
    _resize.get(this)();
  }
}

let c1 = new Circle(2, 'CRED');
c1.radius = 100;
console.log(c1.radius);
```

<h4>ES6 Class Inheritance  </h4>

- For inheritance extends keyword should use
- Also should provide super() function for parent/Shape class parameters/arguments

```
class Shape {
  constructor(color) {
    this.color = color;
  }

  draw() {
    console.log('Shaping');
  }
}

class Rectangle extends Shape {
  // parent/Shape class parameter should also provide here
  constructor(color, width, height) {
    // super() is constructor function of parent/Shape class
    super(color);
    this.width = width;
    this.height = height;
  }

  calculate() {
    return this.width + this.height;
  }
}

let r = new Rectangle('green', 4, 5);
console.log(r);
r.draw();
```

<h4> ES6 Method Overriding of Inherited Class  </h4>

```
class Shape {
  constructor(color) {
    this.color = color;
  }

  draw() {
    console.log('Shaping');
  }
}

class Rectangle extends Shape {
  constructor(color, width, height) {
    super(color);
    this.width = width;
    this.height = height;
  }

// Overriding draw method of Shape class
  draw() {
    console.log('Overriding draw method of Shape class');
  }

  calculate() {
    return this.width + this.height;
  }
}

let r = new Rectangle('green', 4, 5);
console.log(r);
r.draw();
```

### ES6 Module System

- **export default** a function means we can call it by that file name
- Shape file:

```
class Shape {
  constructor(color) {
    this.color = color;
  }

  draw() {
    console.log('Shaping');
  }
}

export default Shape;

```

- Rectangle File import Shape class and exporting default

```
import Shape from './Shape';

class Rectangle extends Shape {
  constructor(color, width, height) {
    super(color);
    this.width = width;
    this.height = height;
  }

  draw() {
    console.log('Overriding draw method for Shape class');
  }

  calculate() {
    return this.width + this.height;
  }
}

export default Rectangle;
```

- Importing Rectangle in app.js for view

```
import Rectangle from './Rectangle';

let r = new Rectangle('green', 4, 5);
console.log(r);
r.draw();
```

- MultipleFunc files exporting

```
export const add = (a, b) => a + b;

export const sub = (a, b) => a - b;

export const times = (a, b) => a * b;

export const div = (a, b) => a / b;

```

- Importing files from MultipleFunc function

```
// Importing all function as MultipleFunc and then use it as object

import * as MultipleFunc from './func';

console.log(MultipleFunc.add(1, 2));
console.log(MultipleFunc.div(10, 2));

// Importing add and sub function from MultipleFunc with destructuring way
// We can simply call add(4,5) way don't need to use here any other name

import { add, sub } from './func';

console.log(add(4, 5));
console.log(sub(4, 5));
```

## Error Handeling

- js default error :
  - EvalError
  - InternalError
  - RangeError
  - ReferenceError
  - SyntaxError
  - TypeError
  - URIError

### Error Handeling With If Else Condition Check

```
function changeToInt(value) {
  let result = Number.parseInt(value);
  if (!result) {
    return 'String changing to number';
  }

  return result;
}

let callingApp = changeToInt('dfdf45.5');
console.log(callingApp);
```

### Error Handeling with Try Catch Block

- If in try block have any error, it show the catch block

```
function makeWords(text) {
  try {
    let str = text.trim();
    let words = str.split(' ');
    return words;
  } catch (error) {
    //  console.log(error.message);
    console.log('Please provide a valid number');
  }
}

let result = makeWords('   Md   Rana ');
console.log(result);
```

- Throwing an error in catch block with throw object

```
try {
  console.log('Line 1');
  throw new Error('Custome error throwing !');
  console.log('Line 1');
  console.log('Line 1');
  console.log('Line 1');
} catch (e) {
  console.log(e.message);
}
```

- Throwing an error with finally block
- Finally block will show any how if have error or not

```
try {
  console.log('Line 1');
  throw new Error('Custome error throwing !');
  console.log('Line 1');
  console.log('Line 1');
  console.log('Line 1');
} catch (e) {
  console.log(e.message);
} finally {
  console.log('This is a finally block');
}
```

- Created a Custom Error Class

```
class customError extends Error {
  constructor(msg) {
    super(msg);
    if (Error.captureStackTrace) {
      Error.captureStackTrace(this, customError);
    }
  }
}

try {
  console.log('Line 1');
  throw new customError('Custome error throwing !');
  console.log('Line 1');
  console.log('Line 1');
  console.log('Line 1');
} catch (e) {
  //   console.dir(e);
  console.log(e);
} finally {
  console.log('This is a finally block');
}
```

## Asynchronous Javascript

- Js is a asynchronous programming language
- Js Single threaded programming language though we can use it as multi threaded programming language. Because of its browser engine make js act like multi threaded programming language.
- Asynchronous Example:-

![image](https://user-images.githubusercontent.com/45126545/194788080-c0fccf5b-03fe-4f76-82c8-041b2f588e37.png)

```
console.log('Line 1');

setTimeout(() => {
  console.log('Line 2');
}, 4000);

console.log('Line 3');

setTimeout(() => {
  console.log('Line 2');
}, 0);

setTimeout(() => {
  console.log('Line 2');
}, 1000);
```

### How to Handle XMLHttpRequest Using Callback

- Creating a common function for getRequest with the help of callback function

```
function getRequest(url, callback) {
  const xhr = new XMLHttpRequest();
  xhr.open('get', url);

  xhr.onreadystatechange = function (e) {
    if (xhr.readyState === 4) {
      if (xhr.status === 200) {
        let response = JSON.parse(xhr.response); // Converting json string into javascript object
        callback(null, response);
      }
    } else {
      callback(xhr.status, null);
    }
  };

  xhr.send();
}

getRequest('https://jsonplaceholder.typicode.com/users', (err, res) => {
  if (err) {
    console.log(err);
  } else {
    console.log(res); // getting all response
  }
});

getRequest('https://jsonplaceholder.typicode.com/posts', (err, res) => {
  if (err) {
    console.log(err);
  } else {
    res.forEach((r) => {
      console.log(r.title); // getting individual posts title
    });
  }
});

```

### Promise

- `new Promise` is a constructor function
- `new Promise` callback function
- `new Promise` work with asynchronous behaviour
- `new Promise` pass two parameter `resolve, reject` both of these are return a callback function

- `then` block get data from resolver
- `catch` block get data from reject

```
function getIphone(isPassed) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (isPassed) {
        resolve('I have got an I phone');
      } else {
        reject(new Error('You have failed'));
      }
    }, 2000);
  });
}

// console.log(getIphone(true));
getIphone(false)
  .then((res) => {
    console.log(res);
  })
  .catch((e) => {
    console.log(e.message);
  });
```

- Data fetching from `fetch api` with `new Promise` constructor function

```
const BASE_URL = 'https://jsonplaceholder.typicode.com';
function getRequest(url) {
  return new Promise((resolve, reject) => {
    const xhr = new XMLHttpRequest();
    xhr.open('get', url);
    xhr.onreadystatechange = function (e) {
      if (xhr.readyState === 4) {
        if (xhr.status === 200) {
          let response = JSON.parse(xhr.response); // Converting json string into javascript object
          resolve(response);
        } else {
          reject(new Error('Error Happned Bro...'));
        }
      }
    };

    xhr.send();
  });
}

getRequest(`${BASE_URL}/users/1dfdf`)
  .then((response) => {
    console.log(response);
  })
  .catch((e) => {
    console.log(e);
  });
```

- For delaying Promise instead of setTimeout

```
const delay = (s) => new Promise((resolve) => setTimeout(resolve, s * 1000));

delay(1).then(() => console.log('1 seconds delay'));
delay(2).then(() => console.log('2 seconds delay'));
delay(3).then(() => console.log('3 seconds delay'));
delay(4).then(() => console.log('4 seconds delay'));
delay(5).then(() => console.log('5 seconds delay'));
```

- Instantly create promise and resolve it

```
let p1 = Promise.resolve('Testing');
p1.then((v) => {
  console.log(v);
});
```

- Instantly create promise and reject it

```
let p2 = Promise.reject('RECJECT');
p1.catch((e) => {
  console.log(e);
});
```

<h4>Promise Methods</h4>

- `Promise.all()` Method

```
let p1 = Promise.resolve('One');
let p2 = Promise.resolve('Two');
let p3 = Promise.resolve('Three');

let promiseArr = [p1, p2, p3];

Promise.all(promiseArr).then((arr) => {
  console.log(arr);
});
```

- It proves that Promise.all() always show all of its data together. If in this promise array any of this item have any problem data won't show
- If all array item resolve, it will get data otherwise it will reject

```
let p1 = new Promise((resolve) => {
  setTimeout(resolve, 3000, 'One');
});

let p2 = new Promise((resolve) => {
  setTimeout(resolve, 4000, 'Two');
});

let p3 = new Promise((resolve) => {
  setTimeout(resolve, 5000, 'Three');
});

let promiseArr = [p1, p2, p3];

Promise.all(promiseArr).then((arr) => console.log(arr));
```

- `Promise.race()` Method
- `Promise.race` show first item which one win the race against time

```
let p1 = new Promise((resolve) => {
  setTimeout(resolve, 3000, 'One');
});

let p2 = new Promise((resolve) => {
  setTimeout(resolve, 4000, 'Two');
});

let p3 = new Promise((resolve) => {
  setTimeout(resolve, 5000, 'Three');
});

let promiseArr = [p1, p2, p3];

// Promise.race show first item which one win the race against time.
Promise.race(promiseArr).then((v) => console.log(v));
```

### Async Await

- `async` function replace of `Promise` constructor function
- `async` function return a `Promise`
- No need to use Promise at anymore. Instead of `new Promise` in `es6` introduced `async await`
- We can use `await` only in `async` function

```
async function myFetchData() {
  try {
    let res = await fetch('https://jsonplaceholder.typicode.com/user');

    let data = await res.json();

    let names = data.map((u) => u.name);

    console.log(names);
  } catch (e) {
    console.log(e.message);
  }
}

myFetchData();

```

- If there have multiple Promise
- These three Promise array item will resolve at a time

```
let promises = [Promise.resolve(1), Promise.resolve(2), Promise.resolve(3)];

async function promiseAll() {
  let result = await Promise.all(promises);
  console.log(result);
}

promiseAll();
```

Example:

```
let p1 = new Promise((resolve) => {
  setTimeout(resolve, '3000', 'Promise Data');
});

async function myAsyncFunc() {
  // p1.then((v) => {
  //   alert(v);
  // });

  let v = await p1;
  console.log(v);
}
```

Example:

```
async function test() {
  return 'test';
}

test().then((v) => console.log(v));
```

<h4>Async iterator</h4>

```
let asyncIterable = {
  [Symbol.asyncIterator]() {
    let i = 0;
    return {
      next() {
        if (i < 5) {
          return Promise.resolve({
            value: i++,
            done: false,
          });
        } else {
          return Promise.resolve({
            done: true,
          });
        }
      },
    };
  },
};

let iterate = asyncIterable[Symbol.asyncIterator]();

// Old way
/* (async function () {
  // let v = await iterate.next();
  // console.log(v);

  console.log(await iterate.next());
  console.log(await iterate.next());
  console.log(await iterate.next());
  console.log(await iterate.next());
  console.log(await iterate.next());
  console.log(await iterate.next());
})();
 */

// Clear way to iterate async function
(async function () {
  for await (let v of asyncIterable) {
    console.log(v);
  }
})();

```

## DOM - Document Object Model

- `Dom` is a browser functionality, it's only work with `javascript`.
- `Dom` is a `web api`
- Browser provide `dom` api
- `Dom` is a tree like data structure. Browser data structure name is `dom`
- `Javascript` initially created for browser dom
- `Dom` can manipulate every kind of `html` element
  - `html` element means `html tag`, `attribute` and `text`
- Every html element call in `dom` as `node`

![image](https://user-images.githubusercontent.com/45126545/197379490-37fa5ce5-f4ce-4fc1-9e46-e0070575e044.png)

- Main four types of `node item`:

  - Element node
  - Text node
  - Attribute node
  - Comment node

![element](https://user-images.githubusercontent.com/45126545/197383460-1c3a6693-4657-48ee-b736-f28f23d57c99.png)

- Dom continously collecting event of browser and change it immediately and refresh web page

### Window Object

- `Window Object` is a global object of javascript
- `Document` is property of `window object`
- We can call or use any method or property without using `window.setTimeout()` -> `setTimeout()`
