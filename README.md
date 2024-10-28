### In this article  -  -  -
+ What is a variable? 
+ Declaring a variable
+ [Initializing a variable](#initializing-a-variable)
+ A note about var
+ Updating a variable
+  Variable types
+ Dynamic typing
+ Constants in JavaScript
+ JavaScript Hosting
+ JavaScript Scopes
+ JavaScript DataTypes



[ JavaScript Array Method Reference](https://www.w3schools.com/jsref/jsref_obj_array.asp)


# JavaScript Variables 


| Prerequisites: | A basic understanding of HTML and CSS, an understanding of what JavaScript is. |
| ------ | ----------- |

| Objective: |To gain familiarity with the basics of JavaScript variables. |
| ------ | ----------- |


Variables  not just strings and numbers. Variables can also contain complex data and even entire functions to do amazing things. You'll learn more about this as you go along.

### Examlpes

```js
   // HTML
    <button id="button_A">Press me</button>
<h3 id="heading_A"></h3>
```
```
 //JavaScript

const buttonA = document.querySelector("#button_A");
const headingA = document.querySelector("#heading_A");

let count = 1;

buttonA.onclick = () => {
  buttonA.textContent = "Try again!";
  headingA.textContent = `${count} clicks so far`;
  count += 1;
};
//example pressing the button runs some code.
```
## Declaring a variable
To do this, we type the keyword let and name of Variables ;
```js
  let myName;
  let myAge;
```

```js
      myName;
      myAge;  

      //execution
```
## Initializing a variable

```js
      myName = "Chris";
      myAge = 37; 

      //Try going back to the console now
```
## Declare and initialize a variable at the same time

```js
     let myDog = "Rover";
```

## A Note about var

Back when JavaScript was first created, this was the only way to declare variables

```jsmyName = "Chris";

function logName() {
  console.log(myName);
}

logName();

var myName; 


//This works because of hoisting — read var hoisting for more detail on the subject.
```


```js


  var myName = "Chris";
  var myName = "Bob";


  // You can declare the same variable as many times
```

```js
let myName = "Chris";
let myName = "Bob";  

 //It will through an error Let declare only once
```

```js
   //You'd have to do this instead:


  let myName = "Chris";
      myName = "Bob";     
```

```js
 //Change or Update  value of Variables


myName = "Bob";
myAge = 40;

```

## Use var as all modern browsers have supported let since 2015.

#### An aside on variable naming rules 
 just using Latin characters (0-9, a-z, A-Z) and the underscore character.

 + You shouldn't use other characters 
 + Don't use underscores at the start of variable names 
 + Don't use numbers at the start of variables.
 + A safe convention to stick to is lower camel case, where you stick together multiple words.
 + Make variable names intuitive, so they describe the data they contain.
 + Variables are case sensitive — so myage is a different variable from myAge.
 + You can't use words like var, function, let, and for as variable names. Browsers recognize them as different code items, and so you'll get errors.

###  Good name examples

```js
 age
 myAge
 init
 initialColor
 finalOutputValue
 audio1
 audio2 
```
###  Bad name examples

```js
  1
a
_12
myage
MYAGE
var
Document
skjfndskjfnbdskjfb
thisisareallylongvariablenameman
```
## Variable types
#### Numbers , Strings , Booleans , Arrays , Objects , Dynamic typing

```js
     //Number
  let myAge = 17;
```

```js
 //Strings

 let dolphinGoodbye = "So long and thanks for all the fish";
```

```js
  // Array


let myNameArray = ["Chris", "Bob", "Jim"];
let myNumberArray = [10, 15, 40];

```

```js
//Object

let dog = { name: "Spot", breed: "Dalmatian" };     typeof dog;
```

## Constants in JavaScript

+ you must initialize them when you declare them
+ you can't assign them a new value after you've initialized them.

```js
    // Example

   const count;// Error no initialized 
  
   let count = 1;

    count = 2;//Error you can"t assign again
 ```

 ####  update, add, or remove properties of const

 ```js
  const bird = { species: "Kestrel" };
 console.log(bird.species); // "Kestrel"
```
You can update, add, or remove properties of an object declared using const, because even though the content of the object has changed, the constant is still pointing to the same object:
```js
bird.species = "Striated Caracara";
console.log(bird.species); // "Striated Caracara"
```
### When to use const and when to use let

If you can't do as much with const as you can with let, why would you prefer to use it rather than let? In fact const is very useful. If you use const to name a value, it tells anyone looking at your code that this name will never be assigned to a different value. Any time they see this name.

## Hosting 

```js
   // following two lines run successfully due to JavaScript hosting



   console.log(a)//undefine
   greet ()
   function greet (){
   console.log("Good Morning") }
    
   var a =4 ;   // Declaration hosted at the top but initialization not
   console.log(a)


```

```js
   
   console.log(a) //Error
   greet ()
   function greet (){
   console.log("Good Morning") }
    
   let a =4 ;   
   console.log(a)


```

```js
   let a;
   console.log(a)
   greet ()
   function greet (){
   console.log("Good Morning") }
    
   let a =4 ;   
   console.log(a)


```

## JavaScript Scope

### Block scope, Function scope, Global scope

Before ES6 (2015), JavaScript variables had only Global Scope and Function Scope.

ES6 introduced two important new JavaScript keywords: let and const.

These two keywords provide Block Scope in JavaScript.

Variables declared inside a { } block cannot be accessed from outside the block:

### Examples of scopes

```js
 {
  let x = 2;
}
// x can NOT be used here
```
```js
{
  var x = 2;
}
// x CAN be used here
```
```js
/ code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```
```js
let carName = "Volvo";
// code here can use carName

function myFunction() {
// code here can also use carName
}
```
```js
var x = 2;       // Global scope
let x = 2;       // Global scope
const x = 2;       // Global scope
```

#### Automatically Global
If you assign a value to a variable that has not been declared, it will automatically become a GLOBAL variable.

This code example will declare a global variable carName, even if the value is assigned inside a function.

```js
 myFunction();

// code here can use carName

function myFunction() {
  carName = "Volvo";
}
```

#### Global Variables in HTML

```js
 var carName = "Volvo";
// code here can use window.carName


let carName = "Volvo";
// code here can not use window.carName

```
### JavaScript Data Types

**JavaScript has 8 Datatypes**
+ String
+ Number
+ Bigint
+ Boolean
+ Undefined
+ Null
+ Symbol
+ Object

The Object Datatype .

The object data type can contain both built-in objects, and user defined objects:

Built-in object types can be:

objects, arrays, dates, maps, sets, intarrays, floatarrays, promises, and more.


```js
// Numbers:
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");


let x = "Volvo" + 16; //When adding a number and a string, JavaScript will treat the number as a string.



let x = 16 + 4 + "Volvo";//Result 20Volvo

let x = "Volvo" + 16 + 4;//Result Volvo164 //js conceder 164 as string
```

### JavaScript Types are Dynamic
```js
let x;       // Now x is undefined
x = 5;       // Now x is a Number
x = "John";  // Now x is a String
```
### JavaScript Strings

```js
// Single quote inside double quotes:
let answer1 = "It's alright";

// Single quotes inside double quotes:
let answer2 = "He is called 'Johnny'";

// Double quotes inside single quotes:
let answer3 = 'He is called "Johnny"';
```

### JavaScript Numbers

```js
// With decimals:
let x1 = 34.00;

// Without decimals:
let x2 = 34;
```
#### JavaScript Booleans
```js
let x = 5;
let y = 5;
let z = 6;
(x == y)       // Returns true
(x == z)       // Returns false

```
#### JavaScript Arrays
```js
const cars = ["Saab", "Volvo", "BMW"];
```
#### JavaScript Objects
```js
 const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
#### The typeof Operator
```js
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"

typeof 0              // Returns "number"
typeof 314            // Returns "number"
typeof 3.14           // Returns "number"
typeof (3)            // Returns "number"
typeof (3 + 4)        // Returns "number"
```
#### Undefined

```js
let car;    // Value is undefined, type is undefined
```
#### Empty Values

```js
let car = "";    // The value is "", the typeof is "string

``



