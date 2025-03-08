11:19 | 2024-12-03
# Links

[[Software design patterns Master Index]]
# Content

This is a behavioural design pattern that provides a way to access the elements of a collection sequentially without giving access to the actual collection object.

This allows clients to traverse items in the collection in a standard way without having to know any details of the collections specific implementation.

Components:
- Iterator - interface or abstract class that defines the methods for accessing/traversing elements such as next() or hasNext()
- Concrete Iterator - class that implements the iterator
- Aggregate - interface or abstract class that defined a method for creating an iterator
- Concrete Aggregate - class that implements the Aggregate and returns an instance of the Concrete Iterator

Benefits
- Decouples the traversal algorithm from the collection allowing multiple combinations or algorithms and collections
- Flexible - new traversal operations can be added without modifying the collections interface

![[Pasted image 20241203112856.png]]

### References

[Iterator](https://refactoring.guru/design-patterns/iterator)