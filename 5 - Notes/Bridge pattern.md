15:19 | 2024-10-31
# Links

[[Software design patterns Master Index]]
# Content

This pattern uses composition instead of inheritance to allow the implementation of a class to vary from the abstraction of it.

This example shows the problem in a simple way if you try and use inheritance: ![[Pasted image 20241031152659.png]]

If you added more combinations of shapes and colours, the number of subclasses would grow exponentially.

Rather than this you can compose out the Colour and have the Shape interface reference it (i.e. use Composition). This link is the Bridge:
![[Pasted image 20241031152801.png]]

The Shape class then gets a reference field pointing at one of the Colour objects. 

Here is a more real world example:
![[Pasted image 20241031153240.png]]

Structure
- Abstraction - defined the abstract interface and maintains a reference to an object of type `Implementor` 
- Refined Abstraction - Extends the `Abstration` class and implements additional functionality
- Implementor - An interface that defines methods to be implemented
- ConcreteImplementor - Implements the `Implementor` interface and provides concrete functionality


References
[Bridge](https://refactoring.guru/design-patterns/bridge)