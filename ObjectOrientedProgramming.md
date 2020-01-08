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
