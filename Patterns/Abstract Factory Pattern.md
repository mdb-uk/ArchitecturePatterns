
[[Architecture Patterns Index]] #SoftwareEngineering #Creational
# Abstract Factory Pattern

This is a Creational software design pattern that lets you create families of related objects without specifying their concrete class.

As per the below images, your abstract factory churns out groups of 'furniture' objects, but when you instantiate the factory you can choose which style of objects you would like, therefore it remains flexible on the detailed implementation.

The concrete factory still returns an abstract type in their signature, so that client code does not get tightly coupled, but they will actually return the specific style of objects that they have been created to handle.

![[Pasted image 20241004084605.png]]

![[Pasted image 20241004084638.png]]

### References

[Abstract Factory](https://refactoring.guru/design-patterns/abstract-factory)

[Abstract Factory Pattern - GeeksforGeeks](https://www.geeksforgeeks.org/abstract-factory-pattern/)

