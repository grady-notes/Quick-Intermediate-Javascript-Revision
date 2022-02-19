# Javascript Objects

A set of named values is known as an object in Javascript. In simple words, an object is a set key and value pair that holds a valid data type. Objects are immutable data types.

```javascript
// example of object
var person = {
    name: "Aatif",
    age: 19
}

// accessing the values of the object "person"
// 1- dot notation (mostly used)
console.log(person.name, person.age)

// 2 - call by key
console.log(person["name"], person["age"])
```

Javascript supports nesting objects

```javascript
// nested object
// person object contains one more object in it named "name" 
var person = {
    name: {
        firstName: "Aatif",
        lastName: "Mastan"
    }
}


// accessing nested values by dot notation
console.log(person.name.firstName, person.name.lastName)
```

A more traditional way of creating an object in Javascript is using the `new` keyword

```javascript
var person = new Object();

// values can be assigned to this newly created object using the assignment operator
person.name = "Aatif"
person.age = 19

// logging this "person" will print out the entire object
console.log(person) 
```
