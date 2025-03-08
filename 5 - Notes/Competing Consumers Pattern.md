11:34 | 2024-11-11
# Links

[[Architecture Patterns Master Index]]
# Content

This pattern is designed to handle high volumes of requests by distributing them across multiple concurrent (identical) consumers to optimise throughput, improve scalability and availability and balance the workload.

Key concepts:

- Message queue - The app sends requests as messages to the queue
- Multiple consumers - Several consumer instances read and process these messages from the queue
- Load balancing - The system ensures that each message is only processed by one consumer

Benefits
- Scalable
- Reliable & Resilient
- Decoupled (Producers and Consumers operate independently)

Considerations
- Message ordering - order of processing is not guaranteed so you must design your applications with this in mind
- Idempotency - It's important to ensure that Consumers process messages in an idempotent way
- Poison message detection - implement mechanisms to detect and handle malformed messages

![[Pasted image 20241111115317.png]]
### References

[Competing Consumers pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/competing-consumers)