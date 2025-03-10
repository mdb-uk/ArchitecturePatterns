# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content


Space-based architecture (SBA) is a software design approach that organizes the system around the concept of "spaces", which are essentially isolated and autonomous units of functionality. Each space has its own data, logic, and interface, and they communicate with each other through message passing.

![[Pasted image 20240808133311.png]]

The big advantage of this is that it promotes high degrees of isolation and autonomy, making it easier to test, deploy and evolve the system. It also handles complex business logic more easily, and finally easy handling of scalability and performance (because each space is independent and can be scaled independently).

The big disadvantage of this architecture is the complexity it introduces, and communication between the independent spaces can be challenging. It can also be tricky to avoid coupling between the spaces.

![[Pasted image 20240808133828.png]]

References
[Software Architecture Patterns: Space-based Architecture - DEV Community](https://dev.to/alexr/software-architecture-patterns-space-based-architecture-h2i)

[Space-Based Architecture Style - Mastering Software Architecture (romerogabriel.github.io)](https://romerogabriel.github.io/mastering-software-architecture/arch_styles/space_based_arch/)