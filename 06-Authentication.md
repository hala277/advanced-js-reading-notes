# Authentication

1. Explain what a “Singleton” is (in Computer Science terms)
*A singleton is a class that permits only one instance of itself to be produced and provides access to that instance after it has been constructed. It has static variables that can hold one-of-a-kind and private instances of itself. It is used when a user wants to limit the instantiation of a class to only one object. This is frequently useful when a single entity must coordinate actions throughout a system.*

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes.

*When we want to ensure that just one object is instantiated, we use singleton. As a result, rather than generating a new object, we must verify that the constructor is invoked only once and then reuse the instance.*

**We may accomplish this by modifying our class to include:**

1. hidden (private)constructor
2. a public getInstance function that returns a class instance

## Terms

**Router Middleware**

*In the application's request-response cycle, middleware functions have access to the request object (req), the response object (res), and the next middleware function. We frequently define endpoints in Express that use HTTP verbs to represent GET, POST, DELETE, and PUT requests. A router manages these incoming requests.* 

**Dynamic Module Loading**

*Dynamic loading is a method for a computer program to load a library (or other binary) into memory at runtime, retrieve the addresses of the library's functions and variables, execute those functions or access those variables, and then unload the library from memory.*

**Singleton Pattern**

*The singleton pattern is a software design pattern that limits the number of instances of a class to one. This is beneficial when only one item is required to coordinate system-wide actions.*

**CRUD -> REST Method Matches:** 

1. PUT = Create and Update
2. Post = Create 
3. GET = Read 
4. Delete = Deletes.

**Mock Testing**

*Mocking is the process of constructing a mock version of an external or internal service that can replace the actual one, allowing your tests to run faster and more consistently.*

## Securing Passwords 

*Algorithms for cryptographic hashing MD5, SHA1, SHA256, SHA512, and SHA-3 are all general-purpose hash functions that are used to produce a digest of large amounts of data in the shortest amount of time possible. Hashing is the best approach to safeguard passwords and is believed to be quite safe for ensuring data or password integrity. Cyber crooks use passwords as their first line of protection. It's the most important aspect of everything we do on the internet. The advantage of hashing is that if a database containing hashed passwords is stolen, only the hashes are stolen, not the plaintext passwords.*

**CRYPTOGRAPHIC HASH ALGORITHM PROBLEMS:**
1. Brute Force Assault: Because hashes cannot be reversed, instead of reversing the password hash, an attacker can just keep trying different inputs until he finds one that yields the identical hash value, which is known as a brute force attack.
2. Hash Collision Attack: Because hash functions have a limitless input length and a predefined output length, it's inevitable that two separate inputs will give the same hash output. Hash Collision Attack is a vulnerability in MD5, SHA1, and SHA2. two hash function input strings that return the same hash result.

## Basic Auth 

*Basic access authentication is a technique for an HTTP user agent to submit a user name and password when making a request in the context of an HTTP transaction. A request including basic HTTP authentication includes a header field in the form of Authorization: Basic `<credentials>`, where credentials is the Base64 encoding of the ID and password linked by a single colon`:`.*

## OWASP auth cheatsheet 

*Authentication: is the process of confirming that a person, entity, or website is who they say they are. In the context of web applications, authentication is generally accomplished by submitting a username or ID, as well as one or more pieces of secret information that should only be known by a specific user.*

*Session Management is the technique through which a server keeps track of the status of a client. This allows a server to remember how to respond to subsequent requests throughout a transaction. A session identifier is kept on the server and can be transferred back and forth between the client and the server while sending and receiving requests. Sessions should be one-of-a-kind for each user and computationally challenging to forecast. More information on recommended practices in this area can be found in the Session Management Cheat Sheet.*

[for Authentication General Guidelines](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

## bcrypt docs 

*its A library to help you hash passwords.*

*to Install this library use: `npm install bcrypt`*

**To hash a password:**

```js

bcrypt.genSalt(saltRounds, function(err, salt) {
    bcrypt.hash(myPlaintextPassword, salt, function(err, hash) {
        // Store hash in your password DB.
    });
});

```

**To check a password:**

```js

// Load hash from your password DB.
bcrypt.compare(myPlaintextPassword, hash, function(err, result) {
    // result == true
});
bcrypt.compare(someOtherPlaintextPassword, hash, function(err, result) {
    // result == false
});

```

### for more resource: 
- [Node.JS and Singleton Pattern](https://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)
- [What is Router Middleware in express](https://stackoverflow.com/questions/63106648/what-is-router-middleware-in-express#:~:text=The%20term%20is%20composed%20of,or%20call%20the%20next%20middleware.)
- [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
- [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
- [OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)
- [bcrypt docs](https://www.npmjs.com/package/bcrypt)