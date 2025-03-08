# Links

[[Architecture]] [[Architecture Patterns Master Index]]
# Content


This pattern divides the system into two main parts; the client and the server.

The client is the device or application which initiates the request for a service or resource. Typically this would be some form of user facing application like a web browser or mobile app.

The server provides the services or resources requested by clients and handle complex processing and large scale data storage.

This pattern uses the request-response model, where the client makes a request to the server which processes the request and then returns a response. This communication often uses HTTPS for web based services or SQL for database queries for example.

Resources are centralised on the server which simplifies maintenance, updates and security management.

This pattern is easily scalable as more servers can be added.

A disadvantage of this pattern is the cost to buy and maintain sufficient servers to handle all requests.

![[Pasted image 20240912144734.png]]

### References

[5 essential patterns of software architecture | Enable Architect (redhat.com)](https://www.redhat.com/architect/5-essential-patterns-software-architecture)

[Client-Server Architecture - System Design - GeeksforGeeks](https://www.geeksforgeeks.org/client-server-architecture-system-design/)