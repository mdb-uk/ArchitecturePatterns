[[Architecture Patterns Index]] #Antipattern

#Antipattern 
# Distributed Monolith

This is effectively an Architectural anti-pattern which you want to avoid. This sometimes arises from making a pre-mature jump to Microservices. It isn't always without fail a bad thing, and sometimes it may work, but it's not a state to aim for.

![[Pasted image 20250312092741.png]]

Effectively a Distributed Monolith involves components that are separated out (i.e. separate deployments etc) but are still very tightly coupled to each other. Changes to one components will have knock on effects on others, and complexity increases across the board with additional features and logic being added.

![[Pasted image 20250312092900.png]]

Often you end up with a Distributed Monolith by accident, by attempting to implement [[Microservices]] but not properly separating concerns and logic.

Indications that you have a Distributed Monolith:

- A small change to application logic requires concurrent changes to many applications
- Multiple services and components access the same database
- The number of parameters passed to multiple microservices grows continuously over time
- Multiple microservices and components share common boilerplate code
- Services retain increasing amounts of logic with each successive change to a system

If you have a Distributed monolith you can either continue with or, or design a proper Microservice architecture from scratch. 

### References

https://www.techtarget.com/searchapparchitecture/tip/The-distributed-monolith-What-it-is-and-how-to-escape-it

https://www.linkedin.com/pulse/distributed-monoliths-recognizing-addressing-luis-soares-m-sc-/

https://dev.to/morintd/understand-the-difference-between-monolith-microservices-and-distributed-monolith-39kb