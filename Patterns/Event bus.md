 [[Architecture Patterns Index]] #EventDriven #Communication
# Event bus


This pattern is closely related to the [[Pub-Sub]] pattern. It's a specialisation of that pattern where you have an orchestrator (the eponymous Event Bus) that distributes messages from publishers to subscribers so that the publishers and subscribers do not have to be aware of each other.

![[Pasted image 20240918120032.png]]

"For the "publisher/subscriber" pattern, subscriber components have to subscribe (or unsubscribe) to an event publisher. This means the life time of the event publishers is as least as long or longer than any of its subscribers. There are lots of simple scenarios where this is sufficient.

However, when you have a system where you have certain event publishers for a certain _type_ of event, and you may also have subscribers for this _type_ of event, and the life times of publishers and subscribers is completely independent from each other, you need a middle-man component to manage this. That middle-man is called an **event-bus**."

"One important aspect of publish/subscribe is that _all potential subscribers need to know and locate all potential publishers_, whereas in a bus setup everyone only needs to know the bus and the respective topic. This is significantly less complex (or: pushes the complexity into the bus implementation that you can purchase as middleware)."


References

[Implementing event-based communication between microservices (integration events) - .NET | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/integration-event-based-microservice-communications#the-event-bus)

[Event-Driven Architecture and Pub/Sub Pattern Explained (altexsoft.com)](https://www.altexsoft.com/blog/event-driven-architecture-pub-sub/)

[message queue - Event bus vs PubSub - Software Engineering Stack Exchange](https://softwareengineering.stackexchange.com/questions/437732/event-bus-vs-pubsub)