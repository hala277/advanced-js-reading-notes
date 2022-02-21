# Read02

## Middleware
1. Name 3 real world use cases where you’d want to change the request with custom middleware?
* Auth middleware
* Logging Middleware 
* validateCookies 

2. True or false: The route handler is middleware?
*false*

3. In what ways can a middleware function end the process and send data to the browser? *next(), responce.end, response.send*

4. At what point in the request lifecycle can you “inject” middleware?

5. What can cause express to error with “Request headers sent twice, cannot start a second response”
 
 *This issue occurs when we send the user or client several answers. That means the receiver is receiving two responses when only one should be sent.*

 ## Vocabulary
 * **Middleware:** *Middleware is software that extends the operating system's capabilities and provides common services and capabilities to applications.*

* **Request Object:** *is the primary point of entry for an application to send a request to the Library; all operations on a URL must use a Request object.*

* **Response Object:** *its When an HTTP request is received, the response object represents the HTTP response that an Express app provides.*

* **Application Middleware:** *software that sits between an operating system and the applications*

* **Routing Middleware:** *express.Router()*

* **Test Driven Development** *TDD is a software development approach in which test cases are created to specify and validate what the code will accomplish.*

* **Behavioral Testing** *Behavioral testing, often known as black-box testing, examines the program's exterior behavior.*


## Review: ES6 Classes
*Classes serve as a starting point for the creation of things. They wrap data with code that allows them to work with it. Classes in JS are prototype-based, but they also include some syntax and semantics that are not shared with ES5 class-like semantics.we can say that class are special functions*

**class syntax components:**
1. class expressions.

*class expressions can be named or unnamed like `let Name = class`*
2. class declarations. 

*to declare a class we can use the keyword class with the name of the class like `class Name`*

**The difference between function and class declarations is that functions can be called in code that appears before they are defined, whereas classes must be defined before they can be formed.**

## Using Express Routing

* what is Routing? 

*The process by which an application's endpoints (URIs) react to client requests is referred to as routing. For a basic understanding of routing*

* how did we define routing?

*using methods of Express app object which it is correspond to HTTP methods like app.get, app.post or app.all so we can handle all HTTP methods, also we can use app.use to specify middleware as callback function*

*routing method can have more than one callback function as arguments, so when we have more than one callback function It is critical to pass next as an argument to the callback function and then call next() within the function body to pass control to the next callback.*

* what is Route methods?

*A route method is derived from one of the HTTP methods and is connected to an express class instance.*

* what is Route paths?

*The endpoints at which requests can be made are defined by route pathways in conjunction with a request method. Strings, string patterns, and regular expressions can all be used as route pathways.*

* what is Route handlers?

*To manage a request, you can supply numerous callback functions that act as middleware. The sole exception is that these callbacks may use next('route') to skip the remaining route callbacks. This technique can be used to place preconditions on a route, then pass control to succeeding routes if there is no reason to continue with the present route.*


## Writing middleware for use in Express apps

*Middleware functions have access to the request object (req), the response object (res), and the next function in the request-response cycle of the application.and The next function is an Express router function that, when called, executes the middleware that comes after the current middleware.*

**we can perform middleware function in this following tasks:**

1. Run whatever code you want.
2. Make modifications to the request and response objects.
3. Put an end to the request-response loop.
4. Call the next middleware in the stack.

## How Node JS middleware Works?

1. As the name implies, it appears in the middle of something, namely the request and response cycle.

2. The request and response objects are accessible to middleware.

3. The middleware has access to the following function in the request-response life cycle.

![how middleware work](https://miro.medium.com/max/1400/1*wIkLR_9twvmG-LitHYoftw.png)

![next and middleware](https://miro.medium.com/max/1400/1*ptNjzuT0m2BQ9YpQTVwVLg.png)

### Types of express middleware:
1. Application level middleware `app.use`.
2. Router level middleware `router.use`.
3. Built-in middleware `express.static,express.json,express.urlencoded`.
4. Error handling middleware `app.use(err,req,res,next)`.
5. Thirdparty middleware `bodyparser,cookieparser`.

## Express Routing

*The new Router is included with Express 4.0. Router functions similarly to a mini-Express application. It does not provide any views or settings, but it does have routing APIs such as.use,.get,.param, and route.It is a small express application that lacks all of the bells and whistles of an express application, only the routing functionality.*

-------------

### resources:
* [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
* [Writing middleware for use in Express apps](https://expressjs.com/en/guide/writing-middleware.html)
* [How Node JS middleware Works?](https://selvaganesh93.medium.com/how-node-js-middleware-works-d8e02a936113)
* [Using Express Routing](https://expressjs.com/en/guide/routing.html)
* [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)









