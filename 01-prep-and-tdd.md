# Read01

## 1. Event Loop 

*JavaScript is an asynchronous, single-threaded programming language. It indicates that the main thread, where JavaScript code is executed, executes one line at a time, with no option of parallel execution. The event loop is the trick that allows JavaScript to appear to be multithreaded even if it is really single-threaded.*

### How its work?

*When the SetTimeOut function is invoked and the Web API makes the indicated wait, the callback function in the event queue has not yet run and is waiting for its time into the stack.That's where the event loop comes in; it takes the first event from the Event Queue and adds it to the stack, in this case, the callback function.This function then calls any other functions contained within it.This cycle is known as the event loop, and it is how JavaScript handles events.*

## 2. JS callback functions

### What is a Callback Function?

*A callback function is a function that is passed as a parameter to another function.*

### Why do we need Callback Functions?

*JavaScript executes code in top-down order. But, there are some circumstances where code is executed (or must be executed) after something else has occurred, and not sequentially. This is referred to as asynchronous programming. Callbacks ensure that a function does not run before a task is completed, but only after the task has been performed. It aids in the development of asynchronous JavaScript code and protects us from issues and errors. In JavaScript, a callback function is created by passing it as a parameter to another function and then calling it back immediately after something happens or a task is done.*

### ways to  create a Callback
1. Callback function
 ```js
const message = function () {
  console.log("This message is shown after 3 seconds");
};

setTimeout(message, 3000); 
```
2. Using anonymous function its a function without a name in js
```js
setTimeout(function () {
  console.log("This message is shown after 5 seconds");
}, 5000);

```
3. callback as an arrow function
```js
setTimeout(() => {
  console.log("This message is shown after 6 seconds");
}, 6000);

```

## 3. JS Promises

*In JavaScript, promises are used to handle asynchronous operations. They are simple to manage when dealing with several asynchronous activities when callbacks might lead to unmanageable code.*

*we did use promises to improve code readability, asynchronous operation handling, flow of control definition in asynchronous logic, and error management.*

#### **A Promise exists in four states:**
1. **fulfilled:** The promise-related action was successful.
2. **rejected:** The promise-related action failed.
3. **pending:** The promise is still pending, it has not yet been fulfilled or rejected.
4. **settled:** The promise has been fulfilled or rejected

`The Promise constructor can be used to create a promise.`

**Syntax:**
```
var promise = new Promise(function(resolve, reject){
     //do something
});

```
**Parameters**

* The promise constructor only accepts one argument, which is a callback function (and that callback function is also referred as an anonymous function too).

* The resolve and refuse arguments are passed to the callback function.

* Execute activities within the callback function, and if all goes well, call resolve.

* If the desired procedures fail, call reject.

**Promise Consumers:** 

1. `then():` When a promise is resolved or refused, then() is called. It can alternatively be defined as a career that takes data from a promise and successfully executes it.
2. `catch():` catch() is called when a promise is denied or an error occurs during execution. It is used as an Error Handler if an error is possible at any phase.

## 4. JS Async/Await

**Async:**
*It essentially enables us to write promise-based code as if it were synchronous, while also ensuring that the execution thread is not broken. It can work asynchronously thanks to the event loop. Async functions always return a value. It ensures that a promise is returned, and if it isn't, javascript wraps it in a promise that is resolved with the value of the promise.*

**Await:**
*To wait for the promise, use the await function. It could only be used within the async block. It instructs the code to wait until the promise returns a response. It just delays the async block.*

## 5. Test-Driven Development

**first what is testing?**

*Testing is the process of ensuring that a program receives the correct input and produces the desired output and side effects. Specifications are used to define these right inputs, outputs, and side effects. You may have come across testing files with the `filename.spec.js` naming pattern. The spec is an abbreviation for standard. It is the file in which we declare or assert what our code should do and then test it to ensure that it does so.*

**When it comes to testing, we have two options:** 
1. **manual testing:** *Manual testing is the practice of checking your application or code from the standpoint of the user. Navigating around the browser or application in an attempt to test the functioning and uncover bugs.* 
2. **automated testing:** *automated-testing entails writing code that tests to see if other code works. Unlike manual testing, the specifications are consistent from test to test. The most significant advantage is the ability to test numerous things much more quickly.*

### Test-Driven Development
*Test-driven development is the process of identifying what you want your software to accomplish (the specifications), creating a failed test, and then building the code to pass that test. It is most commonly used in automated testing. Although the principles might be used for manual testing as well.*

**to do Project setup:**
1. Create an NPM project: `npm init`
2. Create `id.js` and add it to the project’s root.
3. Install Jest: `npm install jest --D`
4. Update the `package.json` test script

*to run our test script we did use: `npm run test`.*

### **How Do We Write a Test?**
*Tests are just functions that take a few arguments. We can use either `it()` or `test()` to run our test.*


```
`describe()` allows us to divide up our tests into sections
```

### Testing Based on Specifications
*While it may be tempting to simply sit down and start entering application logic, a well-planned approach will make development easier. We must define what our program will accomplish. Specifications are used to outline these objectives.*

