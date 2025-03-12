[[Architecture Patterns Index]] #SoftwareEngineering
# Onion Architecture

The Onion Architecture is a way of architecting an application from a code perspective.

Rather than the traditional layered approach:

![[Pasted image 20241128152737.png]]

You use the Onion approach:
![[Pasted image 20241128152750.png]]

Dependencies are inverted (the IoC principle), meaning the core of the app does not depend on layers above it.

In this approach the domain model is the core of your app, and it is wrapped in a domain service layer, which in turn is wrapped in app service layer and finally the outer layer is the UI layer, handling Tests and external connections.

Beyond those relationships between a layer and it's direct neighbours (i.e. the layer above and beneath it) there are no links between other layers, meaning they have no knowledge of each other.

Benefits
- Testability
- Loose coupling
- Maintainable

Considerations
- Complexity - more difficult to understand and implement correctly for beginners
- Overhead for simple apps

![[Pasted image 20241128153301.png]]
### References

[The Onion Architecture : part 1 | Programming with Palermo](https://jeffreypalermo.com/2008/07/the-onion-architecture-part-1/)
[Onion Architecture: Definition, Principles & Benefits | CodeGuru](https://www.codeguru.com/csharp/understanding-onion-architecture/)
[Onion Architecture in ASP.NET Core - Code Maze](https://code-maze.com/onion-architecture-in-aspnetcore/)