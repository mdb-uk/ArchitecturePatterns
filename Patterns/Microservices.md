# Links

[[Architecture]] [[Architecture Patterns Index]] [[Microservices (tag)|Microservices (tag)]]
# Content

This pattern is an approach where an application is structured as a collection of small autonomous services. Each of these is self-contained and focuses on specific business capability within a bounded context.

Key Characteristics:

- Loosely coupled - services are independent so can be updated and scaled independently
- Autonomous - independent development, deployment and scaling
- Business-oriented - organised around business capabilities, not technical layers
- Resilient - one service failing doesn't necessarily affect others
- Decentralised Governance - freedom to choose the best tools and technologies for each service

Some common design patterns using the Microservices approach:

- API Gateway - single entry point for all client requests, routing them to appropriate microservices
- Service Discovery - helps services find each other dynamically often involving a service registry
- Circuit Breaker - prevents cascading failures by stopping calls to a failing service
- Bulkhead - Isolates resources to prevent a failure in one service from affecting others
- Event sourcing - Captures changes to data as a sequence of events ensuring consistency

Challenges

- Complexity - lots of services to manage can be complex, requiring robust monitoring and orchestration
- Data management - ensuring data consistency across services and be tricky
- Network latency - this must be considered as microservice architectures are inherently chatty across the network

![[Pasted image 20240821154401.png]]
![[Pasted image 20240821154440.png]]

References

[Design a microservices architecture - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/microservices/design/)
[Microservice Architecture and Design Patterns - DZone](https://dzone.com/articles/design-patterns-for-microservices)