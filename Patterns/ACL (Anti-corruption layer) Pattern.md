[[Architecture Patterns Index]] #Cybersecurity
# ACL (Anti-corruption layer) Pattern


This pattern managed interactions between subsystems, especially when integrating modern applications with legacy systems or external services.

The ACL acts as a mediator or translator between the involved systems that may have different data models, protocols or semantics. It ensures that the core system remains unaffected by complexities or inconsistencies of the other system(s).

The ACL isolates the core system by sitting between it and all other systems and all communications pass through the ACL. It converts communications into a format the core system can understand and vice versa.

The ACL can be implemented as a [[Façade Pattern]] or [[Adapter Pattern]] layer.

This pattern is useful in legacy integrations, when two systems need to communicate but have different data models or communication types, or to assist a gradual migration.

Benefits include maintaining integrity of the core system, reducing potential technical debt and flexibility.

Some considerations include the additional latency that the the ACL can introduce, operational overhead of the extra complexity and scalability of the ACL.

![[Pasted image 20241029151006.png]]

### References

[Anti-corruption Layer pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/anti-corruption-layer)
[Anti-corruption layer pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/acl.html)