15:01 | 2024-11-14
# Links

[[Software design patterns Master Index]]
# Content

This is a structural design pattern that lets you save memory by keeping certain parts of the state shared between objects.

Systems that are spawning lots of objects which each have copies of the same data can run into memory issues.

This pattern removes the state that is not entirely controlled by the individual objects and externalises it into the flywheel so all objects can share it.



[Flyweight](https://refactoring.guru/design-patterns/flyweight)
