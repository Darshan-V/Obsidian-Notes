There are several ways to get real time data from the backend,

- **Server sent events (SSE)** - usually web page has to request to the server to receive new data; that is, the client makes the request for data to the server. With SSE it is possible for the server to send new data to the client without a client request any time, by pushing a message to the client page, these incoming message can be treated as events + data inside the client's web page.
- **WebSockets** - Web sockets are defined as a two-way communication between the servers and the clients, which mean both the parties, communicate and exchange data at the same time. This protocol defines a full duplex communication from the ground up. Web sockets take a step forward in bringing desktop rich functionalities to the web browsers.
- **Long Polling**
- **Short Polling**
