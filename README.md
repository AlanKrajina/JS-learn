## JS Questions - updated


* [Data types](#data-types)
* [Hoisting](#hoisting)
* [Scope](#scope)
* [What is "use strict";? what are the advantages and disadvantages to using it?](#what-is-use-strict-what-are-the-advantages-and-disadvantages-to-using-it)
* [Explain how prototypal inheritance works](#explain-how-prototypal-inheritance-works)
* [Prototype Chain](#prototype-chain)
* [Difference Between Class and Prototypal Inheritance?](#difference-between-class-and-prototypal-inheritance)
* [Explain how `this` works in JavaScript](#explain-how-this-works-in-javascript)
* [What's the difference between `.call` and `.apply`?](#whats-the-difference-between-call-and-apply)
* [Bind, Call, Apply](#Bind-Call-Apply)
* [Classes](#Classes)
* [Module](#Module)
* [What is a closure, and how/why would you use one?](#what-is-a-closure-and-howwhy-would-you-use-one)
* [Callbacks](#callbacks)
* [Name two programming paradigms important for JavaScript app developers](#name-two-programming-paradigms-important-for-JavaScript-app-developers)
* [What is functional programming?](#What-is-functional-programming)
* [What is object oriented programming?](#What-is-object-oriented-programming)
* [What are the pros and cons of functional programming vs object-oriented programming?](#What-are-the-pros-and-cons-of-functional-programming-vs-object-oriented-programming)
* [What are the differences between ES6 class and ES5 function constructors?](#what-are-the-differences-between-es6-class-and-es5-function-constructors)
* [What advantage is there for using the arrow syntax for a method in a constructor?](#what-advantage-is-there-for-using-the-arrow-syntax-for-a-method-in-a-constructor)
* [What is the definition of a higher-order function?](#what-is-the-definition-of-a-higher-order-function)
* [What are two-way data binding and one-way data flow, and how are they different?](#What-are-two-way-data-binding-and-one-way-data-flow-and-how-are-they-different)
* [Design Patterns](#design-patterns)
* [Explain why the following doesn't work as an IIFE: `function foo(){ }();`. What needs to be changed to properly make it an IIFE?](#explain-why-the-following-doesnt-work-as-an-iife-function-foo--what-needs-to-be-changed-to-properly-make-it-an-iife)
* [What's the difference between a variable that is: `null`, `undefined` or undeclared? How would you go about checking for any of these states?](#whats-the-difference-between-a-variable-that-is-null-undefined-or-undeclared-how-would-you-go-about-checking-for-any-of-these-states)
* [What's a typical use case for anonymous functions?](#whats-a-typical-use-case-for-anonymous-functions)
* [How do you organize your code? (module pattern, classical inheritance?)](#how-do-you-organize-your-code-module-pattern-classical-inheritance)
* [What's the difference between host objects and native objects?](#whats-the-difference-between-host-objects-and-native-objects)
* [Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?](#difference-between-function-person-var-person--person-and-var-person--new-person)
* [When would you use `document.write()`?](#when-would-you-use-documentwrite)
* [Explain Ajax in as much detail as possible.](#explain-ajax-in-as-much-detail-as-possible)
* [What are the advantages and disadvantages of using Ajax?](#what-are-the-advantages-and-disadvantages-of-using-ajax)
* [Explain how JSONP works (and how it's not really Ajax).](#explain-how-jsonp-works-and-how-its-not-really-ajax)
* [What's the difference between an "attribute" and a "property"?](#whats-the-difference-between-an-attribute-and-a-property)
* [Why is extending built-in JavaScript objects not a good idea?](#why-is-extending-built-in-javascript-objects-not-a-good-idea)
* [Difference between document `load` event and document `DOMContentLoaded` event?](#difference-between-document-load-event-and-document-domcontentloaded-event)
* [What is the difference between `==` and `===`?](#what-is-the-difference-between--and-)
* [NaN](#nan)
* [Explain the same-origin policy with regards to JavaScript.](#explain-the-same-origin-policy-with-regards-to-javascript)
* [Why is it called a Ternary expression, what does the word "Ternary" indicate?](#why-is-it-called-a-ternary-expression-what-does-the-word-ternary-indicate)
* [Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?](#why-would-you-use-something-like-the-load-event-does-this-event-have-disadvantages-do-you-know-any-alternatives-and-why-would-you-use-those)
* [Explain what a single page app is and how to make one SEO-friendly.](#explain-what-a-single-page-app-is-and-how-to-make-one-seo-friendly)
* [What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?](#what-are-some-of-the-advantagesdisadvantages-of-writing-javascript-code-in-a-language-that-compiles-to-javascript)
* [What tools and techniques do you use debugging JavaScript code?](#what-tools-and-techniques-do-you-use-for-debugging-javascript-code)
* [Explain the difference between mutable and immutable objects.](#explain-the-difference-between-mutable-and-immutable-objects)
* [Explain the difference between synchronous and asynchronous functions.](#explain-the-difference-between-synchronous-and-asynchronous-functions)
* [What is event loop? What is the difference between call stack and task queue?](#what-is-event-loop-what-is-the-difference-between-call-stack-and-task-queue)
* [Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`](#explain-the-differences-on-the-usage-of-foo-between-function-foo--and-var-foo--function-)
* [What are the differences between variables created using `let`, `var` or `const`?](#what-are-the-differences-between-variables-created-using-let-var-or-const)
* [Can you give an example for destructuring an object or an array?](#can-you-give-an-example-for-destructuring-an-object-or-an-array)
* [ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?](#es6-template-literals-offer-a-lot-of-flexibility-in-generating-strings-can-you-give-an-example)
* [What are the benefits of using spread syntax and how is it different from rest syntax?](#what-are-the-benefits-of-using-spread-syntax-and-how-is-it-different-from-rest-syntax)
* [How can you share code between files?](#how-can-you-share-code-between-files)
* [Nodejs](#nodejs)
* [Big O](#big-o)
* [Object iteration](#object-iteration)
* [Object methods](#object-methods)
* [Array methods](#array-methods)
* [String methods](#string-methods)
* [Spread and Rest](#spread-and-rest)
* [DOM](#DOM)
* [Event Listeners](#Event-Listeners)
* [Asynchronous JavaScript](#Asynchronous-JavaScript)
* [Promises?](#promises)
* [What are the pros and cons of using Promises instead of callbacks?](#what-are-the-pros-and-cons-of-using-promises-instead-of-callbacks)


### Data types

The latest ECMAScript standard defines 8 data types:

7 data types that are primitives:                // stored in memory on a STACK
- `Boolean`
- `Null`
- `Undefined`
- `Number`
- `BigInt`
- `String`
- `Symbol`
- and `Object`   // reference types

Reference types: // all types of objects         // stored in memory on a HEAP
- `object literals`
- `arrays`
- `functions`
- `dates`
- `all other objects..`

#### STACK

##### primitive 
(they dont change)

```js
let first = 20
let second = first

first = 50

// first
// 50

// second
// 20              // NOT CHANGED 
```

##### object
(they change)

```js
let first = {name: 'alan'}
let second = first

first.name = 'john'

second.name
// "john"                    // CHANGED
```

SHALLOW copying:

```js
let first = {name: 'alan'}
let second = first
let third = Object.assign({},first)        // OBJECT.ASSIGN immutable method      - Object.create DOESNT WORK

first.name = 'john'                        // changing value of original object

second.name                  // CHANGED
// "john"

third.name                   // NOT CHANGED!!!
// "alan"

https://scotch.io/bar-talk/copying-objects-in-javascript
```

DEEP copying:

(for NESTED objects)

```js
let obj = { 
  a: 1,
  b: { 
    c: 2,
  },
}

let newObj = JSON.parse(JSON.stringify(obj));

obj.b.c = 20;                // changing nested value of original object

console.log(obj); 
// { a: 1, b: { c: 20 } }

console.log(newObj); 
// { a: 1, b: { c: 2 } }     (New Object Intact!), with shallow copying c: would change to 20
```

### Hoisting

Hoisting is a term used to explain the behavior of variable declarations in your code. Variables declared or initialized with the `var` keyword will have their declaration "moved" up to the top of the current scope, which we refer to as hoisting. However, only the declaration is hoisted, the assignment (if there is one), will stay where it is.

Note that the declaration is not actually moved - the JavaScript engine parses the declarations during compilation and becomes aware of declarations and their scopes. It is just easier to understand this behavior by visualizing the declarations as being hoisted to the top of their scope. Let's explain with a few examples.

```js
// var declarations are hoisted.

console.log(foo); // undefined

var foo = 1;
console.log(foo); // 1

// let/const declarations are NOT hoisted.

console.log(bar); // ReferenceError: bar is not defined

let bar = 2;
console.log(bar); // 2
```

Function declarations have the body hoisted while the function expressions (written in the form of variable declarations) only has the variable declaration hoisted.

```js
// Function Declaration - HOISTED

console.log(foo); // [Function: foo]

foo(); // 'FOOOOO'

function foo() {
  console.log('FOOOOO');
}
console.log(foo); // [Function: foo]


// Function Expression - NOT HOISTED

console.log(bar); // undefined

bar(); // Uncaught TypeError: bar is not a function

var bar = function() {
  console.log('BARRRR');
};
console.log(bar); // [Function: bar]
```

### Scope

- Global scope
- Local scope
- Function Scope
- Block Scope
- Lexical Scope
- Scope chain

#### Global scope

```js
var carName = "Volvo";

// code here can use carName

function myFunction() {

  // code here can also use carName

}
```

#### Local scope

```js
// code here can NOT use carName

function myFunction() {
  var carName = "Volvo";

  // code here CAN use carName

}
```

#### Function Scope

Function scope means that parameters and variables defined in a function are visible everywhere within the function, but are not visible outside of the function.

```js
function doSomething(){
  console.log(x);
  var x = 1;
}
doSomething(); //undefined


function doSomething(){
  console.log(x);
  let x = 1;
}
doSomething();
//Uncaught ReferenceError: x is not defined
}
```

#### Block Scope

In contrast, the var declaration has no block scope.

Variables declared with let and const can have block scope. They can only be accessed in the block in which they are defined.

```js
if(true){
    var myVar = 1        // var
    }

myVar
// 1


if(true){
    let myVar = 1       // let
    }

myVar
// VM637:1 Uncaught ReferenceError: myVar is not defined
//     at <anonymous>:1:1

}
```

#### Lexical Scope

Lexical scope is the ability of the inner function to access the outer scope in which it is defined.

The log function is a closure. It refers the x variable from its parent function autorun(), not the one from the run() function.

The closure function has access to the scope in which it was created, not the scope in which it was executed.

The local function scope of autorun() is the lexical scope of the log() function.

```js
(function autorun(){
    let x = 1;
    function log(){
      console.log(x);
    };
    
    function run(fn){
      let x = 100;
      fn();
    }
    
    run(log);//1
})();

// 1
```

#### Scope Chain

Every scope has a link to the parent scope. 

When a variable is used, JavaScript looks down the scope chain until it either finds the requested variable or until it reaches the global scope, which is the end of the scope chain.

```js
let x0 = 0;
(function autorun1(){
 let x1 = 1;
  
 (function autorun2(){
   let x2 = 2;
  
   (function autorun3(){
     let x3 = 3;
      
     console.log(x0 + " " + x1 + " " + x2 + " " + x3);//0 1 2 3
    })();
  })();
})();
```

Variables defined in `global scope` are available everywhere in the application.

In a module, a variable declared outside any function is hidden and not available to other modules unless it is explicitly exported.

Function scope means that parameters and variables defined in a function are visible everywhere within the function

Variables declared with let and const have block scope. var doesn’t have block scope.

`In "Strict Mode", undeclared variables are not automatically global.`


### What is `"use strict";`? What are the advantages and disadvantages to using it?

'use strict' is a statement used to enable strict mode to entire scripts or individual functions. Strict mode is a way to opt into a restricted variant of JavaScript.

Advantages:

* Makes it impossible to accidentally create global variables.
* Makes assignments which would otherwise silently fail to throw an exception.
* Makes attempts to delete undeletable properties throw (where before the attempt would simply have no effect).
* Requires that function parameter names be unique.
* `this` is undefined in the global context.
* It catches some common coding bloopers, throwing exceptions.
* It disables features that are confusing or poorly thought out.

Disadvantages:

* Many missing features that some developers might be used to.
* No more access to `function.caller` and `function.arguments`.
* Concatenation of scripts written in different strict modes might cause issues.

Overall, I think the benefits outweigh the disadvantages, and I never had to rely on the features that strict mode blocks. I would recommend using strict mode.

```js

function looseyGoosey() {
  return this
}
 
function noInferringAllowed() {
  "use strict"
  return this
}
 
looseyGoosey() === window; //=> true
noInferringAllowed() === undefined //=> true
```

### Explain how prototypal inheritance works

`Inheritance` refers to an object’s ability to access methods and other properties from another object. 
Objects can inherit things from other objects. 
Inheritance in JavaScript works through something called `prototype`s and this form of inheritance is often called `prototypal inheritance`.

#### Example of Prototypal Inheritance


```javascript
function User(name, email) {
  this.name = name;
  this.email = email;
}
  
User.prototype.sayHello = function() {                      // prototype of a constructor function
  console.log(`Hello everybody, my name is ${this.name}`);
};
 
let sarah = new User('sarah', 'sarah@example.com');
let lauren = new User('Lauren', 'lauren@example.com');
 
sarah.sayHello(); //=> // "Hello everybody, my name is sarah!"
lauren.sayHello(); //=> // "Hello everybody, my name is Lauren!"
```

Things to note are:

The prototype is just a JavaScript Object.
```js
User.prototype;
// {sayHello: ƒ, constructor: ƒ}

typeof User.prototype;
// object
```
To prove the efficiency of sharing methods via prototype:

```js
lauren.sayHello === sarah.sayHello; //=> true
```
In short, `inheritance` in JavaScript is implemented through the `prototype chain`. Every normally created object, array, and function has a `prototype chain` of __proto__ properties ending with Object.prototype at the top. This is why they’re all considered first-class objects in JavaScript.

Functions have a prototype property in addition to the __proto__ property. When using a constructor function with `new`, it’s good practice to place methods on the function’s prototype instead of on the object itself. The returned object’s __proto__ will be equal to the function’s prototype so it will inherit all methods on the function’s prototype. This prevents unnecessary memory usage and improves speed.

We can check if an object has its own property by using the hasOwnProperty method. We can manually set up inheritance by using `Object.create`.


### Prototype Chain

All objects in JavaScript (with a few exceptions) have a `prototype`. Also, an object’s prototype itself is an `object`.
```js

class Dog {
  constructor(name){
    this.name = name;
  }
}

typeof Dog.prototype; // => object
```

Because a prototype is an object, a prototype can have its own prototype! 
In this case, the prototype of Dog.prototype is Object.prototype:

```js
Object.prototype.isPrototypeOf(Dog.prototype);

// returns true
```

How is this useful? You may recall the hasOwnProperty method from a previous challenge:
```js

let duck = new Bird("Donald");
duck.hasOwnProperty("name"); // => true
```

The `hasOwnProperty` method is defined in `Object.prototype`, which can be accessed by `Bird.prototype`, which can then be accessed by `duck`. 

This is an example of the `prototype chain`. 

In this prototype chain, 

`Bird` is the `supertype` for `duck`, 

while `duck` is the `subtype`. 

`Object` is a `supertype` for both `Bird` and `duck`. 

`Object` is a `supertype` for all objects in JavaScript. 

Therefore, any object can use the `hasOwnProperty` method.

```js
class Dog {
  constructor(name){
    this.name = name;
  }
}

let beagle = new Dog("Snoopy");

Dog.prototype.isPrototypeOf(beagle);  // => true

Object.prototype.isPrototypeOf(Dog.prototype);  // => true
```


### Difference Between Class and Prototypal Inheritance?

`Class Inheritance`: 
- instances inherit from classes

- The `extends` keyword

A class is like a blueprint — a description of the object to be created. 
Classes inherit from classes and create subclass relationships: hierarchical class taxonomies.
Instances are typically instantiated via constructor functions with the `new` keyword. Class inheritance may or may not use the `class` keyword from ES6.

```js
class Shoe{
   ...
}

class Boot extends Shoe{
   ...
}

let hikingShoe = new Boot(..)
```


`Prototypal Inheritance`: 
- instances inherit directly from other objects. 

Instances are typically instantiated via factory functions or `Object.create()`.

Instances may be composed from many different objects, allowing for easy selective inheritance.

```js
as above in Example of Prototypal Inheritance
```

The difference between `classical inheritance` and `prototypal inheritance` is that `classical` inheritance is limited to classes inheriting from other classes while `prototypal` inheritance supports the cloning of any object using an object linking mechanism.

![difference](https://res.cloudinary.com/practicaldev/image/fetch/s--P-uVQjti--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/ii4vwgaxg6jyt8e19zpd.png)


##### When is classical inheritance an appropriate choice?

- Rarely, almost never, or never.
- A single level is sometimes OK, from a framework base-class such as React.Component.
- “Favor object composition over class inheritance.”


##### When is prototypal inheritance an appropriate choice?

- In situations where modules or functional programming don’t provide an obvious solution.
- When you need to compose objects from multiple sources. (mixins)
- Any time you need inheritance.

### Explain how `this` works in JavaScript


- Outside of any function, this refers to the global object. In web browsers, this is the window

- Inside an object method, this refers to the object that received the method call

- Inside a standalone function, even one inside a method, this will default to the global object

- When using strict mode in a standalone function, as we do inside classes, this will be undefined

- Arrow functions dont define their own this like standard functions do.

#### Object Method 

```javascript

function User(name, email) {
    this.name = name;
    this.email = email;
}
  // this.sayHello = function(){  
  //  console.log(`Hello everybody, my name is ${this.name}!`);
  // }} - ne koristimo to 

User.prototype.sayHello = function() {
    console.log(`Hello everybody, my name is ${this.name}`);
};

 

let lauren = new User('lauren', 'lauren@gmail.com')
lauren.sayHello()
// "Hello everybody, my name is lauren!"
```

#### class
```javascript

class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }
 
  sayHello() {
    console.log(`Hello, my name is ${this.name}`);
  }
}

-----

class Teacher extends User {
  sayHello(){
    console.log('hello')
  }
}
 
-----

let fred = new User('fred', 'fred@gmail.com')
fred.sayHello()
// Hello, my name is fred
 
let tom = new Teacher('tom', 'tom@gmail.com')
tom.sayHello()                                    // overwritea staru FUNKCIJU 
// hello

----------------------------------------------------------------


class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }
 
  sayHello() {
    console.log(`Hello, my name is ${this.name}`);
  }
}
 

--- 
 
class Teacher extends User {

  teachMath(){
  return `My name is ${this.name} and 1 + 1 is 2.`
  }

  sayHello(){
    super.sayHello()          // SUPER dodaje staru FUNKCIJU da mozemo modificirat staru bez overwritea
    console.log('hello')
  }
}
 
---

let fred = new User('fred', 'fred@gmail.com')
fred.sayHello()
// Hello, my name is fred


let tom = new Teacher('tom', 'tom@gmail.com')
tom.sayHello()
// Hello, my name is tom
// hello

tom.teachMath()    // --> only available to Teacher instance
// My name is Tom and 1 + 1 is 2.

```

## this 
```javascript

let person = {
    greet: function() {   // hash {greet: function()}  --> person.greet
        // this == person
        function otherFunction() {
            // this == window
            return this;
        }
 
        // otherFunction is invoked, returning the functions value of `this`, which is window
        return otherFunction();
    }
};
 
person.greet();
// window


-> NESTED FUNCTIONS:
    1. level=  this -> object 
    2. level=  this -> global window 

```

#### Arrow Functions 

```javascript

let person = {
    greet: function() {
        // this == person
        const otherFunction = () => {
            // this == person still, due to the arrow function
            return this;
        };
 
        // otherFunction is invoked, returning the functions value of `this`, which is person
        return otherFunction();
    }
};
 
person.greet();
// { greet: [Function: greet] }



-> NESTED FUNCTIONS:
    1. level=  this -> object 
    2. level=  this -> object

```

#### Callback

```javascript

[1, 2, 3].filter(function(element) {
    console.log(this);
    return element % 2 == 0;
});
// window
// window
// window

```

#### Class
```javascript

class Person {
    constructor(name) {
        this.name;
    }
 
    greet() {
        function innerFunction() {
            return this;              // refers to greet() not Person object
        }
        return innerFunction();
    }
}
 

let sally = new Person('Sally');
sally.greet();
// undefined


-> NESTED FUNCTIONS:
    1. level=  this -> object 
    2. level=  this -> global window 

```


### What's the difference between `.call` and `.apply`?

Both `.call` and `.apply` are used to invoke functions and the first parameter will be used as the value of `this` within the function. However, `.call` takes in comma-separated arguments as the next arguments while `.apply` takes in an array of arguments as the next argument. An easy way to remember this is C for `call` and comma-separated and A for `apply` and an array of arguments.

```js
function add(a, b) {
  return a + b;
}

console.log(add.call(null, 1, 2)); // 3
console.log(add.apply(null, [1, 2])); // 3
```

### Bind, Call, Apply

##### bind 

The bind method returns a function that needs to be called, but wherever the function that `bind` was called on had a `this` reference, the `this` is "hard set" to what was passed into `bind`.

```javascript

let sally = { name: 'Sally' };
 
function greet(customer) {
    console.log(`Hi ${customer}, my name is ${this.name}!`);
}
 
let newGreet = greet.bind(sally); // newGreet is context-bound to sally
 
newGreet('Bob');                // sally je vec sejvano, "Bob" je customer argument
// Hi Bob, my name is Sally!
 
greet('Bob');                   // sally ovdje nije sejvano, "Bob" je customer argument
// Hi Bob, my name is !



- by calling greet.bind(sally), we return a new function that we then assign to the variable newGreet. 
Invoking newGreet shows that the this object is bound to sally

- Note that the original greet function is unchanged. bind does not change it. 
Instead, bind copies the function, and sets the copied functions this context to whatever is passed 
through as an argument.


greet.bind(sally)('Bob');
// Hi Bob, my name is Sally!

But this is just a noisy way of doing the same work of call() or apply().

```
##### call 

This is a method on a function that calls the function, just like (). You provide a new execution context as the first argument, traditionally called thisArg, and the arguments you want to send to the function after the thisArg. An invocation of call looks like:


##### apply

This is a method on a function that calls the function, just like (). You provide a new execution context as the first argument, traditionally called thisArg, and the arguments you want to send to the function as an Array after the thisArg. An invocation of apply looks like: 

#### .call and .apply 
```javascript


let sally = { name: 'Sally' };
 
function greet(customerOne, customerTwo) {
    console.log(`Hi ${customerOne} and ${customerTwo}, my name is ${this.name}!`);
}
 
greet.call(sally, 'Terry', 'George');        // sally -> this
// Hi Terry and George, my name is Sally!

greet.call(sally);
// Hi undefined and undefined, my name is Sally!


-----------------

var person1 = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
var person2 = {
  firstName:"John",
  lastName: "Doe",
}

person1.fullName.call(person2);  // Will return "John Doe"

-----------------

The APPLY works similarly to call, except that apply only takes two arguments: 
- the value of this, 
- and then an Array of arguments to pass to the function, like so:


greet.apply(sally, ['Terry', 'George']);
// Hi Terry and George, my name is Sally!


----> the first argument to call() or apply() is always the value for this <----

```

```javascript

let asgardianBrothers = [
  {
    firstName: "Thor",
    familyName: "Odinsson"
  },
  {
    firstName: "Loki",
    familyName: "Laufeysson-Odinsson"
  }
]
 
let intro = function(person, line) {
  return `${person.firstName} ${person.familyName} says: ${line}`
}
 
let introWithContext = function(line){
  return `${this.firstName} ${this.familyName} says: ${line}`
}

let phrase = "I like this brown drink very much, bring me another!"
intro(asgardianBrothers[0], phrase) //=> Thor Odinsson says: I like this brown drink very much, bring me another!

intro(asgardianBrothers[0], phrase) === introWithContext.call(asgardianBrothers[0], phrase)     //=> true
intro(asgardianBrothers[0], phrase) === introWithContext.apply(asgardianBrothers[0], [phrase])  //=> true
```


### Classes

Syntactical sugar over JavaScript's existing prototype-based inheritance.

A `constructor` can use the `super` keyword to call the constructor of the super class.

The `extends` keyword is used in class declarations or class expressions to create a class as a child of another class.

If there is a `constructor` present in the subclass, it needs to first call `super()` before using `"this"`.

```js
class Animal { 
  constructor(name) {
    this.name = name;
  }
  
  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name, title) {               // if we have a CONSTRUCTOR here it wont run the CONSTRUCTOR from  					           // class Animal  -> we create a instance with new values
    super(name);                           // IF WE HAVE super() it WILL look for constructor in class Animal
    this.title = title;                    // because its accesing 'this.name' from speak() in class Animal
  }

  speak() {
    console.log(`${this.name} barks and has ${this.title}.`);
  }
}

let ani = new Animal('alan')
ani.speak()
//alan makes a noise.

let dogi = new Dog('semi','spots')
dogi.speak()
// semi barks and has spots.


// Adding Prototype method
Animal.prototype.bark = () => console.log('woof')

ani.bark()
// woof

dogi.bark()
// woof
```

##### Prototype methods 

Array prototype methods:   // stored on Array prototype
```js
sort()
filter()
reduce()
..
```

Date prototype methods:   // stored on Date prototype
```js
getDay()
getMonth()
...
```

- `__proto__` points to the Array `prototype` - this is where the methods you can use are stored

```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  // Getter
  get area() {
    return this.calcArea();
  }
  // Method
  calcArea() {
    return this.height * this.width;
  }
}

const square = new Rectangle(10, 10);

console.log(square.area); // 100
```

##### Static methods

The `static` keyword defines a static method for a class. Static methods are called without instantiating their class and cannot be called through a class instance. Static methods are often used to create utility functions for an application.

```js
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }

  static distance(a, b) {
    const dx = a.x - b.x;
    const dy = a.y - b.y;

    return Math.hypot(dx, dy);
  }
}

const p1 = new Point(5, 5);
const p2 = new Point(10, 10);
p1.distance; //undefined
p2.distance; //undefined

console.log(Point.distance(p1, p2)); // 7.0710678118654755
```




### Module

Module is a collection of components. If we have multiple components that communicate, or simply must be shown together in order to form an integrated whole, then you most likely need a module.

A component may be a variable, function, class and so forth. In other words, everything that can be exported by the export statement is a component (or you can call it a block, a unit etc).

More:
https://www.freecodecamp.org/news/javascript-modules-a-beginner-s-guide-783f7d7a5fcc/

#### Why use modules?

1) `Maintainability`: By definition, a module is self-contained. A well-designed module aims to lessen the dependencies on parts of the codebase as much as possible, so that it can grow and improve independently. Updating a single module is much easier when the module is decoupled from other pieces of code.

2) `Namespacing`: In JavaScript, variables outside the scope of a top-level function are global (meaning, everyone can access them). Because of this, it’s common to have “namespace pollution”, where completely unrelated code shares global variables.

3) `Reusability`


### What is a closure, and how/why would you use one?

A closure is the combination of a function and the lexical environment within which that function was declared. The word `lexical` refers to the fact that lexical scoping uses the location where a variable is declared within the source code to determine where that variable is available. 

`Closures` are functions that have access to the outer (enclosing) function's variables—scope chain even after the outer function has returned.

One drawback to using closures is that they can lead to over-consumption of memory, and possibly memory leaks if not handled properly.

```js
const newTaxFunction = function (countryName, taxRate, ...exemptItems) {
  return function (item, priceInCents) {
    const formattedPrice = '$' + (priceInCents / 100).toFixed(2);
    const exempt = exemptItems.indexOf(item) > -1;
    const taxDue = exempt ? 0 : priceInCents * taxRate / 100;
    const formattedTaxDue = '$' + taxDue.toFixed(2);
 
    console.log(`In ${countryName}, ${item} costs ${formattedPrice}.`);
    console.log('That item', exempt ? 'is' : 'is not', 'exempt from taxation.');
    console.log(`The total tax due is: ${formattedTaxDue}.`);
  };
};

// Generate the closure

const franceTax = newTaxFunction('France', 0.15, 'wine', 'macaron', 'baguette', 'croissant');
const canadaTax = newTaxFunction('Canada', 0.125, 'maple syrup', 'poutine', 'kindness');
const mexicoTax = newTaxFunction('Mexico', 0.05, 'queso', 'futbol', 'tequila', 'avocado');


// Use the closure

canadaTax('poutine', 599);
// LOG: In Canada, poutine costs $5.99.
// LOG: That item is exempt from taxation.
// LOG: The total tax due is: $0.00.
 
canadaTax('futbol', 1999);
// LOG: In Canada, futbol costs $19.99.
// LOG: That item is not exempt from taxation.
// LOG: The total tax due is: $2.50.
 
mexicoTax('Big Mac', 199);
// LOG: In Mexico, Big Mac costs $1.99.
// LOG: That item is not exempt from taxation.
// LOG: The total tax due is: $0.10.
```

Example 2.

```js
function adder(firstDigit){
  let x = firstDigit;
  return function adder2(secondDigit){
    return x + secondDigit
  }
}


let closure = adder(1)    // closes outer function

closure(2)                // calls with arguments for inner function
```

- any function where you are using a variable outside scope are closures
- lexical scoping - looks outside to find variable value
- "Closures are nothing but FUNCTIONS WITH PRESERVED DATA"


### Callbacks 

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

```js
function doHomework(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}
function alertFinished(){
  alert('Finished my homework');
}
doHomework('math', alertFinished);
```

```javascript
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);

```
React:
```javascript
  handleOnChange(event) {                // callback funtion
    this.setState({
      text: event.target.value
    });
  }


  onChange={event => this.handleOnChange(event)} />

```

#### Callback Hell

https://www.freecodecamp.org/news/how-to-deal-with-nested-callbacks-and-avoid-callback-hell-1bc8dc4a2012/

```js
const makeBurger = nextStep => {
  getBeef(function (beef) {
    cookBeef(beef, function (cookedBeef) {
      getBuns(function (buns) {
        putBeefBetweenBuns(buns, beef, function(burger) {
          nextStep(burger)
        })
      })
    })
  })
}

// Make and serve the burger
makeBurger(function (burger) => {
  serve(burger)
})
```

There are four solutions to callback hell:

- Write comments
- Split functions into smaller functions
- Using Promises
- Using Async/await


##### PROMISE 

```js
const makeBurger = () => {
  return getBeef()
    .then(beef => cookBeef(beef))
    .then(cookedBeef => getBuns(beef))
    .then(bunsAndBeef => putBeefBetweenBuns(bunsAndBeef));
};

// Make and serve burger
makeBurger().then(burger => serve(burger));
```




### Name two programming paradigms important for JavaScript app developers

- Prototypal inheritance (also: prototypes, OLOO).
- Functional programming (also: closures, first class functions, lambdas).


### What is functional programming?

Functional programming produces programs by composing mathematical functions and avoids shared state & mutable data.
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

- Pure functions

*Given the same input, will always return the same output. Produces no side effects.*

- Immutability

*Object whose state cannot be modified after it is created. Examples of native JavaScript values that are immutable are numbers and strings. Examples of native JavaScript values that are mutable include objects, arrays, functions, classes, sets, and maps.*

- Function composition

*Process of combining two or more functions to produce a new function.*

- Recursion

*Technique for iterating over an operation by having a function call itself repeatedly until it arrives at a result.*

- Higher-order functions

*Functions that take other functions as arguments or return functions as their results. Taking an other function as an argument is often referred as a callback function, because it is called back by the higher-order function.*

- Currying

*Technique of evaluating function with multiple arguments , into sequence of function with single argument. ... Currying helps you to avoid passing the same variable again and again. It helps to create a higher order function.*

### What is object oriented programming?

Features or mechanisms which makes a Language Object Oriented like:

##### Object:
- using an Object Literal:

```js
//Defining object 
let person = { 
    first_name:'Mukul', 
    last_name: 'Latiyan', 
  
    //method 
    getFunction : function(){ 
        return (`The name of the person is  
          ${person.first_name} ${person.last_name}`) 
    }, 
    //object within object 
    phone_number : { 
        mobile:'12345', 
        landline:'6789'
    } 
} 
console.log(person.getFunction());  
console.log(person.phone_number.landline); 
```

- old way pre ES6:

```js
//using a constructor 
function person(first_name,last_name){ 
   this.first_name = first_name; 
   this.last_name = last_name; 
} 
//creating new instances of person object 
let person1 = new person('Mukul','Latiyan'); 
let person2 = new person('Rahul','Avasthi'); 
  
console.log(person1.first_name); 
console.log(`${person2.first_name} ${person2.last_name}`);
```

- using Object.create() method, + we can use .assign

```js
const Book = { 
   summary : function() { 
      console.log(`${this.title} is written by ${this.author}.`)
   }
}
const book1 = Object.create(Book);   

book1.author = "Paulo Coelho";
book1.title = "Hippie";

console.log(book1.summary());
> Hippie is written by Paulo Coelho.
```

##### Classes & Inheritance
// blueprint of an object, new way ES6 to create Object using Class

```js
class Book {
   constructor(name) {
   // properties
      this.name = name
   }
}

Book.prototype.sayTitle = function() {                   
  console.log(`Title of the book is ${this.name}`);
};

const book = new Book("The Alchemist");

book.sayTitle()

// Title of the book is The Alchemist
```

##### Encapsulation

- The process of wrapping `property` and `function` within a single unit is known as `encapsulation`.
- In the code the `title` and the `author` are only visible inside the scope of the function `Book` and the method summary is visible to the caller of `Book`. So the `title` and the `author` are `encapsulated` inside `Book`.

```js
const Book = function(t, a) {
   let title = t; 
   let author = a; 
   
   return {
      summary : function() { 
        console.log(`${title} written by ${author}.`);
      } 
   }
}
const book1 = new Book('Hippie', 'Paulo Coelho');

book1.summary();
//  Hippie written by Paulo Coelho.
```


### What are the pros and cons of functional programming vs object-oriented programming?

##### OOP Pros: 
It’s easy to understand the basic concept of objects and easy to interpret the meaning of method calls. OOP tends to use an imperative style rather than a declarative style, which reads like a straight-forward set of instructions for the computer to follow.

##### OOP Cons: 
OOP Typically depends on shared state. Objects and behaviors are typically tacked together on the same entity, which may be accessed at random by any number of functions with non-deterministic order, which may lead to undesirable behavior such as race conditions

##### FP Pros: 
Using the functional paradigm, programmers avoid any shared state or side-effects, which eliminates bugs caused by multiple functions competing for the same resources. With features such as the availability of point-free style (aka tacit programming), functions tend to be radically simplified and easily recomposed for more generally reusable code compared to OOP.

##### FP Cons: 
Over exploitation of FP features such as point-free style and large compositions can potentially reduce readability because the resulting code is often more abstractly specified, more terse, and less concrete.


### What are the differences between ES6 class and ES5 function constructors?

Let's first look at example of each:

```js
// ES5 Function Constructor
function Person(name) {
  this.name = name;
}

// ES6 Class
class Person {
  constructor(name) {
    this.name = name;
  }
}
```

For simple constructors, they look pretty similar.

The main difference in the constructor comes when using inheritance. If we want to create a `Student` class that subclasses `Person` and add a `studentId` field, this is what we have to do in addition to the above.

```js
// ES5 Function Constructor
function Student(name, studentId) {
  // Call constructor of superclass to initialize superclass-derived members.
  Person.call(this, name);

  // Initialize subclass's own members.
  this.studentId = studentId;
}

Student.prototype = Object.create(Person.prototype);
Student.prototype.constructor = Student;

// ES6 Class
class Student extends Person {
  constructor(name, studentId) {
    super(name);
    this.studentId = studentId;
  }
}
```

It's much more verbose to use inheritance in ES5 and the ES6 version is easier to understand and remember.


### What advantage is there for using the arrow syntax for a method in a constructor?

The main advantage of using an arrow function as a method inside a constructor is that the value of `this` gets set at the time of the function creation and can't change after that. So, when the constructor is used to create a new object, `this` will always refer to that object. For example, let's say we have a `Person` constructor that takes a first name as an argument has two methods to `console.log` that name, one as a regular function and one as an arrow function:
- binds `this` to the instance of an object upon creation and it cannot change after

```js
const Person = function(firstName) {             // pre ES6
  this.firstName = firstName;
  this.sayName1 = function() { console.log(this.firstName); };
  this.sayName2 = () => { console.log(this.firstName); };
};

const john = new Person('John');
const dave = new Person('Dave');

john.sayName1(); // John
john.sayName2(); // John

// The regular function can have its 'this' value changed, but the arrow function cannot
john.sayName1.call(dave); // Dave (because "this" is now the dave object)
john.sayName2.call(dave); // John

john.sayName1.apply(dave); // Dave (because 'this' is now the dave object)
john.sayName2.apply(dave); // John

john.sayName1.bind(dave)(); // Dave (because 'this' is now the dave object)
john.sayName2.bind(dave)(); // John

var sayNameFromWindow1 = john.sayName1;
sayNameFromWindow1(); // undefined (because 'this' is now the window object)

var sayNameFromWindow2 = john.sayName2;
sayNameFromWindow2(); // John
```

The main takeaway here is that `this` can be changed for a normal function, but the context always stays the same for an arrow function. So even if you are passing around your arrow function to different parts of your application, you wouldn't have to worry about the context changing.

This can be particularly helpful in React class components. If you define a class method for something such as a click handler using a normal function, and then you pass that click handler down into a child component as a prop, you will need to also bind `this` in the constructor of the parent component. If you instead use an arrow function, there is no need to also bind "this", as the method will automatically get its "this" value from its enclosing lexical context. (See this article for an excellent demonstration and sample code: https://medium.com/@machnicki/handle-events-in-react-with-arrow-functions-ede88184bbb)


### What is the definition of a higher-order function?

A higher-order function is any function that takes one or more functions as arguments, which it uses to operate on some data, and/or returns a function as a result. Higher-order functions are meant to abstract some operation that is performed repeatedly. The classic example of this is `map`, which takes an array and a function as arguments. `map` then uses this function to transform each item in the array, returning a new array with the transformed data. Other popular examples in JavaScript are `forEach`, `filter`, and `reduce`. A higher-order function doesn't just need to be manipulating arrays as there are many use cases for returning a function from another function. `Function.prototype.bind` is one such example in JavaScript.

**Map**

Let say we have an array of names which we need to transform each string to uppercase.

```js
const names = ['irish', 'daisy', 'anna'];
```

The imperative way will be as such:

```js
const transformNamesToUppercase = function(names) {
  const results = [];
  for (let i = 0; i < names.length; i++) {
    results.push(names[i].toUpperCase());
  }
  return results;
};
transformNamesToUppercase(names); // ['IRISH', 'DAISY', 'ANNA']
```

Use `.map(transformerFn)` makes the code shorter and more declarative.

```js
const transformNamesToUppercase = function(names) {
  return names.map(name => name.toUpperCase());
};
transformNamesToUppercase(names); // ['IRISH', 'DAISY', 'ANNA']
```

### What are two-way data binding and one-way data flow, and how are they different?

`Two way data binding` means that UI fields are bound to model data dynamically such that when a UI field changes, the model data changes with it and vice-versa.

`One way data flow` means that the model is the single source of truth. Changes in the UI trigger messages that signal user intent to the model (or “store” in React). Only the model has the access to change the app’s state. The effect is that data always flows in a single direction, which makes it easier to understand.

One way data flows are deterministic, whereas two-way binding can cause side-effects which are harder to follow and understand.


### Design Patterns

Design patterns are reusable solutions to commonly occurring problems in software design.

Reusing design patterns can speed up the software development process by providing us with tested and proven solutions to common development problems while ensuring that we write readable, reusable and maintainable codes.

Design patterns can be categorized into `creational patterns`, `structural patterns`, and b`ehavioral patterns`.

#### Creational Pattern
Creational patterns focus on optimizing new object creation so as to suit the situation we are working it. The basic method for object creation might add some design complexities so these patterns help to remove such complexities.

- Constructor pattern
- Module pattern
- Singleton pattern
- Factory pattern
- Prototype pattern

#### Structural Pattern
Structural patterns are concerned with how objects are made up and simplify relationships between different objects. These patterns ensure that objects are structured in a manner that when one part of the system changes, the entire structure of the system doesn't need to do the same.

Decorator
- Facade
- Flyweight

#### Behavioural Pattern
Behavioral design patterns are concerned with the assignment of responsibilities between objects and how objects communicate.

- Mediator
- Observer
- Command

https://www.javascriptjanuary.com/blog/writing-maintainable-and-readable-javascript-design-patterns


#### Can you give an example of one of the ways that working with this has changed in ES6?

ES6 allows you to use [arrow functions](http://2ality.com/2017/12/alternate-this.html#arrow-functions) which uses the [enclosing lexical scope](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#No_separate_this). This is usually convenient, but does prevent the caller from controlling context via `.call` or `.apply`—the consequences being that a library such as `jQuery` will not properly bind `this` in your event handler functions. Thus, it's important to keep this in mind when refactoring large legacy applications.


### Explain why the following doesn't work as an IIFE: `function foo(){ }();`. What needs to be changed to properly make it an IIFE?

IIFE stands for Immediately Invoked Function Expressions. The JavaScript parser reads `function foo(){ }();` as `function foo(){ }` and `();`, where the former is a *function declaration* and the latter (a pair of parentheses) is an attempt at calling a function but there is no name specified, hence it throws `Uncaught SyntaxError: Unexpected token )`.

Here are two ways to fix it that involves adding more parentheses: `(function foo(){ })()` and `(function foo(){ }())`. Statements that begin with `function` are considered to be *function declarations*; by wrapping this function within `()`, it becomes a *function expression* which can then be executed with the subsequent `()`. These functions are not exposed in the global scope and you can even omit its name if you do not need to reference itself within the body.

You might also use `void` operator: `void function foo(){ }();`. Unfortunately, there is one issue with such approach. The evaluation of given expression is always `undefined`, so if your IIFE function returns anything, you can't use it. An example:

```
// Don't add JS syntax to this code block to prevent Prettier from formatting it.
const foo = void function bar() { return 'foo'; }();

console.log(foo); // undefined
```


### What's the difference between a variable that is: `null`, `undefined` or undeclared? How would you go about checking for any of these states?

**Undeclared** variables are created when you assign a value to an identifier that is not previously created using `var`, `let` or `const`. Undeclared variables will be defined globally, outside of the current scope. In strict mode, a `ReferenceError` will be thrown when you try to assign to an undeclared variable. Undeclared variables are bad just like how global variables are bad. Avoid them at all cost! To check for them, wrap its usage in a `try`/`catch` block.

```js
function foo() {
  x = 1; // Throws a ReferenceError in strict mode
}

foo();
console.log(x); // 1
```

A variable that is `undefined` is a variable that has been declared, but not assigned a value. It is of type `undefined`. If a function does not return any value as the result of executing it is assigned to a variable, the variable also has the value of `undefined`. To check for it, compare using the strict equality (`===`) operator or `typeof` which will give the `'undefined'` string. Note that you should not be using the abstract equality operator to check, as it will also return `true` if the value is `null`.

```js
var foo;
console.log(foo); // undefined
console.log(foo === undefined); // true
console.log(typeof foo === 'undefined'); // true

console.log(foo == null); // true. Wrong, don't use this to check!

function bar() {}
var baz = bar();
console.log(baz); // undefined
```

A variable that is `null` will have been explicitly assigned to the `null` value. It represents no value and is different from `undefined` in the sense that it has been explicitly assigned. To check for `null,` simply compare using the strict equality operator. Note that like the above, you should not be using the abstract equality operator (`==`) to check, as it will also return `true` if the value is `undefined`.

```js
var foo = null;
console.log(foo === null); // true
console.log(typeof foo === 'object'); // true

console.log(foo == undefined); // true. Wrong, don't use this to check!
```

As a personal habit, I never leave my variables undeclared or unassigned. I will explicitly assign `null` to them after declaring if I don't intend to use it yet. If you use a linter in your workflow, it will usually also be able to check that you are not referencing undeclared variables.


### What's a typical use case for anonymous functions?

They can be used in IIFEs to encapsulate some code within a local scope so that variables declared in it do not leak to the global scope.

```js
(function() {
  // Some code here.
})();
```

As a callback that is used once and does not need to be used anywhere else. The code will seem more self-contained and readable when handlers are defined right inside the code calling them, rather than having to search elsewhere to find the function body.

```js
setTimeout(function() {
  console.log('Hello world!');
}, 1000);
```

Arguments to functional programming constructs or Lodash (similar to callbacks).

```js
const arr = [1, 2, 3];
const double = arr.map(function(el) {
  return el * 2;
});
console.log(double); // [2, 4, 6]
```


### How do you organize your code? (module pattern, classical inheritance?)

In the past, I've used Backbone for my models which encourages a more OOP approach, creating Backbone models and attaching methods to them.

The module pattern is still great, but these days, I use React/Redux which utilize a single-directional data flow based on Flux architecture. I would represent my app's models using plain objects and write utility pure functions to manipulate these objects. State is manipulated using actions and reducers like in any other Redux application.

I avoid using classical inheritance where possible. When and if I do, I stick to [these rules](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4).


### What's the difference between host objects and native objects?

Native objects are objects that are part of the JavaScript language defined by the ECMAScript specification, such as `String`, `Math`, `RegExp`, `Object`, `Function`, etc.

Host objects are provided by the runtime environment (browser or Node), such as `window`, `XMLHTTPRequest`, etc.


### Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

This question is pretty vague. My best guess at its intention is that it is asking about constructors in JavaScript. Technically speaking, `function Person(){}` is just a normal function declaration. The convention is to use PascalCase for functions that are intended to be used as constructors.

`var person = Person()` invokes the `Person` as a function, and not as a constructor. Invoking as such is a common mistake if the function is intended to be used as a constructor. Typically, the constructor does not return anything, hence invoking the constructor like a normal function will return `undefined` and that gets assigned to the variable intended as the instance.

`var person = new Person()` creates an instance of the `Person` object using the `new` operator, which inherits from `Person.prototype`. An alternative would be to use `Object.create`, such as: `Object.create(Person.prototype)`.

```js
function Person(name) {
  this.name = name;
}

var person = Person('John');
console.log(person); // undefined
console.log(person.name); // Uncaught TypeError: Cannot read property 'name' of undefined

var person = new Person('John');
console.log(person); // Person { name: "John" }
console.log(person.name); // "john"
```


### When would you use `document.write()`?

`document.write()` writes a string of text to a document stream opened by `document.open()`. When `document.write()` is executed after the page has loaded, it will call `document.open` which clears the whole document (`<head>` and `<body>` removed!) and replaces the contents with the given parameter value. Hence it is usually considered dangerous and prone to misuse.


### Explain Ajax in as much detail as possible.

Ajax (asynchronous JavaScript and XML) is a set of web development techniques using many web technologies on the client side to create asynchronous web applications. With Ajax, web applications can send data to and retrieve from a server asynchronously (in the background) without interfering with the display and behavior of the existing page. By decoupling the data interchange layer from the presentation layer, Ajax allows for web pages, and by extension web applications, to change content dynamically without the need to reload the entire page. In practice, modern implementations commonly substitute use JSON instead of XML, due to the advantages of JSON being native to JavaScript.

The `XMLHttpRequest` API is frequently used for the asynchronous communication or these days, the `fetch` API.


### What are the advantages and disadvantages of using Ajax?

**Advantages**

* Better interactivity. New content from the server can be changed dynamically without the need to reload the entire page.
* Reduce connections to the server since scripts and stylesheets only have to be requested once.
* State can be maintained on a page. JavaScript variables and DOM state will persist because the main container page was not reloaded.
* Basically most of the advantages of an SPA.

**Disadvantages**

* Dynamic webpages are harder to bookmark.
* Does not work if JavaScript has been disabled in the browser.
* Some webcrawlers do not execute JavaScript and would not see content that has been loaded by JavaScript.
* Basically most of the disadvantages of an SPA.


### Explain how JSONP works (and how it's not really Ajax).

JSONP (JSON with Padding) is a method commonly used to bypass the cross-domain policies in web browsers because Ajax requests from the current page to a cross-origin domain is not allowed.

JSONP works by making a request to a cross-origin domain via a `<script>` tag and usually with a `callback` query parameter, for example: `https://example.com?callback=printData`. The server will then wrap the data within a function called `printData` and return it to the client.

```html
<!-- https://mydomain.com -->
<script>
function printData(data) {
  console.log(`My name is ${data.name}!`);
}
</script>

<script src="https://example.com?callback=printData"></script>
```

```js
// File loaded from https://example.com?callback=printData
printData({ name: 'Yang Shun' });
```

The client has to have the `printData` function in its global scope and the function will be executed by the client when the response from the cross-origin domain is received.

JSONP can be unsafe and has some security implications. As JSONP is really JavaScript, it can do everything else JavaScript can do, so you need to trust the provider of the JSONP data.

These days, [CORS](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing) is the recommended approach and JSONP is seen as a hack.


### What's the difference between an "attribute" and a "property"?

Attributes are defined on the HTML markup but properties are defined on the DOM. To illustrate the difference, imagine we have this text field in our HTML: `<input type="text" value="Hello">`.

```js
const input = document.querySelector('input');
console.log(input.getAttribute('value')); // Hello
console.log(input.value); // Hello
```

But after you change the value of the text field by adding "World!" to it, this becomes:

```js
console.log(input.getAttribute('value')); // Hello
console.log(input.value); // Hello World!
```


### Why is extending built-in JavaScript objects not a good idea?

Extending a built-in/native JavaScript object means adding properties/functions to its `prototype`. While this may seem like a good idea at first, it is dangerous in practice. Imagine your code uses a few libraries that both extend the `Array.prototype` by adding the same `contains` method, the implementations will overwrite each other and your code will break if the behavior of these two methods is not the same.

The only time you may want to extend a native object is when you want to create a polyfill, essentially providing your own implementation for a method that is part of the JavaScript specification but might not exist in the user's browser due to it being an older browser.


### Difference between document `load` event and document `DOMContentLoaded` event?

The `DOMContentLoaded` event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.

`window`'s `load` event is only fired after the DOM and all dependent resources and assets have loaded.


### What is the difference between `==` and `===`?

`==` is the abstract equality operator while `===` is the strict equality operator. The `==` operator will compare for equality after doing any necessary type conversions. The `===` operator will not do type conversion, so if two values are not the same type `===` will simply return `false`. When using `==`, funky things can happen, such as:

```js
1 == '1'; // true
1 == [1]; // true
1 == true; // true
0 == ''; // true
0 == '0'; // true
0 == false; // true
```

My advice is never to use the `==` operator, except for convenience when comparing against `null` or `undefined`, where `a == null` will return `true` if `a` is `null` or `undefined`.

```js
var a = null;
console.log(a == null); // true
console.log(a == undefined); // true
```

### NaN

The NaN property represents "Not-a-Number" value. This property indicates that a value is not a legal number.

```js
isNaN(NaN);       // true
isNaN(undefined); // true
isNaN({});        // true

isNaN(true);      // false
isNaN(null);      // false
isNaN(37);        // false


// This is a false positive and the reason why isNaN is not entirely reliable
isNaN('blabla');   // true: "blabla" is converted to a number. 
                   // Parsing this as a number fails and returns NaN
```

### Explain the same-origin policy with regards to JavaScript.

The same-origin policy prevents JavaScript from making requests across domain boundaries. An origin is defined as a combination of URI scheme, hostname, and port number. This policy prevents a malicious script on one page from obtaining access to sensitive data on another web page through that page's Document Object Model.


### Why is it called a Ternary expression, what does the word "Ternary" indicate?

"Ternary" indicates three, and a ternary expression accepts three operands, the test condition, the "then" expression and the "else" expression. Ternary expressions are not specific to JavaScript and I'm not sure why it is even in this list.


### Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?

The `load` event fires at the end of the document loading process. At this point, all of the objects in the document are in the DOM, and all the images, scripts, links and sub-frames have finished loading.

The DOM event `DOMContentLoaded` will fire after the DOM for the page has been constructed, but do not wait for other resources to finish loading. This is preferred in certain cases when you do not need the full page to be loaded before initializing.


### Explain what a single page app is and how to make one SEO-friendly.


Web developers these days refer to the products they build as web apps, rather than websites. While there is no strict difference between the two terms, web apps tend to be highly interactive and dynamic, allowing the user to perform actions and receive a response to their action. Traditionally, the browser receives HTML from the server and renders it. When the user navigates to another URL, a full-page refresh is required and the server sends fresh new HTML to the new page. This is called server-side rendering.

However, in modern SPAs, client-side rendering is used instead. The browser loads the initial page from the server, along with the scripts (frameworks, libraries, app code) and stylesheets required for the whole app. When the user navigates to other pages, a page refresh is not triggered. The URL of the page is updated via the [HTML5 History API](https://developer.mozilla.org/en-US/docs/Web/API/History_API). New data required for the new page, usually in JSON format, is retrieved by the browser via [AJAX](https://developer.mozilla.org/en-US/docs/AJAX/Getting_Started) requests to the server. The SPA then dynamically updates the page with the data via JavaScript, which it has already downloaded in the initial page load. This model is similar to how native mobile apps work.

The benefits:

* The app feels more responsive and users do not see the flash between page navigations due to full-page refreshes.
* Fewer HTTP requests are made to the server, as the same assets do not have to be downloaded again for each page load.
* Clear separation of the concerns between the client and the server; you can easily build new clients for different platforms (e.g. mobile, chatbots, smart watches) without having to modify the server code. You can also modify the technology stack on the client and server independently, as long as the API contract is not broken.

The downsides:

* Heavier initial page load due to the loading of framework, app code, and assets required for multiple pages.
* There's an additional step to be done on your server which is to configure it to route all requests to a single entry point and allow client-side routing to take over from there.
* SPAs are reliant on JavaScript to render content, but not all search engines execute JavaScript during crawling, and they may see empty content on your page. This inadvertently hurts the Search Engine Optimization (SEO) of your app. However, most of the time, when you are building apps, SEO is not the most important factor, as not all the content needs to be indexable by search engines. To overcome this, you can either server-side render your app or use services such as [Prerender](https://prerender.io/) to "render your javascript in a browser, save the static HTML, and return that to the crawlers".


### What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?

Some examples of languages that compile to JavaScript include CoffeeScript, Elm, ClojureScript, PureScript, and TypeScript.

Advantages:

* Fixes some of the longstanding problems in JavaScript and discourages JavaScript anti-patterns.
* Enables you to write shorter code, by providing some syntactic sugar on top of JavaScript, which I think ES5 lacks, but ES2015 is awesome.
* Static types are awesome (in the case of TypeScript) for large projects that need to be maintained over time.

Disadvantages:

* Require a build/compile process as browsers only run JavaScript and your code will need to be compiled into JavaScript before being served to browsers.
* Debugging can be a pain if your source maps do not map nicely to your pre-compiled source.
* Most developers are not familiar with these languages and will need to learn it. There's a ramp up cost involved for your team if you use it for your projects.
* Smaller community (depends on the language), which means resources, tutorials, libraries, and tooling would be harder to find.
* IDE/editor support might be lacking.
* These languages will always be behind the latest JavaScript standard.
* Developers should be cognizant of what their code is being compiled to — because that is what would actually be running, and that is what matters in the end.

Practically, ES2015 has vastly improved JavaScript and made it much nicer to write. I don't really see the need for CoffeeScript these days.


### What tools and techniques do you use for debugging JavaScript code?

* React and Redux
  * [React Devtools](https://github.com/facebook/react-devtools)
  * [Redux Devtools](https://github.com/gaearon/redux-devtools)
* Vue
  * [Vue Devtools](https://github.com/vuejs/vue-devtools)
* JavaScript
  * [Chrome Devtools](https://hackernoon.com/twelve-fancy-chrome-devtools-tips-dc1e39d10d9d)
  * `debugger` statement
  * Good old `console.log` debugging


### Explain the difference between mutable and immutable objects.

Immutability is a core principle in functional programming, and has lots to offer to object-oriented programs as well. A mutable object is an object whose state can be modified after it is created. An immutable object is an object whose state cannot be modified after it is created.


#### What is an example of an immutable object in JavaScript?

In JavaScript, some built-in types (numbers, strings) are immutable, but custom objects are generally mutable.

Some built-in immutable JavaScript objects are `Math`, `Date`.

Here are a few ways to add/simulate immutability on plain JavaScript objects.

**Object Constant Properties**

By combining `writable: false` and `configurable: false`, you can essentially create a constant (cannot be changed, redefined or deleted) as an object property, like:

```js
let myObject = {};
Object.defineProperty(myObject, 'number', {
  value: 42,
  writable: false,
  configurable: false,
});
console.log(myObject.number); // 42
myObject.number = 43;
console.log(myObject.number); // 42
```

**Prevent Extensions**

If you want to prevent an object from having new properties added to it, but otherwise leave the rest of the object's properties alone, call `Object.preventExtensions(...)`:

```
var myObject = {
  a: 2
};

Object.preventExtensions(myObject);

myObject.b = 3;
myObject.b; // undefined
```

In non-strict mode, the creation of `b` fails silently. In strict mode, it throws a `TypeError`.

**Seal**

`Object.seal()` creates a "sealed" object, which means it takes an existing object and essentially calls `Object.preventExtensions()` on it, but also marks all its existing properties as `configurable: false`.

So, not only can you not add any more properties, but you also cannot reconfigure or delete any existing properties (though you can still modify their values).

**Freeze**

`Object.freeze()` creates a frozen object, which means it takes an existing object and essentially calls `Object.seal()` on it, but it also marks all "data accessor" properties as writable:false, so that their values cannot be changed.

This approach is the highest level of immutability that you can attain for an object itself, as it prevents any changes to the object or to any of its direct properties (though, as mentioned above, the contents of any referenced other objects are unaffected).

```js
var immutable = Object.freeze({});
```

Freezing an object does not allow new properties to be added to an object and prevents from removing or altering the existing properties. `Object.freeze()` preserves the enumerability, configurability, writability and the prototype of the object. It returns the passed object and does not create a frozen copy.

#### What are the pros and cons of immutability?

**Pros**

* Easier change detection - Object equality can be determined in a performant and easy manner through referential equality. This is useful for comparing object differences in React and Redux.
* Programs with immutable objects are less complicated to think about, since you don't need to worry about how an object may evolve over time.
* Defensive copies are no longer necessary when immutable objects are returning from or passed to functions, since there is no possibility an immutable object will be modified by it.
* Easy sharing via references - One copy of an object is just as good as another, so you can cache objects or reuse the same object multiple times.
* Thread-safe - Immutable objects can be safely used between threads in a multi-threaded environment since there is no risk of them being modified in other concurrently running threads.
* Using libraries like ImmmutableJS, objects are modified using structural sharing and less memory is needed for having multiple objects with similar structures.

**Cons**

* Naive implementations of immutable data structures and its operations can result in extremely poor performance because new objects are created each time. It is recommended to use libraries for efficient immutable data structures and operations that leverage on structural sharing.
* Allocation (and deallocation) of many small objects rather than modifying existing ones can cause a performance impact. The complexity of either the allocator or the garbage collector usually depends on the number of objects on the heap.
* Cyclic data structures such as graphs are difficult to build. If you have two objects which can't be modified after initialization, how can you get them to point to each other?


#### How can you achieve immutability in your own code?

One way to achieve immutability is to use libraries like [immutable.js](http://facebook.github.io/immutable-js/), [mori](https://github.com/swannodette/mori) or [immer](https://github.com/immerjs/immer).

The alternative is to use `const` declarations combined with the techniques mentioned above for creation. For "mutating" objects, use the spread operator, `Object.assign`, `Array.concat()`, etc., to create new objects instead of mutate the original object.

Examples:

```js
// Array Example
const arr = [1, 2, 3];
const newArr = [...arr, 4]; // [1, 2, 3, 4]

// Object Example
const human = Object.freeze({race: 'human'});
const john = { ...human, name: 'John' }; // {race: "human", name: "John"}
const alienJohn = { ...john, race: 'alien' }; // {race: "alien", name: "John"}
```


### Explain the difference between synchronous and asynchronous functions.

Synchronous functions are blocking while asynchronous functions are not. In synchronous functions, statements complete before the next statement is run. In this case, the program is evaluated exactly in order of the statements and execution of the program is paused if one of the statements take a very long time.

Asynchronous functions usually accept a callback as a parameter and execution continue on the next line immediately after the asynchronous function is invoked. The callback is only invoked when the asynchronous operation is complete and the call stack is empty. Heavy duty operations such as loading data from a web server or querying a database should be done asynchronously so that the main thread can continue executing other operations instead of blocking until that long operation to complete (in the case of browsers, the UI will freeze).


### What is event loop? What is the difference between call stack and task queue?

The event loop is a single-threaded loop that monitors the call stack and checks if there is any work to be done in the task queue. If the call stack is empty and there are callback functions in the task queue, a function is dequeued and pushed onto the call stack to be executed.


### Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

The former is a function declaration while the latter is a function expression. The key difference is that function declarations have its body hoisted but the bodies of function expressions are not (they have the same hoisting behavior as variables). For more explanation on hoisting, refer to the question above [on hoisting](#explain-hoisting). If you try to invoke a function expression before it is defined, you will get an `Uncaught TypeError: XXX is not a function` error.

**Function Declaration**

```js
foo(); // 'FOOOOO'
function foo() {
  console.log('FOOOOO');
}
```

**Function Expression**

```js
foo(); // Uncaught TypeError: foo is not a function
var foo = function() {
  console.log('FOOOOO');
};
```


### What are the differences between variables created using `let`, `var` or `const`?

Variables declared using the `var` keyword are scoped to the function in which they are created, or if created outside of any function, to the global object. `let` and `const` are _block scoped_, meaning they are only accessible within the nearest set of curly braces (function, if-else block, or for-loop).

```js
function foo() {
  // All variables are accessible within functions.
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';

  console.log(bar); // bar
  console.log(baz); // baz
  console.log(qux); // qux
}

console.log(bar); // ReferenceError: bar is not defined
console.log(baz); // ReferenceError: baz is not defined
console.log(qux); // ReferenceError: qux is not defined
```

```js
if (true) {
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';
}

// var declared variables are accessible anywhere in the function scope.
console.log(bar); // bar
// let and const defined variables are not accessible outside of the block they were defined in.
console.log(baz); // ReferenceError: baz is not defined
console.log(qux); // ReferenceError: qux is not defined
```

`var` allows variables to be hoisted, meaning they can be referenced in code before they are declared. `let` and `const` will not allow this, instead throwing an error.

```js
console.log(foo); // undefined

var foo = 'foo';

console.log(baz); // ReferenceError: can't access lexical declaration 'baz' before initialization

let baz = 'baz';

console.log(bar); // ReferenceError: can't access lexical declaration 'bar' before initialization

const bar = 'bar';
```

Redeclaring a variable with `var` will not throw an error, but 'let' and 'const' will.

```js
var foo = 'foo';
var foo = 'bar';
console.log(foo); // "bar"

let baz = 'baz';
let baz = 'qux'; // Uncaught SyntaxError: Identifier 'baz' has already been declared
```

`let` and `const` differ in that `let` allows reassigning the variable's value while `const` does not.

```js
// This is fine.
var some = 'alan';
some = 'joe';

let foo = 'foo';
foo = 'bar';

// This causes an exception. Uncaught TypeError: Assignment to constant variable.
const baz = 'baz';
baz = 'qux';
```


### Can you give an example for destructuring an object or an array?

Destructuring is an expression available in ES6 which enables a succinct and convenient way to extract values of Objects or Arrays and place them into distinct variables.

**Array destructuring**

```js
// Variable assignment.
const foo = ['one', 'two', 'three'];

const [ja, ti, on] = foo;
console.log(ja); // "one"
console.log(ti); // "two"
console.log(on); // "three"
```

```js
// Swapping variables
let a = 1;
let b = 3;

[a, b] = [b, a];
console.log(a); // 3
console.log(b); // 1
```

**Object destructuring**

```js
// Variable assignment.
const o = { p: 42, q: true };
const { p, q } = o;

console.log(p); // 42
console.log(q); // true
```


### ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?

Template literals help make it simple to do string interpolation, or to include variables in a string. Before ES2015, it was common to do something like this:

```js
var person = { name: 'Tyler', age: 28 };
console.log('Hi, my name is ' + person.name + ' and I am ' + person.age + ' years old!');
// 'Hi, my name is Tyler and I am 28 years old!'
```

With template literals, you can now create that same output like this instead:

```js
const person = { name: 'Tyler', age: 28 };
console.log(`Hi, my name is ${person.name} and I am ${person.age} years old!`);
// 'Hi, my name is Tyler and I am 28 years old!'
```

Note that you use backticks, not quotes, to indicate that you are using a template literal and that you can insert expressions inside the `${}` placeholders.

A second helpful use case is in creating multi-line strings. Before ES2015, you could create a multi-line string like this:

```js
console.log('This is line one.\nThis is line two.');
// This is line one.
// This is line two.
```

Or if you wanted to break it up into multiple lines in your code so you didn't have to scroll to the right in your text editor to read a long string, you could also write it like this:

```js
console.log('This is line one.\n' +
	'This is line two.');
// This is line one.
// This is line two.
```

Template literals, however, preserve whatever spacing you add to them. For example, to create that same multi-line output that we created above, you can simply do:

```js
console.log(`This is line one.
This is line two.`);
// This is line one.
// This is line two.
```

Another use case of template literals would be to use as a substitute for templating libraries for simple variable interpolations:

```js
const person = { name: 'Tyler', age: 28 };
document.body.innerHTML = `
  <div>
    <p>Name: ${person.name}</p>
    <p>Name: ${person.age}</p>
  </div>
`
```

**Note that your code may be susceptible to XSS by using `.innerHTML`. Sanitize your data before displaying it if it came from a user!**



### What are the benefits of using spread syntax and how is it different from rest syntax?

ES6's spread syntax is very useful when coding in a functional paradigm as we can easily create copies of arrays or objects without resorting to `Object.create`, `slice`, or a library function. This language feature is used often in Redux and RxJS projects.

```js
function putDookieInAnyArray(arr) {
  return [...arr, 'dookie'];
}

const result = putDookieInAnyArray(['I', 'really', "don't", 'like']); // ["I", "really", "don't", "like", "dookie"]

const person = {
  name: 'Todd',
  age: 29,
};

const copyOfTodd = { ...person };
```

ES6's rest syntax offers a shorthand for including an arbitrary number of arguments to be passed to a function. It is like an inverse of the spread syntax, taking data and stuffing it into an array rather than unpacking an array of data, and it works in function arguments, as well as in array and object destructuring assignments.

```js
function addFiveToABunchOfNumbers(...numbers) {
  return numbers.map(x => x + 5);
}

const result = addFiveToABunchOfNumbers(4, 5, 6, 7, 8, 9, 10); // [9, 10, 11, 12, 13, 14, 15]

const [a, b, ...rest] = [1, 2, 3, 4]; // a: 1, b: 2, rest: [3, 4]

const { e, f, ...others } = {
  e: 1,
  f: 2,
  g: 3,
  h: 4,
}; // e: 1, f: 2, others: { g: 3, h: 4 }
```


### How can you share code between files?

This depends on the JavaScript environment.

On the client (browser environment), as long as the variables/functions are declared in the global scope (`window`), all scripts can refer to them. Alternatively, adopt the Asynchronous Module Definition (AMD) via RequireJS for a more modular approach.

On the server (Node.js), the common way has been to use CommonJS. Each file is treated as a module and it can export variables and functions by attaching them to the `module.exports` object.

ES2015 defines a module syntax which aims to replace both AMD and CommonJS. This will eventually be supported in both browser and Node environments.


### Nodejs

Node.js (Node) is an open source development platform for executing JavaScript code server-side. Node is useful for developing applications that require a persistent connection from the browser to the server and is often used for real-time applications such as chat, news feeds and web push notifications.




### Big O

- mathematical notation we use to find out how long an algorithm takes to run (speed) and amount of memory it uses

Good code:
1. readable
2. scalable:
- big O allows to measure scalability of code (how efficient it is)
- speed + memory


![Big O](https://res.cloudinary.com/practicaldev/image/fetch/s--0mOYX8w0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/r38ytuycnzi6hd8dnevh.png)


#### *Big O's

**O(1)** *Constant*- no loops

**O(log N)** *Logarithmic*- usually searching algorithms have log n if they are sorted (Binary Search)

**O(n)** *Linear*- for loops, while loops through n items

**O(n log(n))** *Log Liniear*- usually sorting operations

**O(n^2)** *Quadratic*- every element in a collection needs to be compared to ever other element. Two nested loops

**O(2^n)** *Exponential*- recursive algorithms that solves a problem of size N

**O(n!)** *Factorial*- you are adding a loop for every element

- Iterating through half a collection is still **O(n)**
- Two separate collections: **O(a * b)**

#### *What can cause time in a function?*

**Operations** (+, -, *, /)

**Comparisons** (<, >, ==)

**Looping** (for, while)

**Outside Function call** (function())

#### *BookRule* 

**Rule 1:** Always worst Case

**Rule 2:** Remove Constants

**Rule 3:** Different inputs should have different variables. **O(a+b)**. A and B arrays nested would be **O(a*b)**

**Rule 4:** Drop Non-dominant terms

##### *What causes Space complexity?*

- Variables
- Data Structures
- Function Call
- Allocations


#### _______________________ O(n) ________________________ 

- LINEAR
- as the number of elements increase so does the number of operations (linearly)
- for loops, while loops through n items

- 4 items in array
- 4 operations (is this === 'nemo'?)

```js
const fish = ['dory', 'bruce', 'marlin', 'nemo'];

function findNemo2(fish) {
  for (let i = 0; i < fish.length; i++) {
    if (fish[i] === 'nemo') {
      console.log('Found NEMO!');
    }
  }
}

findNemo2(fish)

// it takes linear time to find nemo
// big 0 depends on number of inputs n
// n -> number of inputs

-> O(n)

op
|
|      *
|    *
|  *
|   
-------------el
```

example 2.

```js
function funChallenge(input) {
  let a = 10;                                // O(1)     not changing
  a = 50 + 3;                                // O(1)

  for (let i = 0; i < input.length; i++) {   // O(n)    n->input
    anotherFunction();                       // O(n)
    let stranger = true;                     // O(n)
    a++;                                     // O(n)
  }
  return a;                                  // O(1)
}


RESULT:

-> 3 + n + n + n + n

-> BIG O(3 + 4n)


OR simplifying:


-> BIG O(n)     // following 4 rules

```

#### _______________________ O(1) ________________________ 

- CONSTANT TIME
- no loops
- algorithm will run the SAME (once in example), regardless of how many elements there are 


```js
function compressFirstBox(boxes){
   console.log(boxes[0])           // O(1)
}


op
|
|      
|    
|  *******
|   
-------------el

- number of operations stay the same

```
example 2.

```js
const boxes = [0,1,2,3,4,5]

    function logFirstTwoBox(boxes){
      console.log(boxes[0]);         // O(1)
      console.log(boxes[1])          // O(1)
    }

logFirstTwoBox(boxes)              // in total -> O(2)  (2->number of operations)
// 0, 1                            // in other words it is called O(1) - constant time

```

#### _______________________ O(n^2) ________________________ 


```js
//Log all pairs of array

const boxes = ['a', 'b', 'c', 'd', 'e'];

function logAllPairsOfArray(array) {
  for (let i = 0; i < array.length; i++) {       // O(n)
    for (let j = 0; j < array.length; j++) {       // O(n) NESTED
      console.log(array[i], array[j])
    }
  }
}

logAllPairsOfArray(boxes)


-> O(n^2)    // nested so multiply


Big-O Complexity Chart - horrible

```

#### _______________________ O(n!) ________________________ 

- adding nested loop for every input (n)

```js
// where n is the argument to the function:

void nFacRuntimeFunc(int n) {
  for(int i=0; i<n; i++) {
    nFacRuntimeFunc(n-1);
  }
}
```

#### 4 Rules

*Rule 1*: Worst Case

*Rule 2*: Remove Constants

*Rule 3*: Different terms for inputs

*Rule 4*: Drop Non Dominants


__________1. Worst Case__________

- always think about this when calculating Big O 

```js
const everyone = ['dory', 'bruce', 'marlin', 'gill', 'bloat', 'nigel', 'squirt', 'darla', 'hank', 'nemo'];

-> "worst case" here is that 'nemo' is at the end of array -> iteration through all elements in array

- if 'nemo' was first in array -> O(1)


function findNemo2(fish) {
  for (let i = 0; i < fish.length; i++) {
    if (fish[i] === 'nemo') {
      console.log('Found NEMO!');
      break;                       // stoping iteration on true
    }
  }
}

findNemo2(fish)
```


__________2. Remove Constants__________

```js
function printFirstItemThenFirstHalfThenSayHi100Times(items) {
    console.log(items[0]);                          // n = 1

    var middleIndex = Math.floor(items.length / 2);
    var index = 0;

    while (index < middleIndex) {                   // n/2
        console.log(items[index]);
        index++;
    }

    for (var i = 0; i < 100; i++) {                 // n = 100
        console.log('hi');
    }
}


--> O(1 + n/2 + 100) - big O 
--> O(n/2 + 1)       

- we only care about items on the CHART
-> removed constants 
----> O(n)    BIG O
```


example 2.
```js
    function compressBoxesTwice(boxes){

      boxes.forEach(box => console.log(box));  // O(n)

      boxes.forEach(box => console.log(box));  // O(n)

    }

-> O(2n)

-> removed constants
----> O(n)    BIG O

- line in graph increases LINEAR
```


__________3. Different terms for inputs__________


```js
    function compressBoxesTwice(boxes , boxes2){   // different terms for inputs

      boxes.forEach(box => console.log(box));  // O(n)

      boxes2.forEach(box => console.log(box));  // O(n)

    }


-> O(n + n)    // not nested so plus
```


__________4. Drop Non Dominants__________

```js
function printAllNumbersThenAllPairSums(numbers) {

  console.log('these are the numbers:');
  numbers.forEach(function(number) {
    console.log(number);
  });

  console.log('and these are their sums:');
  numbers.forEach(function(firstNumber) {
    numbers.forEach(function(secondNumber) {
      console.log(firstNumber + secondNumber);
    });
  });
}

printAllNumbersThenAllPairSums([1,2,3,4,5])


O(n + n^2)

-> drop Non Dominants:

-----> O(n^2)

- n^2 more important than n
```


### Object iteration

```js
let some1 = {
        blogss: ['blog1', 'blog2'],
        getthem: function(){
            this.blogss.forEach(el=>console.log(el))}   // this
}

some1.getthem()
// blog1
// blog2
```

For most objects,  `for .. in` :

```js
let obj = {
    name: 'alan',
    age: 32
}

for (let key in obj){
    console.log(key, obj[key])
}

// name alan
// age 32

for (let key in obj){
    console.log(obj[key])
}

// alan
// 32
```

With ES6, if you need both `keys` and `values` simultaneously, do:

```js
for (let [key, value] of Object.entries(some1)) {
    console.log(key, value);
}

blogss (2) ["blog1", "blog2"]

getthem ƒ (){
            this.blogss.forEach(el=>console.log(el))}
```

To avoid logging inherited properties, check with `hasOwnProperty` :

```js
for (let key in yourobject) {
   if (yourobject.hasOwnProperty(key)) {
      console.log(key, yourobject[key]);
   }
}
```

Iterate on properties by index: yourobject[keys[i]]

```js

let keys = [];
for (let key in yourobject) {      
    if (yourobject.hasOwnProperty(key)) keys.push(key);
}
 
for (let i=300; i < keys.length && i < 600; i++) { 
   console.log(keys[i], yourobject[keys[i]]);
} 
```

### Iterate through an array of objects

##### 1. Just loop through an array

```js
const myArray = [{x:100}, {x:200}, {x:300}];

myArray.forEach((element, index, array) => {
    console.log(element.x); // 100, 200, 300
    console.log(index); // 0, 1, 2
    console.log(array); // same myArray object 3 times
});
```

Note: Array.prototype.forEach() is not a functional way strictly speaking, as the function it takes as the input parameter is not supposed to return a value, which thus cannot be regarded as a pure function.

##### 2. Check if any of the elements in an array pass a test

```js
const people = [
    {name: 'John', age: 23}, 
    {name: 'Andrew', age: 3}, 
    {name: 'Peter', age: 8}, 
    {name: 'Hanna', age: 14}, 
    {name: 'Adam', age: 37}];

const anyAdult = people.some(person => person.age >= 18);
console.log(anyAdult); 
// true
```

##### 3. Transform to a new array

```js
const myArray = [{x:100}, {x:200}, {x:300}];

const newArray= myArray.map(element => element.x);
console.log(newArray); 
// [100, 200, 300]
```

Note: The map() method creates a new array with the results of calling a provided function on every element in the calling array.

##### 4. Sum up a particular property, and calculate its average

```js
const myArray = [{x:100}, {x:200}, {x:300}];

const sum = myArray.map(element => element.x).reduce((a, b) => a + b, 0);
console.log(sum); 
// 600 = 0 + 100 + 200 + 300

const average = sum / myArray.length;
console.log(average);
// 200
```

##### 5. Create a new array based on the original but without modifying it

```js
const myArray = [{x:100}, {x:200}, {x:300}];

const newArray= myArray.map(element => {
    return {
        ...element,
        x: element.x * 2
    };
});

console.log(myArray); 
// [100, 200, 300]
console.log(newArray); 
// [200, 400, 600]


// const newArray = [...myArray].map(el=> el.x * 2 )
// [200, 400, 600]

```

##### 6. Count the number of each category

```js
const people = [
    {name: 'John', group: 'A'}, 
    {name: 'Andrew', group: 'C'}, 
    {name: 'Peter', group: 'A'}, 
    {name: 'James', group: 'B'}, 
    {name: 'Hanna', group: 'A'}, 
    {name: 'Adam', group: 'B'}];

const groupInfo = people.reduce((groups, person) => {
    const {A = 0, B = 0, C = 0} = groups;
    if (person.group === 'A') {
        return {...groups, A: A + 1};
    } else if (person.group === 'B') {
        return {...groups, B: B + 1};
    } else {
        return {...groups, C: C + 1};
    }
}, {});

console.log(groupInfo); 
// {A: 3, C: 1, B: 2}
```

##### 7. Retrieve a subset of an array based on particular criteria

```js
const myArray = [{x:100}, {x:200}, {x:300}];

const newArray = myArray.filter(element => element.x > 250);
console.log(newArray); 
// [{x:300}] 
```

Note: The filter() method creates a new array with all elements that pass the test implemented by the provided function.

##### 8. Sort an array

```js
const people = [
  { name: "John", age: 21 },
  { name: "Peter", age: 31 },
  { name: "Andrew", age: 29 },
  { name: "Thomas", age: 25 }
];

let sortByAge = people.sort(function (p1, p2) {
  return p1.age - p2.age;
});

console.log(sortByAge);

(4) [{…}, {…}, {…}, {…}]
0: {name: "John", age: 21}
1: {name: "Thomas", age: 25}
2: {name: "Andrew", age: 29}
3: {name: "Peter", age: 31}
```

##### 9. Find an element in an array

```js
const people = [ {name: "john", age:23},
                {name: "john", age:43},
                {name: "jim", age:101},
                {name: "bob", age:67} ];

const john = people.find(person => person.name === 'john');
console.log(john);
// {name: "john", age:23}
```
The Array.prototype.find() method returns the value of the first element in the array that satisfies the provided testing function.


## Object methods

#### new Object() - `object constructor` - literal

```js
let person = new Object();

person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";

person
// {firstName: "John", lastName: "Doe", age: 50, eyeColor: "blue"}
```

- different ways for functions in objects: 
```js
let user = {
    login(){
        console.log('loged in');
    },
    logout: () => {
        console.log('loged out');
    }
}

user.login()
// loged in

user.logout()
// loged out
```

#### Create new object using SPREAD - `non-destructive`

```js
const person = {name: 'alan', age: 10}

const some = person

some === person
// true

const some2 = {...person}

some2
// {name: "alan", age: 10}

some2 === person
// false
```


#### Using Class constructor

```js
class Book {
   constructor(name) {
   // properties
      this.name = name
   }
}

Book.prototype.sayTitle = function() {                   
  console.log(`Title of the book is ${this.name}`);
};

const book = new Book("The Alchemist");

book.sayTitle()

// Title of the book is The Alchemist
```

#### Object.create(obj)

The `Object.create()` method creates a new object, using an existing object as the prototype of the newly created object.

```javascript
const person = {
  isHuman: false,
  printIntroduction: function () {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  }
};

const me = Object.create(person);

me.name = "Matthew"; // "name" is a property set on "me", but not on "person"
me.isHuman = true; // inherited properties can be overwritten

me.printIntroduction();
// expected output: "My name is Matthew. Am I human? true"

me === person    // false
```

#### Object.assign(target, sourceObj) - `destructive`  

The `Object.assign()` method copies all enumerable own properties from one or more source objects to a target object. It returns the `target object`.

The `target` object — what to apply the sources’ properties to, which is returned after it is modified.

The `source` object(s) — objects containing the properties you want to apply.


```javascript
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };

const returnedTarget = Object.assign(target, source);

console.log(target);
// expected output: Object { a: 1, b: 4, c: 5 }

console.log(returnedTarget);
// expected output: Object { a: 1, b: 4, c: 5 }
```

##### Object.assign({}, sourceObj) - `non destructive`

```javascript
const obj = { a: 1 };
const copy = Object.assign({}, obj);

console.log(copy); // { a: 1 }
```

##### Object.entries()

The `Object.entries()` method returns an `array` of a given object's own enumerable string-keyed property [key, value] pairs, in the same order as that provided by a for...in loop. (The only important difference is that a for...in loop enumerates properties in the prototype chain as well). 

The order of the array returned by `Object.entries()` does not depend on how an object is defined. If there is a need for certain ordering, then the array should be sorted first, like:

```javascript
Object.entries(obj).sort((a, b) => b[0].localeCompare(a[0]));.
```

```javascript
const anObj = { 100: 'a', 2: 'b', 7: 'c' };

console.log(Object.entries(anObj)); 

// [ ['2', 'b'], ['7', 'c'], ['100', 'a'] ]
```

##### Object.keys()

The `Object.keys()` method returns an `array` of a given object's own enumerable property names, iterated in the same order that a normal loop would.

```javascript
const anObj = { 100: 'a', 2: 'b', 7: 'c' };

console.log(Object.keys(anObj)); 

// console: ['2', '7', '100']
```

##### Object.values()

The `Object.values()` method returns an `array` of a given object's own enumerable property values, in the same order as that provided by a for...in loop. (The only difference is that a for...in loop enumerates properties in the prototype chain as well.)

```javascript
const arrayLikeObj2 = { 100: 'a', 2: 'b', 7: 'c' };

console.log(Object.values(arrayLikeObj2 )); 

// ['b', 'c', 'a']
```

## Array methods

```javascript

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.forEach-----------------------------


const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element)); 

// expected output: "a"
// expected output: "b"
// expected output: "c"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
------------------------.map-------------------------------

const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

// [2, 8, 18, 32]


------------ OBJECT --------------

const people = [ {name: "john", age:23},
                {name: "john", age:43},
                {name: "jim", age:101},
                {name: "bob", age:67} ];
		
let newPeople = people.map( person => {
	if (person.age > 50){
		return {name: person.name, age: 'old'}
		} else {
		return person
		}
});

newPeople

// (4) [{…}, {…}, {…}, {…}]
// {name: "john", age: 23}
// {name: "john", age: 43}
// {name: "jim", age: "old"}
// {name: "bob", age: "old"}

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-------------------------.filter---------------------------

const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

// ["exuberant", "destruction", "present"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
------------------------.find------------------------------

const array1 = [5, 12, 8, 130, 44];

const found = array1.find(element => element > 10);


// found = 12


// learn primjer

function isOdd(element, index, array) {
  return (element %2 === 1);
}
 
console.log([4, 6, 8, 10].find(isOdd)); // undefined, not found
console.log([4, 5, 8, 10].find(isOdd)); // 5


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.reduce-----------------------------


const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));
// expected output: 15


// drugi nacin
[10, 20, 30, 40].reduce(function(memo, i) { return memo + i }) //=> 100
[10, 20, 30, 40].reduce(function(memo, i) { return memo + i }, 100) //=> 200

[10, 20, 30, 40].reduce((memo, i) =>  memo + i ) //=> 100



// learn 1.

function reduceToTotal(values,startingPoint= null){
  const reducer = (accumulator, currentValue) => accumulator + currentValue;
  if (startingPoint === null){
  return values.reduce(reducer)
  } else {
  return values.reduce(reducer,startingPoint)
  }
}


// learn 2.
Using wagesEarnedOnDate, accumulate the value of all dates worked by the employee in the record used as context. 
Amount should be returned as a number.

function calculatePayroll(employees) {
    return employees.reduce((total, e) => total + allWagesFor(e), 0);
}


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.every, .some-----------------------------


function reduceToAllTrue(values){
  const isBelowThreshold = (currentValue) => currentValue ? true : false;
  return values.every(isBelowThreshold);
}


function reduceToAnyTrue(values){
  const isBelowThreshold = (currentValue) => currentValue ? true : false;
  return values.some(isBelowThreshold);
}


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.findIndex---------------------------

const array1 = [5, 12, 8, 130, 44];

const isLargeNumber = (element) => element > 13;

console.log(array1.findIndex(isLargeNumber));
// expected output: 3



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.indexOf----------------------------

const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// expected output: 1

// start from index 2
console.log(beasts.indexOf('bison', 2));
// expected output: 4

console.log(beasts.indexOf('giraffe'));
// expected output: -1



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.flat()-----------------------------


var arr1 = [1, 2, [3, 4]];
arr1.flat(); 
// [1, 2, 3, 4]

var arr2 = [1, 2, [3, 4, [5, 6]]];
arr2.flat();
// [1, 2, 3, 4, [5, 6]]

var arr3 = [1, 2, [3, 4, [5, 6]]];
arr3.flat(2);
// [1, 2, 3, 4, 5, 6]

var arr4 = [1, 2, [3, 4, [5, 6, [7, 8, [9, 10]]]]];
arr4.flat(Infinity);
// [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.join('')----------------------------

fruits.join('')
"BananaOrangeAppleMango"

fruits.join(',')
"Banana,Orange,Apple,Mango"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.slice()------------------------------


var fruits = ["Banana", "Orange", "Apple", "Mango"];

function returnFirstTwoDrivers(fruits) {
  return fruits.slice(0, 2);
};
// fruits = ["Banana", "Orange"];

const returnLastTwoDrivers = function (fruits) {
  return fruits.slice(-2);
};
// fruits = ["Apple", "Mango"];



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.splice()----------------------------


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");

// fruits = ["Banana", "Orange", "Lemon", "Kiwi", "Apple", "Mango"]


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);        // Removes the first element of fruits



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.sort()-----------------------------
-----------------------.reverse()--------------------------

-> destructive - changes original array

STRINGS:

var fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.sort();                        // First sort the elements of fruits
// ["Apple", "Banana", "Mango", "Orange"]

fruits.reverse();                    // Then reverse the order of the elements
// ["Mango", "Apple", "Orange", "Banana"]


-> non destructive:

var fruits = ["Banana", "Orange", "Apple", "Mango"];

let some = [...fruits].sort()

some
// ["Apple", "Banana", "Mango", "Orange"]

fruits
// ["Banana", "Orange", "Apple", "Mango"]


NUMBERS:

- non destructive -> let some = [...primes].sort((a, b) => a - b) 

-> destructive - changes original array:

const primes = [13, 7, 17, 2, 5, 3];
const array = [5, 6, -1, 1, 3]

primes.sort((a, b) => a - b)         // ascending

// [ 2, 3, 5, 7, 13, 17 ]

primes.sort((a, b) => b - a)         // descending 

// [ 17, 13, 7, 5, 3, 2 ]


array.sort((a , b) => a - b)
// [ -1, 1, 3, 5, 6 ]


MATH sorting LIST:

Math.min(0, 150, 30, 20, -8, -200);  // returns -200

Math.max(0, 150, 30, 20, -8, -200);  // returns 150

Math.random();     // returns a random number


---------------- .sort() with a callback ------------------

const primes = [13, 7, 17, 2, 5, 3];

const numberSorter = function (num1, num2) {      // ES5
  return num1 - num2;
};

primes.sort(numberSorter);
// => [2, 3, 5, 7, 13, 17]


If num1 is larger than num2, the subtraction operation will return a positive number, 
which tells .sort() to reverse the order of num1 and num2 in the array. 
If num1 - num2 returns a negative number or 0, .sort() knows to not mess with the ordering.



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.push('Kiwi')-------------------------


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi"); 

// fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.pop()--------------------------------


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();

// fruits = ["Banana", "Orange", "Apple"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.unshift('Lemon')---------------------


var fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.unshift("Lemon")
// 5

// fruits = ["Lemon", "Banana", "Orange", "Apple", "Mango"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.shift()-----------------------------

var fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.shift()
"Banana"

// fruits = ["Orange", "Apple", "Mango"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.toString()---------------------------

var fruits = ["Banana", "Orange", "Apple", "Mango"];

ruits.toString()

// "Banana,Orange,Apple,Mango"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.concat(arr)------------------------

var myGirls = ["Cecilie", "Lone"];
var myBoys = ["Emil", "Tobias", "Linus"];
var myChildren = myGirls.concat(myBoys);

// myChildren = ["Cecilie", "Lone", "Emil", "Tobias", "Linus"]

```


## String methods

```js

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.charAt()----------------------------

var sentence = 'The quick brown fox jumps over the lazy dog.';

var index = 4;

console.log('The character at index ' + index + ' is ' + sentence.charAt(index));
// expected output: "The character at index 4 is q"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.concat()----------------------------

var str1 = 'Hello';
var str2 = 'World';

console.log(str1.concat(' ', str2));
// expected output: "Hello World"

console.log(str2.concat(', ', str1));
// expected output: "World, Hello"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
--------------------.includes()----------------------------

var sentence = 'The quick brown fox jumps over the lazy dog.';

var word = 'fox';

console.log(`The word "${word}" ${sentence.includes(word)? 'is' : 'is not'} in the sentence`);
// expected output: "The word "fox" is in the sentence"


function diffArray(arr1, arr2) {
  return arr1
    .concat(arr2)
    .filter(item => !arr1.includes(item) || !arr2.includes(item));
}
// difference between 2 arrays

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.indexOf()----------------------------

var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

var searchTerm = 'dog';
var indexOfFirst = paragraph.indexOf(searchTerm);

console.log('The index of the first "' + searchTerm + '" from the beginning is ' + indexOfFirst);
// expected output: "The index of the first "dog" from the beginning is 40"

console.log('The index of the 2nd "' + searchTerm + '" is ' + paragraph.indexOf(searchTerm, (indexOfFirst + 1)));
// expected output: "The index of the 2nd "dog" is 52"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.lastIndexOf()------------------------

var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

var searchTerm = 'dog';

console.log('The index of the first "' + searchTerm + '" from the end is ' + paragraph.lastIndexOf(searchTerm));
// expected output: "The index of the first "dog" from the end is 52"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
------------------------.length----------------------------

var str = 'Life, the universe and everything. Answer:';
  
console.log(str + ' ' + str.length);
// expected output: "Life, the universe and everything. Answer: 42"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-------------------.localeCompare()------------------------

var a = 'réservé'; // with accents, lowercase
var b = 'RESERVE'; // no accents, uppercase

console.log(a.localeCompare(b));
// expected output: 1
console.log(a.localeCompare(b, 'en', {sensitivity: 'base'}));
// expected output: 0



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
------------------------.match()---------------------------

var paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
var regex = /[A-Z]/g;
var found = paragraph.match(regex);

console.log(found);
// expected output: Array ["T", "I"]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.replace()---------------------------

var p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';

var regex = /dog/gi;

console.log(p.replace(regex, 'ferret'));
// expected output: "The quick brown fox jumps over the lazy ferret. If the ferret reacted, was it really lazy?"

console.log(p.replace('dog', 'monkey'));
// expected output: "The quick brown fox jumps over the lazy monkey. If the dog reacted, was it really lazy?"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.search()----------------------------

var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

// any character that is not a word character or whitespace
var regex = /[^\w\s]/g;

console.log(paragraph.search(regex));
// expected output: 43

console.log(paragraph[paragraph.search(regex)]);
// expected output: "."



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.slice()----------------------------

var str = 'The quick brown fox jumps over the lazy dog.';

console.log(str.slice(31));
// expected output: "the lazy dog."

console.log(str.slice(4, 19));
// expected output: "quick brown fox"

console.log(str.slice(-4));
// expected output: "dog."

console.log(str.slice(-9, -5));
// expected output: "lazy"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
---------------------.split()------------------------------

var str = 'The quick brown fox jumps over the lazy dog.';

var words = str.split(' ');
console.log(words[3]);
// expected output: "fox"

var chars = str.split('');
console.log(chars[8]);
// expected output: "k"

var strCopy = str.split();
console.log(strCopy);
// expected output: Array ["The quick brown fox jumps over the lazy dog."]



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
--------------------.substring()---------------------------

var str = 'Mozilla';

console.log(str.substring(1, 3));
// expected output: "oz"

console.log(str.substring(2));
// expected output: "zilla"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
--------------------.toLowerCase()-------------------------

var sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toLowerCase());
// expected output: "the quick brown fox jumps over the lazy dog."



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
--------------------.toUpperCase()-------------------------

var sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toUpperCase());
// expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
----------------------.toString()--------------------------

var stringObj = new String("foo");

console.log(stringObj);
// expected output: String { "foo" }

console.log(stringObj.toString());
// expected output: "foo"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.valueOf()--------------------------

var stringObj = new String("foo");

console.log(stringObj);
// expected output: String { "foo" }

console.log(stringObj.valueOf());
// expected output: "foo"



/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------.typeof --------------------------

console.log(typeof 42);
// expected output: "number"

console.log(typeof 'blubber');
// expected output: "string"

console.log(typeof true);
// expected output: "boolean"

console.log(typeof undeclaredVariable);
// expected output: "undefined";


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
-----------------------ITERATION --------------------------

// With ES6

var some = 'uololooo';

[...some ].forEach(c => console.log(c))

u
o
l
o
.
.

// ES5 without the for loop:
text.split('').forEach(function(c) {
    console.log(c);
});

// regular
for (var i = 0; i < str.length; i++) {
  console.log(str.charAt(i));
}

```

## Spread and Rest

#### Spread
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax

Arrays:
```js
const people = ['alan', 'joe', 'mike']
console.log(...people)

// alan joe mike                              // spreads array
```

```js
const people = ['alan', 'joe', 'mike']
const members = ['herc', 'big', ...people]
console.log(members)

// (5) ["herc", "big", "alan", "joe", "mike"]                // spreads array and adds to new one
```

Object:

```js
const person = {name: 'alan', age: 10}
const some = person

some === person
// true

const some2 = {...person}
some2
// {name: "alan", age: 10}

some2 === person
// false                        // creating a full copy - not a pointer
```

#### Rest

- allows us to bundle up arguments inside function in to a single array parameter

```js
const double = (...nums) => {              // takes all arguments and bundles in to single array
	console.log(nums)
	return nums.map(num => num*2)
}

const result = double(1,2,3,4,5,6,7)
console.log(result)

// (7) [1, 2, 3, 4, 5, 6, 7]               // new array
// (7) [2, 4, 6, 8, 10, 12, 14]
```





## DOM

- Document Object Model

### The Query Selector

https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector
https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll

```js
// returns only FIRST:
let el = document.querySelector("h1");
let el = document.querySelector(".myclass");
let el = document.querySelector("#idname");

// return specific:
let el = document.querySelector("div.myclass");
(dev tools -> elements -> right click on element -> copy -> copy selector)

// returns ALL:
let matches = document.querySelectorAll("p");
let matches = document.querySelectorAll(".myclass");
let matches = document.querySelectorAll("#idname");
```

### Adding and Changing Page Content

- changing TEXT:

```js
let el = document.querySelector("h1");

el.innerText                        // returns text
el.innerText = 'something new'      // changes text
el.innerText += 'something new'     // adds text
```

```js
let matches = document.querySelectorAll("p");

matches.forEach( el => {
	el.innerText += ' extra text';
})
```

- changing HTML:

```js
let el = document.querySelector("h1");

el.innerHTML = '<p>something</p>'    // replaces with new HTML
el.innerHTML += '<p>something</p>'   // adds new HTML bellow
```

```js
let content = document.querySelector("h1");
let people = ['alan', 'john', 'mike'];

people.forEach( el => {
	content.innerHTML += `<p>${el}</p>`;
})
```

### Getting and Setting Attributes

.getAttribute, .setAttribute

```js
<a href='https://www.google.com'> Click Here </a>

let link = document.querySelector("a");

link.getAttribute('href')                                  // getAttribute -> returns href string
link.setAttribute('href', 'https://www.amazon.com')        // setAttribute -> changes href string
```

### Changing CSS Styles

.style

```js
let el = document.querySelector("h1");
 
el.style.color                // returns 'orange'    -> color: 'orange'    (object)
el.style.margin = '50px'      // adds margin to style without overwriting all
el.style.fontSize = '60px'    // instead font-size
```

### Adding and Removing Classes

.add, .remove, .toggle

```js
<p class='error'> text </p>

let content = document.querySelector("p");

content.classList.add('error')                // adding a CLASS if no class is there
content.classList.add('success')                // adding and replacing existing CLASS 
content.classList.remove('success')             // remove a CLASS if no class is there
```

Example:
```js
// if error then add error class, if success then add success class

<p> error </p>
<p> error </p>
<p> success </p>
<p> error </p>
<p> success </p>

let all = document.querySelectorAll('p')

let new = all.forEach( el => {
	if( el.innerText === 'error'){           // instead of el.innerText -> el.textContent ( better for not visible text )
						 // other way -> if ( el.textContent.includes('error')
		el.classList.add('error')
	} else {
		el.classList.add('success')
		}
	})
```

#### Toggle Class

```js
let content = document.querySelector(".title");       // already has a class of '.title'

content.classList.toggle('test');                     // 	 adds '.title .test'
content.classList.toggle('test');                     // (again) removes '.title'

```

### NODE Parents, Children & Siblings

- used for dynamic changes (when we dont know the class,tag or it generates randomly)

![node](https://www.qualitestgroup.com/images/howto/DOMTree_HowTo.png)
https://www.w3schools.com/js/js_htmldom_navigation.asp


##### PARENT - CHILD
```js
// accessing children in collection

1. non-destructive creation of array:

<article>
	<h1> text </h1>
	<p> text </p>
	<p> text </p>
	<div> text </div>
</article>

let newArr = Array.from(article.children)      // children method
// [4]


2. iterating

newArr.forEach( child => {
	child.classList.add('newclass')       // adding class to each item
})
```

##### Finding PARENT 

```js
let element = document.querySelector('h1')

let parent = element.parentElement            // parentElement method
```

##### Finding SIBLING 

```js
let element = document.querySelector('h1')

let nextSibling = element.nextElementSibling               // nextElementSibling method
let previousSibling = element.previousElementSibling       // previousElementSibling method

```

### Event Listeners

https://developer.mozilla.org/en-US/docs/Web/Events

```js
// individial element

const button = document.querySelector('button')   

button.addEventListener('click', () => {          // listens for click event and fires a function
	console.log('you clicked me')
})
```
```js
// if we have more elements (li tag) 

const list = document.querySelectorAll('li')

list.forEach(el=> {
	el.addEventListener('click', e => {
		e.target.style.textDecoration = 'line-through'      // on click it changes specific <li> style
		})
	})
```

### Creating and Removing Elements

Remove clicked li:
	
```js
const list = document.querySelectorAll('li')

list.forEach(el=> {
	el.addEventListener('click', e => {
		e.target.remove()                       // on click remove() method removes <li>
		})
	})
```

Add li element on button click:
	
```js
const button = document.querySelector('button')   

const ul = document.querySelector('ul')            // took <ul> that has 4 <li>

button.addEventListener('click', () => {          
	// ul.innerHTML += '<li> added new li </li>'     // adds new <li>  
	
	const li = document.createElement('li');          // BETTER WAY createElement method
	li.textContent = 'added new li';
	
	ul.appent(li)                                     // .append (adds to the bottom)
	el.prepend(li)                                    // .prepend (adds to the top)
})
```

### Event Bubbling and Delegation

EVENT BUBBLING:

When an event triggers on a DOM element, it will attempt to handle the event if there is a listener attached, then the event is bubbled up to its parent and the same thing happens. This bubbling occurs up the element's ancestors all the way to the document. 
Event bubbling is the mechanism behind event delegation.


EVENT DELEGATION is a technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM. The benefits of this technique are:

* Memory footprint goes down because only one single handler is needed on the parent element, rather than having to attach event handlers on each descendant.
* There is no need to unbind the handler from elements that are removed and to bind the event for new elements.

- when we click on a specific LI, that one becomes a EVENT TARGET

https://www.udemy.com/course/modern-javascript-from-novice-to-ninja/learn/lecture/14174917#overview


We dont need eventListener on every LI, we can add one on UL:

```js
const ul = document.querySelector('ul') 

ul.addEventListener('click', e => {
	console.log(e.target)                  // on <li> click it console logs that <li>
	
	if (e.target.tagName === 'LI'){
		e.target.remove()              // removes clicked <li> via bubbling
	}
})
```

### Asynchronous JavaScript

'start now - finish later(callback)'

- JS runs one statement (function) at the time
- example: `setTimeout()`

#### API fetch() + Promise

https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch

- to get data from a server to API endpoints (data as JSON format)

- `.then` -> RESOLVED 
- `.catch` -> promise is REJECTED only when there is an NETWORK ERROR

```js
fetch('http://example.com/movies.json')
  .then((response) => {
    return response.json();
  })
  .then((myJson) => {                       // API json data RESOLVED
    console.log(myJson);
  })
  .catch(err => {                           // REJECTED         
   console.log('rejected', err);
  }) 

```

```js
const bindClickHandlers = () => {
    $('.all_lessons').on('click', e => {           // on click shows all lessons
        e.preventDefault()
        history.pushState(null, null, "lessons")
        getLessons()
  })


// index lessons Ajax     

  const getLessons = () => {
    fetch(`/lessons.json`)
      .then(res => res.json())
      .then(lessons => {                    // API json data
         $('#app-container').html('')
         lessons.forEach(lesson => {
           let newLesson = new Lesson(lesson)
           let lessonHtml = newLesson.formatIndex()
           $('#app-container').append(lessonHtml)
         })
      })
  }
```


#### Async & Await (instead of using .then)

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function

The `async function` declaration defines an `asynchronous function` — a function that returns an `AsyncFunction object`. Asynchronous functions operate in a separate order than the rest of the code via the event loop, returning an implicit `Promise` as its result.

- create function for all async code
- `async function` ALWAYS returns a `promise` whatever is inside
- we use `fetch()` inside to grab data

- `await` stops assinging a value to (const response) until the `promise` is `resolved`
- cleaner way 
- non blocking


```js
const getTodos = async () => {                              // async - added to convert to async function
	
	// with ASYNC and AWAIT we dont need to do ->        fetch('todos/luigi.json').then(() => {...})
	
	const response = await fetch('todos/luigi.json');         // using AWAIT instead .THEN
	const data = await response.json();            	          // returns value of promise when RESOLVED
	return data;
}

// calling:

console.log(1);
console.log(2);

getTodos()
     .then(data => {console.log('resolved', data)})           // have to use .then when calling 
     .catch(err => console.log('rejected', err))              // ERROR if there is problem with json fetch
	
console.log(3);
console.log(4);

// 1
// 2
// 3
// 4
// resolved (3) [{..}, {..}, {..}]                  -> resolved async code - NON BLOCKING async function
	
```



### Promises?

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise

A promise is an object that may produce a single value sometime in the future: either a resolved value or a reason that it's not resolved (e.g., a network error occurred). 

A promise may be in one of 3 possible states: `fulfilled`, `rejected`, or `pending`. 

Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.

Create a promise:
```js
const myFirstPromise = new Promise((resolve, reject) => {
  // do something asynchronous which eventually calls either:
  //
  //   resolve(someValue)        // fulfilled
  // or
  //   reject("failure reason")  // rejected
});
```

Redux promise:

```js
// asynchronous action creators

export const login = (credentials) => {     
    return dispatch => {                    
        return fetch("http://localhost:3001/api/v1/login", {
          credentials: "include",
          method: "POST",
          headers: {
            "Content-Type": "application/json"
          },
          body: JSON.stringify(credentials)
        })                               
        .then(r => r.json())
        .then(response => {                  // promise
          if (response.error) { 
            alert(response.error)
          } else {
            dispatch(setCurrentUser(response.data)) 
            dispatch(getMyComments())   
          }
        })
        .catch(console.log)
    }
  }
  ```
  
##### Example 1.

```js
const getSomething = () => {

	return new Promise((resolve,reject) => {    // takes a function as argument
	// fetch something
	// if we get some data:
	resolve(data);              // data 
	// if there is an error
	reject('some error')
	});
}

// returns promise that will be RESOLVED or REJECTED at some point
// .then -> this callback function will fire IF the PROMISE is RESOLVED

// second callback function IF REJECTED (.catch)

getSomething().then( data => {
	console.log(data)           // data from promise IF RESOLVED
}).catch(err => {                         // second callback function IF REJECTED
	console.log(err);
});


```
  
  
##### Example 2.  XMLHttpRequest (old way)

```js
// function that creates a Promise

const getTodos = (resource) => {

    return new Promise((resolve,reject) => {
        const request = new XMLHttpRequest();                 // OLD WAY -> new way FETCH
	
	request.addEventListener('readystatechange', () => {
	    if(request.readyState === 4 && request.status === 200){
	       const data = JSON.parse(request.responseText);
	       resolve(data);
	    } else if(request.readyState === 4){
	        reject('error getting resource');
	    }
	  });
	  
	  request.open('GET', resource);
	  request.send();
	});
};	

// calling the function with API and returning some data

getTodos('todos/luigi.json').then(data => {        // .then   for data
	console.log('promise resolved:' data);
  }).catch(err => {                                // .catch  for error
  	console.log('promise rejected:' err);
});
```



![promises](https://media.prod.mdn.mozit.cloud/attachments/2018/04/18/15911/32e79f722e83940fdaea297acdb5df92/promises.png)


### What are the pros and cons of using Promises instead of callbacks?

**Pros**

* Avoid callback hell which can be unreadable.
* Makes it easy to write sequential asynchronous code that is readable with `.then()`.
* Makes it easy to write parallel asynchronous code with `Promise.all()`.
* With promises, these scenarios which are present in callbacks-only coding, will not happen:
  * Call the callback too early
  * Call the callback too late (or never)
  * Call the callback too few or too many times
  * Fail to pass along any necessary environment/parameters
  * Swallow any errors/exceptions that may happen

**Cons**

* Slightly more complex code (debatable).
* In older browsers where ES2015 is not supported, you need to load a polyfill in order to use it.

