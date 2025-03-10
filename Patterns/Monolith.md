07:50 | 2024-09-30
# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

Traditional design pattern where all the components of an application are integrated into a single, unified system. This includes all layers of the app (UI, business logic, data access etc) are developed, deployed and maintained as one indivisible unit. Typically would also use a single database for all data storage needs.

Advantages:
- Simple (particularly for smaller apps)
- Performance - can be more efficient because of tight coupling
- Initial set up very easy, can get going quickly
- Debugging can be easier (especially when the monolith is smaller - this becomes less true as it grows)

Disadvantages
- Difficult to scale especially as it grows
- Can be difficult to maintain when it becomes bigger
- Deployment - any change, even a minor one, requires the redeployment of the entire app
- Resistance to new technologies - it is hard to update any component because it affects the whole monolith

Monolithic architecture is often compared to microservices architecture as they are almost contrasting opposites.

![[Pasted image 20240930075551.png]]

### References

[Monolithic Architecture - System Design - GeeksforGeeks](https://www.geeksforgeeks.org/monolithic-architecture-system-design/)
[What is Monolithic Architecture? | IBM](https://www.ibm.com/think/topics/monolithic-architecture)