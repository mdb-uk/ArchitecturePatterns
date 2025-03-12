[[Architecture Patterns Index]] #Decoupling #Polyglot
# Hexagonal Architecture

This pattern, also known as the ports and adapters pattern, aims to create loosely coupled architectures where app components can be tested individually, with no dependencies on data stores or user interfaces.

The pattern helps prevent technology lock in of data stores and UIs, making it easier to evolve the technology stack over time.

The application communicates in this loosely coupled architecture over interfaces called ports, and uses adapters to translate the technical exchanges between components. 

Ports are technology-agnostic entry points into an application component.

Adapters interact with the application through a port by using a specific technology. Adapters plug into these ports, receive data from or provide data to the ports, and transform the data for further processing. For example, a REST adapter enables actors to communicate with the application component through a REST API.

The purpose of the pattern is to isolate business logic from the related code (such as for accessing a persistence component) to avoid tight coupling of business logic to specific technologies.

Useful when:
- You want a decoupled architecture where each component can be fully and individually tested
- Multiple types of clients can use the same domain logic
- You want to be able to switch out technology for layers like UI and persistence without affecting app logic
- Your app requires multiple input providers and output consumers, and customizing the application logic leads to code complexity and lack of extensibility.

Considerations:
- Works well in a DDD (Domain Driven Design) approach.
- Can be complex and harder to troubleshoot if not planned carefully
- Additional maintenance overhead
- Communication between components does introduce some latency

![[Pasted image 20250130100559.png]]
![[Pasted image 20250130100607.png]]
### References

[Hexagonal architecture pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/hexagonal-architecture.html)