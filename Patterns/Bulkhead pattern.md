[[Architecture Patterns Index]] #Resilience
# Bulkhead pattern

This pattern is intended to improve the resilience and reliability of an application by isolating components or services into different units, or 'bulkheads'. The name comes from the isolated compartments in a Ship's hull designed to stop it from sinking.

Key features
- Isolation of failures - problems in one bulkhead do not affect the others, by design
- Resource allocation - resources such as threads, memory or connections are allocated to each bulkhead so they can operate independently and that a failure or overload in one bulkhead cannot affect the others
- Improved resilience - the nature of the pattern means that even if one bulkhead fails the system should be able to keep operating normally
- Granularity - the level of isolation can vary, it can be at the service, within a service, or even at request level

Use cases
- HA - high availability systems can benefit from this pattern because of the resilience it provides
- Preventing cascading failures
- Resource management
- Isolate critical consumers from standard consumers

This diagram shows a bulkhead pattern organised around connection pools: ![[Pasted image 20241031142353.png]]

This diagram shows a bulkhead pattern organised around service instances: ![[Pasted image 20241031142437.png]]

Challenges

- Complexity can be introduced with this pattern
- Resource management, whilst being more fine grained, can be more difficult
- Latency
- Synchronisation and consistency

### References

https://learn.microsoft.com/en-us/azure/architecture/patterns/bulkhead
[Bulkhead Pattern - GeeksforGeeks](https://www.geeksforgeeks.org/bulkhead-pattern/)