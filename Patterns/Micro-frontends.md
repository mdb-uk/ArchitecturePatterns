[[Architecture Patterns Index]] #Microservices #Decoupling #Decentralisation 

# Micro-frontends

Sometimes also called microsites, this pattern extends the [[Microservices]] pattern to include the frontend, so each microservice has it's own frontend.

This approach allows teams to work independently on different services without having to touch the other aspects of the larger system. 

![[Pasted image 20250415114741.png]]

Deployments are independent:

![[Pasted image 20250415114911.png]]

When allocating teams for this style of work, avoid "horizontal" teams who are responsible for a specific aspect across multiple micro-frontends:

![[Pasted image 20250415114957.png]]

### References

[A Comprehensive Guide to Micro Frontend Architecture | by Vivek Shukla | Appfoster | Medium](https://medium.com/appfoster/a-comprehensive-guide-to-micro-frontend-architecture-cc0e31e0c053)

[Micro Frontends](https://martinfowler.com/articles/micro-frontends.html)

[What are Micro Frontends? | GeeksforGeeks](https://www.geeksforgeeks.org/what-are-micro-frontends/)