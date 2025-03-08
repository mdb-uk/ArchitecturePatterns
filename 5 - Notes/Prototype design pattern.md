10:10 | 2024-10-23
# Links

[[Software design patterns Master Index]]
# Content

**Prototype** is a creational design pattern that lets you copy existing objects without making your code dependent on their classes.

Copying an object traditionally would involve firstly creating a new instantiation of the same class, then copying the values of the properties over. The catch is that some properties might be private, so you would lose these values. Furthermore with this approach you need to reference the specific class in your code which makes it tightly coupled and brittle. There is also a case where you may only know the Interface that has been implemented, not the concrete class.

The prototype pattern solves these issues by delegating the cloning process to the actual object being cloned. The pattern declares a common interface, usually just with a single "clone" method, so you don't have to tightly couple your code to a concrete class in order to clone an instance of that class.

![[Pasted image 20241023102337.png]]

![[Pasted image 20241023102349.png]]


References

[Prototype](https://refactoring.guru/design-patterns/prototype)
