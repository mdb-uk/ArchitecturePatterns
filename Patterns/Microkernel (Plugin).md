12:05 | 2024-09-27
# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

This pattern separates the core functionality of a system from it's extended functionalities. 

Key points:

- Minimal core - the microkernel itself contains only the essential functionalities to make the system operational
- Plug-in modules - additional features and functionality are implemented as plug-in modules that interact with the core system

Advantages:
- Extensible
- Flexible
- Isolation
Disadvtantages:
- Complexity of management & coordination
- Performance Overhead

Common use cases for this pattern are IDEs and Web browsers.

![[Pasted image 20240927121020.png]]
### References

[4. Microkernel Architecture - Software Architecture Patterns, 2nd Edition [Book] (oreilly.com)](https://www.oreilly.com/library/view/software-architecture-patterns/9781098134280/ch04.html)