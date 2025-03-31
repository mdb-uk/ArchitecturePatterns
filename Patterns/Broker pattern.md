[[Architecture Patterns Index]] #Routing #Communication
# Broker pattern

This pattern is used in distributed software systems to identify and route traffic to an appropriate server.

## Broker Pattern Roles

- Client: access server’s functionality by sending requests to the broker.
- Server: it make their services available on the broker.
- Broker: find the appropriate server, forward the request and transmit result to client.

![[Pasted image 20240729100242.png]]

## Message Queue vs. Message Broker

A message queue is a form of describing a data structure to hold messages for eventual consumption. Where a message broker is a separate component that manages queues.

In simple words a message queue is a queue like data structure first-in-first-out (FIFO). A message broker is more like service bus; an object that is used to route traffic while allowing to decouple the system into smaller parts.

![[Pasted image 20240729100231.png]]

### References

[Broker Pattern | GeeksforGeeks](https://www.geeksforgeeks.org/broker-pattern/)