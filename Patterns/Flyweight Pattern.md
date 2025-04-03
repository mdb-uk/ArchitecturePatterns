[[Architecture Patterns Index]] #SoftwareEngineering #Behavioural
# Flyweight Pattern

This is a structural design pattern that lets you save memory by keeping certain parts of the state shared between objects.

Systems that are spawning lots of objects which each have copies of the same data can run into memory issues.

This pattern removes the state that is not entirely controlled by the individual objects and externalises it into the flywheel so all objects can share it.

In this example, certain properties of a Tree object are extracted into the TreeType object so they can just exist once rather than being replicated many times:
![[Pasted image 20250403140510.png]]
### References

[Flyweight](https://refactoring.guru/design-patterns/flyweight)
