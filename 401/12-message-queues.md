# Message Queues

## Links

[Socket.io Chat Example](https://socket.io/get-started/chat/)
[Rooms and Namespaces](https://socket.io/docs/v3/rooms/index.html)
[Socket.io Emit Cheatsheet](https://socket.io/docs/v3/emit-cheatsheet/index.html)

**What does it mean that web sockets are bidirectional? Why is this useful?** 

WebSocket allows a single TCP socket connection to be hijacked so that the client-server relationship can relay bi-directional, full-duplex (or sometimes also referred to as double-duplex) messages instantaneously. [instantaneous communication](https://medium.com/@nerdplusdog/websocket-simultaneous-bi-directional-client-server-communication-e7948203054b)

**Does socket.io use HTTP? Why?**

[integrates with (or mounts on) the Node.JS HTTP Server socket.io](https://socket.io/get-started/chat/)

**What happens when a client emits an event?**

the server listens for it and runs functions based on what's attached to the listener

**What happens when a server emits an event?**

The event is sent to everyone

**What happens if a client “misses” an event?**

it gets ignored

**How can we mitigate this?**

attach functions/methods to each listener

## Vocabulary

- [Socket](https://en.wikipedia.org/wiki/Network_socket) - a software structure within a network node of a computer network that serves as an endpoint for sending and receiving data across the network.


- [Web Socket](https://medium.com/@nerdplusdog/websocket-simultaneous-bi-directional-client-server-communication-e7948203054b) - allows a single TCP socket connection to be hijacked so that the client-server relationship can relay bi-directional, full-duplex (or sometimes also referred to as double-duplex) messages instantaneously.


- [Socket.io](https://en.wikipedia.org/wiki/Socket.IO) - enables realtime, bi-directional communication between web clients and servers


- [Client](https://en.wikipedia.org/wiki/Client_(computing)) - computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks


- [Server](https://en.wikipedia.org/wiki/Server_(computing)) - a piece of computer hardware or software (computer program) that provides functionality for other programs or devices, called "clients".


- [OSI Model](https://en.wikipedia.org/wiki/OSI_model) - goal is the interoperability (the ability of computer systems or software to exchange and make use of information) of diverse communication systems with standard communication protocols


- [TCP Model](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) -  provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network.


- [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) - Transmission Control Protocol


- [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) - User Datagram Protocol - With UDP, computer applications can send messages, in this case referred to as datagrams, to other hosts on an Internet Protocol (IP) network


- [Packets](https://www.google.com/search?q=Packets&rlz=1C1CHBF_enUS911US911&oq=Packets&aqs=chrome..69i57j69i60l3.424j0j4&sourceid=chrome&ie=UTF-8) - A packet is a small amount of data sent over a network

