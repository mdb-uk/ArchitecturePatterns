[[Architecture Patterns Index]] #ApplicationArchitecture #Decoupling
# Service oriented architecture

This pattern allows services to communicate over a network. AKA [[SOA]].

Some characteristics of the service oriented pattern:

- Modular - Software is broken down into discrete services that perform specific functions
- Loosely coupled
- Interoperability - Services use standard protocols and interfaces (i.e. SOAP or REST) so that they can work together regardless of the technologies they each use
- Reusable - services are designed to be reusable across different applications and business processes
- Service contract - each service has a contract that defines how it can be used, the I/O and constraints etc.
- Service registry - a central service is often used to register services for discoverability and to promote reuse

SOA can be particularly useful for integrating legacy systems and for environments that require high agility.

![[Pasted image 20241028115035.png]]

References

[What is Service-Oriented Architecture (SOA)? | IBM](https://www.ibm.com/topics/soa)
[Service-oriented architecture - Wikipedia](https://en.wikipedia.org/wiki/Service-oriented_architecture)