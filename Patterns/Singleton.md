07:55 | 2024-10-25
# Links

[[Software design patterns Master Index]]
# Content

Creational design pattern that lets you enforce a single instance of a class while providing a global access point to this instance.

This is a better approach than things like Global variables because those could get overwritten etc, race conditions could occur etc.

The inherent traits of a singleton are:

- Private default constructor, to prevent other objects from using `new` on the singleton class.
- A Static creation method that acts as a constructor - under the hood this calls the private constructor if the class has not already been instantiated but otherwise returns the existing instance


![[Pasted image 20241025080054.png]]

Benefits:
- You can be sure the class only has 1 instance
- Global access point to that instance
- The singleton is initialised

Disadvantages
- Violates Single responsibility, the singleton performs two functions
- Can mask bad design
- Requires special treatment in multithreaded environments so different threads don't create different singletons
- Hard to test as you cannot mock the Singleton normally