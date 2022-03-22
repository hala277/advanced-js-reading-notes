# Message Queues

## Review, Research, and Discussion

+ What does it mean that web sockets are bidirectional? Why is this useful?

*BIDIRECTIONAL. Whereas HTTP relies on a client request to receive a response from the server for every exchange, WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.*

+ Does socket.io use HTTP? Why?

*is established with a WebSocket connection whenever possible, and will use HTTP long-polling as fallback.*

+ What happens when a client emits an event?

*When our server emits events which match the first ‘event’ argument the callback will be run. Inside these callbacks we can take the actions we want on the client-side.*

+ What happens when a server emits an event?

*When the server emits an event, the data delivered by the server is received by the client listening on the other end with the same.on method.*

## Term

+ Socket:  *is one endpoint of a two-way communication link between two programs running on the network.*
+ Web Socket: *The WebSocket API is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server.*
+ Socket.io: *Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.It is built on top of the WebSocket protocol and provides additional guarantees like fallback to HTTP long-polling or automatic reconnection.*
+ client: *The clients connect to the server, exchange information, and then disconnect* 
+ Server: *a server runs on a specific computer and has a socket that is bound to a specific port number.*
+ OSI Model: *is a theoretical framework for describing the functions of a networking system.*
+ TCP Model: *It stands for Transmission Control Protocol/Internet Protocol. The TCP/IP model is a concise version of the OSI model.*
+ TCP: *Transmission Control Protocol (TCP) is a standard that defines how to establish and maintain a network conversation by which applications can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other.*
+ UDP: *User Datagram Protocol (UDP) is a communications protocol that is primarily used to establish low-latency and loss-tolerating connections between applications on the internet. UDP speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.*
+ Packets: *a packet is a small segment of a larger message. Data sent over computer networks such as the Internet, is divided into packets. These packets are then recombined by the computer or device that receives them.*