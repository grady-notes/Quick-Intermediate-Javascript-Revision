# Javascript Promises

Promises in Javascript are a way to make asynchronous code easier to understand, read and write. They are just like promises in real life. In-short if I tell you that I am going to teach you Javascript and if I succeed in doing so, then the promise is resolved. Otherwise the promise is rejected.

Promises in Javascript can be initiated using the `new` keyword. and be stored in a variable. The created promise instance takes a callback. This callback takes two parameters `resolve` and `reject`. These 2 are keywords and have to be written as they are and cannot be replaced by any other words. Inside the promise instance the `resolve()` and `reject()` have to be called in order to implement them.

```javascript
var promise = new Promise(function(resolve, reject){
    var name = "Aatif"
    if (name == "Aatif") {
        resolve("Promise Success")
    } else {
        reject("Promise Failed")
    }
})
```

# Chaining , .then() and .catch()

In the above code we created a promise, and now to execute the promise we have to take promise variable and start chaining it using the `.then()` and `.catch()` methods. `.then()` is executed when the promise is resolved and success message is returned, similarly `.catch()` is executed when the promise is rejected and an error message is returned.

```javascript
// refactoring the above code with .then() and .catch()
var promise = new Promise(function(resolve, reject){
    var name = "Aatif"
    if (name == "Aatif") {
        resolve("Promise Success")
    } else {
        reject("Promise Failed")
    }
})

// each of then and catch take one callback and one parameter which is returned in the previous call of resolve() and reject() in the promise instance
promise.then(function(result){
    console.log(result)
}).catch(function (error){
    console.log(error)
})
```


