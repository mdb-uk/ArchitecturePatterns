[[Architecture Patterns Index]] #SoftwareEngineering #Creational
# Object pool pattern

This is a creational design patter that managed a pool of reusable objects to minimize the overhead of creating and destroying objects.

It maintains a collection of initialised objects and provides mechanisms for clients to efficiently borrow and return objects from the pool.

Clients effectively "borrow" objects from the pool temporarily.

- ****Stage 1: Creation****: Objects are initially created and added to the pool.
- ****Stage 2: Borrowing****: Clients request and borrow objects from the pool.
- ****Stage 3: Usage****: Clients use the borrowed objects for their tasks.
- ****Stage 4: Returning****: After usage, clients return the objects to the pool for reuse.
- ****Stage 5: Rejection or Destruction****: If the pool is full or objects are not used, they may be rejected or removed from the pool.
![[Pasted image 20241028132938.png]]

### References

[Object Pool Design Pattern - GeeksforGeeks](https://www.geeksforgeeks.org/object-pool-design-pattern/)