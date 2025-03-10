# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

[Choreography pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/choreography)

"Have each component of the system participate in the decision-making process about the workflow of a business transaction, instead of relying on a central point of control."

Usually related to microservices, the choreography pattern (along with the related orchestrator pattern) are ways of handling communication in a microservices architecture.

The orchestrator pattern has tight coupling to the orchestrator, whereas the choreography pattern has point to point communication between microservices.

One way to implement choreography is the async message pattern:

![[Pasted image 20240307161600.png]]

Here a publish/subscribe model is used so any service interested in a specific type of message can receive it.

Another example:

![[Pasted image 20240307161852.png]]

Here instead of the messages being centrally orchestrated, each component decides how to deal with it and passes it to the next microservice in the chain: Ingestion > Packing > Scheduling > Delivery.