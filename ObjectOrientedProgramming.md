* [Create a Method on an Object using `this`](#create-a-method-on-an-object-using-`this`)
* [Constructor function with arguments ES6, ES5](#Constructor-function-with-arguments-ES6,ES5)
* [Verify an Object's Constructor with instanceof](#verify-an-object's-constructor-with-instanceof)


### Create a Method on an Object using `this`

```js
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function() {return "This dog has " + this.numLegs + " legs.";}
};

dog.sayLegs();

// "This dog has 4 legs."

```

### Constructor function with arguments ES6, ES5

```js
ES6

class Person {
  constructor(firstName, lastName, age, eyeColor) {
    this.firstName = firstName; 
    this.lastName = lastName;
    this.age = age;
    this.eyeColor = eyeColor;
    this.changeName = function (name) {
      this.lastName = name;
  };
}}


ES5

function Person(firstName, lastName, age, eyeColor) {
  this.firstName = firstName; 
  this.lastName = lastName;
  this.age = age;
  this.eyeColor = eyeColor;
  this.changeName = function (name) {
    this.lastName = name;
  };
}


let myMother = new Person("Sally", "Rally", 48, "green");

myMother 
// Person {firstName: "Sally", lastName: "Rally", age: 48, eyeColor: "green", changeName: ƒ}

myMother.age
// 48

myMother.changeName("Angie")
myMother.lastName
// Angie
```

#### Verify an Object's Constructor with instanceof

```js
myMother instanceof Person 

// true
```

### Iterate Over All Properties (own & prototype)

```js
class Dog {
  constructor(name){
    this.name = name;
  }
}

Dog.prototype.numLegs = 4;

let beagle = new Dog("Snoopy");

let ownProps = [];
let prototypeProps = [];

// Add your code below this line

for(let key in beagle){                          // object iterator
  if (beagle.hasOwnProperty(key)){
    ownProps.push(key)
  } else {
    prototypeProps.push(key)
  }
}

console.log(ownProps); // prints ["name"]
console.log(prototypeProps); // prints ["numLegs"]


Dog.prototype.isPrototypeOf(beagle);            // checking property
// returns true
```

### Set prototype with multiple object properties   

```js
Bird.prototype = {
  numLegs: 2, 
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name);
  }
};
```

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


### Use Inheritance So You Don't Repeat Yourself 

Notice in the example below that the `eat` method is shared by Cat and Bear:

```js
class Cat {
  constructor(name){
    this.name = name;
  }
}

Cat.prototype = {
  constructor: Cat,
  eat: function() {
    console.log("My name is " + this.name);
  }
};


class Bear {
  constructor(name){
    this.name = name;
  }
}

Bear.prototype = {
  constructor: Bear,
  eat: function() {
    console.log("My name is " + this.name);
  }
};
```

The code can be edited to follow the DRY principle by creating a `SUPERTYPE` (or parent) called Animal:

```js
function Animal() { };   // or class

Animal.prototype = {
  constructor: Animal, 
  eat: function() {
    console.log("My name is " + this.name);
  }
};
```

Since Animal includes the describe method, you can remove it from Bird and Bear:

```js
Cat.prototype = {
  constructor: Bird
};

Bear.prototype = {
  constructor: Dog
};
```

### Inherit Behaviors from a Supertype & Set the Child's Prototype to an Instance of the Parent

```js
function Animal() {}   // or class

Animal.prototype = {
  constructor: Animal,
  eat: function() {
    console.log("nom nom nom");
  }
};

function Dog() {}   // or class

Dog.prototype = Object.create(Animal.prototype);  //  Dog now includes all the key "ingredients" from Animal. 

let beagle = new Dog();                           // beagle inherits all of Animal's properties, including the eat method.

beagle.eat(); // Should print "nom nom nom"
```
