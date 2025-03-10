# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content


The publish-subscribe architecture is a messaging pattern used to enable async, scalable and decoupled communication between difference components or services.

Publishers produce and send messages, categorizing them into different classes or topics.

Subscribers are the entities that receive the messages, expressing interesting in one or more topics/classes and only receive the messages that match the ones they have subscribed to.

Message brokers are intermediaries that are sometimes used in this pattern (i.e. event or service bus) that manage the distribution, filtering and routing of messages from publishers to subscribers.

It can use topic based filtering or content based filtering.

It is commonly used in event driven systems, microservices and real-time applications.

Examples:

- Google Cloud Pub/Sub
- Azure Service Bus
- Apache Kafka

![[Pasted image 20240910115017.png]]
![[Pasted image 20240910115031.png]]


References

[What is Pub/Sub Architecture? - GeeksforGeeks](https://www.geeksforgeeks.org/what-is-pub-sub/)
[Architectural overview of Pub/Sub  |  Pub/Sub Documentation  |  Google Cloud](https://cloud.google.com/pubsub/architecture)
[What is Pub/Sub? The Publish/Subscribe model explained (ably.com)](https://ably.com/topic/pub-sub)
[The pros and cons of the Pub-Sub architecture pattern | Enable Architect (redhat.com)](https://www.redhat.com/architect/pub-sub-pros-and-cons)