# Message Queues

What does it mean that web sockets are bidirectional? Why is this useful?
> They can send and recieve data without waiting around for responses. This way data can flow back and forth and eventually queue for a waiting server.

Does socket.io use HTTP? Why?
> First connection is established with HTTP

What happens when a client emits an event?
> The server recieves and handles it.

What happens when a server emits an event?
> It's heard

What happens if a client “misses” an event? How can we mitigate this?
> Listeners should stay on.


Socket - server endpoint with port numbers.
Web Socket - client socket
Socket.io - third party JS library allows data flow between server and client
Client - origin web browser where req are sent from to server
Server - program receives sends and connects to the client
OSI Model - Open System Interconnection Model
TCP Model - bit more concise than OSI
TCP - Transmission Control Protocol
UDP - User Datagram Protocol sends data packets over network
Packets - small bits of data sent over UDP


Which 3 things had you heard about previously and now have better clarity on?
> Sockets, NameSpaces

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
> 

What are you most excited about trying to implement or see how it works?

Preparation Materials
Socket.io Chat Example
Rooms and Namespaces
Socket.io Emit Cheatsheet