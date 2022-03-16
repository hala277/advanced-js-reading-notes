# Socket.io

## Review, Research, and Discussion

+ What is the benefit of transforming data into packets?

*Packet-based networks not only enable new innovations, services, and business opportunities, they are also the most cost-effective, efficient, and scalable networks for content delivery.*

+ UDP is often refereed to as a connectionless protocol. Why is this?

*UDP is a protocol that does not require a connection. It's called a datagram protocol since it's similar to sending a letter and not acknowledging receipt.*

+ Can a socket server application have multiple socket connections?

*Multiple connections on the same server can share the same server-side IP/Port pair as long as the client-side IP/Port pairs are different, and the server can handle as many clients as available system resources allow.*

+ Can a socket connection application be connected to multiple socket servers?

*You can't connect to several servers with a single socket. For each connection, you'll need to make a new socket.*

+ Can an application be both a socket server and a socket connection?

*As long as your protocol allows it, you can utilize the same socket for whatever you want.*


## Term

+ Observer Pattern: 
*The observer pattern is a software design pattern in which a subject object keeps track of its dependents, called observers, and notifies them of any state changes automatically, usually by calling one of their methods.*

+ Listener: 
*represents a handler for an event emitted by an EventTarget object.*

+ Event Handler: 
*is an asynchronous callback routine that runs after an event occurs.*

+ Event Driven Programming: 
*is utilized to make the program as easy as feasible by synchronizing the occurrence of various events.*

+ Event Loop: 
*The event loop is a programming component or design pattern in which a program waits for and dispatches events or messages.*

+ Event Queue:
*is a storage location for events from an application before they are processed by a receiving program or system.*

+ Call Stack:
*A call stack is a mechanism that allows an interpreter (such as the JavaScript interpreter in a web browser) to keep track of its position in a script that calls multiple functions, such as which function is currently being executed and which functions are called from within that function, and so on.*

+ Emit:
*(On the other hand, the publish method allows you to "emit" an event, causing any callbacks associated with the event to 'fire') (get called).*

+ Raise:
*raise an error,The throw statement throws a user-defined exception.*

+ Trigger:
*For the selected items, the trigger() method activates the provided event and the default behavior of an event (such as form submission).*

+ Subscribe:
*The.subscribe() function is similar to jQuery's Promise.then(),.catch(), and.finally() methods, but it works with Observables instead of promises.*

+ database:
*a structured collection of information or data that is usually saved electronically in a computer system.*

## OSI Model Explained 

*The Open Systems Interconnection Model (OSI Model) is a theoretical framework for describing the functions of a networking system. In order to facilitate interoperability between diverse devices and applications, the OSI model describes computing functions into a universal set of rules and standards.*

* ### In a computer network, how is data moved from one machine to another?

*In its most basic form, a network is formed by two computers (end-points) connected by LAN Cable (Network Media) and connectors (RJ45) and sharing data via NICs.*

* ### If one computer runs Microsoft Windows and the other runs Mac OS, how will these two machines communicate with one another?

*The International Organization for Standardization established the 7-layered OSI Model or Open System Interconnection Model in 1984 in order to achieve successful communication across computers or networks of various architectures.*

### The 7-layered OSI Model

1. Application Layer
2. Presentation Layer
3. Session Layer
4. Transport layer
5. Network Layer
6. Data Link Layer
7. Physical Layer

## TCP - Three-way handshake
*TCP stands for transmission control protocol. TCP is a reliable and connection-oriented transport protocol. With TCP, data can be delivered successfully and accurately. Many applications, such as web,  email, and FTP, use TCP.*

**the three steps for three-way handshak:**

* *Step 1: The client sends a SYN segment  to the server, asking for connection.* 

* *Step 2: The server replies with SYN-ACK. SYN-ACK means synchronization and acknowledgement. The server acknowledges the client's connection request. It also asks the client to open a connection too.* 


* *Step 3: The client replies with ACK, which is like"Yes"* 

* *Then the two-way connection is established between them.*

![the three steps for three-way handshak](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-a-tcp-3-way-handshake-process-three-way-handshaking-establishing-connection-6a724e77ba96e241.jpg)

## Socket.io

### What Socket.IO is?

*Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.It is built on top of the WebSocket protocol and provides additional guarantees like fallback to HTTP long-polling or automatic reconnection.*

## Socket.io Server API
![Server API](https://socket.io/images/server-class-diagram-server.png)

## Resources
+ [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)
+ [TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)
+ [Socket.io Documentation](https://socket.io/docs/)
+ [Socket.io Server API](https://socket.io/docs/server-api)
+ [Socket.io Client API](https://socket.io/docs/client-api)
+ [Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)