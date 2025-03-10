# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

Used particularly in microservices to manage distributed transactions and ensure data consistency across multiple services.

- Each service involved in the saga performs a local transaction. These transactions are independent and update the service's internal database
- A central orchestrator (aka saga orchestrator) coordinates the sequence of transactions, sending commands to each service to perform their local transactions and waiting for a response before moving onto the next step
- If a transaction fails, the orchestrator triggers compensating transactions to undo the changes made by previous transactions, ensuring the system returns to a consistent state


![[Pasted image 20240820160316.png]]

There are two approaches to the Saga pattern, Choreography and Orchestration.

### Orchestration

In the Orchestration pattern, **a single orchestrator is responsible for managing the overall transaction status.**

If any of the microservices encounter a failure, the orchestrator is responsible for invoking the necessary compensating transactions:

![[Pasted image 20240820160622.png]]

The Saga orchestration pattern is **useful for brownfield microservice application development architecture.** In other words, this pattern works when we already have a set of microservices and would like to implement the Saga pattern in the application. We need to define the appropriate compensating transactions to proceed with this pattern.
### Choreography

In the Saga Choreography pattern, **each microservice that is part of the transaction publishes an event that is processed by the next microservice.**

In this pattern, the Saga Execution Coordinator is either embedded within the microservice or can be a standalone component.

![[Pasted image 20240820160535.png]]

### 2PC (Two Phase Commit)

This is a precursor to the Saga Orchestration pattern

![[Pasted image 20240820160040.png]]
Drawbacks:

- Coordinator is Single Point of Failure
- All the services are slowed to the speed of the slowest service
- 2PC (two phase commit) protocol is chatty and slow by nature
- 2PC not supported by NoSQL databases

### References

[Saga Pattern in Microservices | Baeldung on Computer Science](https://www.baeldung.com/cs/saga-pattern-microservices)

[Saga pattern - Azure Design Patterns | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga)

[Saga choreography pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/saga-choreography.html)

[Saga orchestration pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/saga-orchestration.html)
