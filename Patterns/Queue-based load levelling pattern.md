12:08 | 2025-01-14
# Links

[[Architecture Patterns Index]]
# Content

This pattern uses a queue as a buffer between the client and the service it invokes. This smooths intermittent heavy loads. This can prevent the service being overwhelmed by the intermittent spikes.

![[Pasted image 20250114121103.png]]

### Benefits

- Maximise resilience, scalability & availability
- Controls costs - service instances only have to scale to deal with average load rather than the peaks

### Considerations

- Application logic to control the flow of data and smooth spikes is required
- Message queues are one-way, so you might need to implement a system that provides a response from the service back to the client
- The lag in dealing with messages - in busy periods this can keep getting larger and larger
- Be careful if you apply autoscaling to services that are listening for requests on the queue. This can result in increased contention for any resources that these services share and diminish the effectiveness of using the queue to level the load.
- Resilience of the queue - it can lose information if this is not high enough

### When to use

This pattern is useful to any application that uses services that are subject to overloading.

This pattern isn't useful if the application expects a response from the service with minimal latency.

### References

https://learn.microsoft.com/en-us/azure/architecture/patterns/queue-based-load-leveling