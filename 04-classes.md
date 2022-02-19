# Javascript Classes

Classes in Javascript are exactly similar to classes in other programming languages. JS Classes are also an abstraction of collection of Objects also known as a blueprint for Javascript Objects. All the entities of the same class have common properties and methods. Classes are also a type of function with superpowers which can be handled dynamically under any kind of inputs and workflow. Similar to functions, classes can also be declared and referred. Variables used inside classes are called Properties and functions used inside classes are called Methods

```javascript
// declaration using class keyword
class Car {
    getInfo(name = "Default CAR") {
        console.log(name + "is a good car")
    }
}
// classes cannot execute on their own, they have to be converted into an object. this is called creating an instance of the class
var bwm = Car()
// methods of a class can be called the same way we call values of an object
bmw.getInfo("BMW M3")
// expected output
// BMW M3 is a good car
```

# this and constructor()

Notice that we passed an argument to the `getInfo()` method. This is generally not a good way of writing code. Instead it can be done using by setting global values with respect to the current parent class and passing values to this global scope. To create a global scope within the class we use the `contructor()` and to pass values to it we use `this` keyword. `contructor()` defined the way in which the object is created and `this` sets up a reference to the constructor.

```javascript
// refactoring the above code with constructor() and this
class Car {
    constructor(_name) { 
        // _name can be replaced with any variable name, but be sure to use the same throughout the program
        this.name = _name;
    }
    getInfo() {
        console.log(this.name + "is a good car")
    }
}
var bmw = new Car("BMW M3") // we pass the name as an argument to the instance
bmw.getInfo()
```

# Inheritance, extends, super() & super

Inheritance means deriving subclasses form a base class. In simple words using the properties and methods of another class into a new class is known as Inheritance. In order to inherit from a base class we use the `extends` keyword. The `super()` method has to be called in the constructor of the new class before using `this` keyword. Finally methods can be accessed using the `super.methodName` statement.

```javascript
// refactoring the above code with inheritance and super

// creating a new class with commonInfo() method
class Vehicle {
  commonInfo() {
    console.log("I am a Vehicle");
  }
}

class Car extends Vehicle {
  constructor(_name) {
    // _name can be replaced with any variable name, but be sure to use the same throughout the program
    // super() has to be called  before accessing this keyword
    super();
    this.name = _name;
  }
  getInfo() {
    super.commonInfo()
    console.log(this.name + " is a good car");
  }
}
var bmw = new Car("BMW M3"); // we pass the name as an argument to the instance
bmw.getInfo();
```
