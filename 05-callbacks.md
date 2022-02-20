# Javascript Callbacks

Callbacks in Javascript are special functions that are passed into another function as an argument and then called in the same parent function to complete some routine code. Callbacks are executed along with the parent functions. Callbacks are anonymous functions i.e. neither they have a name nor they are stored in any variable.

```javascript
// example of callback and parent function
// let us write a parent function foo() which will take 2 arguments, one being a number and the other one will be another function which will act upon the previous argument
function foo(number, fn) {
    fn(number)
}
// by definition of callbacks, fn is being called insie the parent function
// callback function will be written at the time of calling the parent function
foo(2, function(e){
    console.log(2 + e)
})
// here in foo() we have written fn(number) which means our callback needs an argument, hence we passed e
// when foo() is run, the callback will also run resulting in the addition of 2 and e, which will be 4
```
