14:49 | 2025-01-30
# Links

[[Architecture Patterns Index]]
# Content

This pattern is like a halfway house between a [[Monolith]] and [[Microservices]] architectures. You still have one application deployed as a whole at an infrastructure level, but within the app it's broken down into loosely coupled and independent code modules;

![[Pasted image 20250130145049.png]]

![[Pasted image 20250130145156.png]]

Each module can follow their own architectural style and logical separations, for instance in the above screenshot, modules are all following the layered (or [[Layered (n-tier)]] architecture, but they do not all have to be following the same pattern.

Challenges
- Complexity - more than monolith but potentially less than microservices
- Dependency management
- Deployment complexity
- Testing overhead

### References

[Microservices Killer: Modular Monolithic Architecture | by Mehmet Ozkaya | Design Microservices Architecture with Patterns & Principles | Medium](https://medium.com/design-microservices-architecture-with-patterns/microservices-killer-modular-monolithic-architecture-ac83814f6862)

[What Is a Modular Monolith? - GeeksforGeeks](https://www.geeksforgeeks.org/what-is-a-modular-monolith/)