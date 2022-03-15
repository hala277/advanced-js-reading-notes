# Event Driven Applications

## Review, Research, and Discussion

* Why is access control important?

*Access control is a crucial part of data security since it determines who has access to and uses company data and resources. Access control policies ensure that users are who they say they are and have proper access to company data through authentication and permission.*

* Describe an application that would need access control.

*we can use it at Role-Based Access Control, designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees' positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.*

* What is a role used for?

*the role determines which permissions the system grants to the user. For example, you can designate whether a user is an administrator, a specialist, or an end-user, and limit access to specific resources or tasks.*

* Why is role based access control more scalable than discretionary or mandatory access control?

*that because RBAC (role-based access control) is a way of restricting network access based on individual users' positions within an organization. The most stringent level of control is Mandatory Access Control (MAC). Furthermore, while Discretionary Access Control provides a more flexible environment than Mandatory Access Control, it also increases the danger of data being made accessible to people who should not have access.*

## Terms

* Authorization: the process of confirming which apps, files, and data a user has access to.

* Role Based Access Control: role-based access control (RBAC) or role-based security is an approach to restricting system access to authorized users.

* Capabilities: the access rights that are given to a role of a user.

## Event Driven Programming in Node.js

**Event Driven Programming:** 
*Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.*

**The most recognizable example of Event-Driven Programming is The Web Browser.**

*farther more An event occurs every time you interact with a webpage through its user interface. A click event is triggered when you click a button. A keydown event is initiated when you press a key. These events have related routines that are executed when they are triggered to alter the user interface in some way.*

**The following notions are used in event-driven programming:**

1. When an event is triggered, an Event Handler is a callback function that is called.
2. A Main Loop is a program that listens for event triggers and then calls the event handler for that event.

![event-driven programming](https://media.geeksforgeeks.org/wp-content/uploads/20211017211104/EDP1drawio.png)

**EventEmitter:** 
*The EventEmitter is a Node module that allows objects to communicate. EventEmitter is at the heart of Node's asynchronous event-driven design. EventEmitter is the ancestor of several of Node's built-in modules.*

### **emitter object has two key characteristics:**

* Emitting name events:
*Emitting an event is the notification that something has happened. This circumstance is frequently caused by a status change in the broadcasting object.*

* Registering and unregistering listener functions:
*The binding and unbinding of callback functions with their respective events is referred to as this.*

### Event-Driven Programming Principles:

+ A suite of functions for handling the events.
+ Binding registered functions to events.
+ When a registered event is received, an event loop polls for new events and calls the matching event handler(s).

### resources: 
+ [Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)
+ [Explain Event-Driven Programming in Node.js](https://www.geeksforgeeks.org/explain-event-driven-programming-in-node-js/#:~:text=Event%2Ddriven%20programming%20is%20used,when%20an%20event%20is%20triggered.)
+ [Node.js v17.7.1 documentation](https://nodejs.org/api/events.html)




