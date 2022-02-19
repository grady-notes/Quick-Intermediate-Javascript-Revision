# Javascript Functions

Just like any other programming language, functions are the primary building blocks of any code in Javascript too. Functions add more meaning to the systematic flow of the program. In simple words, functions take some input and return an appropriate output  where there is some obvious relationship between the input and output.

Functions can be declared in 2 ways, one being the most commonly used `function` keyword and the other is setting up a reference to a variable, however both of them can be invoked / called using a common method i.e. directly making a call to the function.

```javascript
// example of function keyword
function foo() {
    console.log("I am FOO")
}

// example of reference function
var bar = function() {
    console.log("I am BAR")
}

// calling both the functions is done in the same way
foo()
bar()
```

Passing parameters / arguments to the functions can increase the range of the functions and make them more dynamic and easier to interact with.

```javascript
// example of parameter / argument
function greet(name) {
    console.log("Hello, " + name + ". Welcome to Functions")
}
// calling the above created function by passing an actual name as the parameter
greet("Aatif") //whatever passed here instead of Aatif will appear in output
```

In the previous examples we were directly printing out the values of the outputs of the functions. Generally functions have to be more dynamic and preserve the state of the function into a seperate place. We will use the `return` keyword for that purpose. The `return` keyword stores the exact output of the function which can be used later.

```javascript
// example of return keyword in a complete program
function add (a, b) {
    return a + b
}
var sum = add(2,3) // storing the result in the variable sum
console.log("Addition is : " + sum)
```

In the previous example, the function requires two arguments `a` and `b`, that is why we passed in `2` and `3` as the two mandatory arguments. But what if we skip any any of the argument and just pass in `2` or just `3`. Yes, it will break the entire program. We can avoid that by using default values, so even if we skip any one of the argument, it will be replaced with its default value.

```javascript
// example of default values
function add (a = 0, b = 0) { 
    // we simply assign values at declaration
    // default values can be anything but 0 is preferred in case of numerical programs
    return a + b
}
var sum = add(2) // notice that I have skipped an value
console.log("Addition is : " + sum)
// expected output will be 
// Addition is : 2
// hence program will not break
```
