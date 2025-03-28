[[Architecture Patterns Index]] #Decoupling #Composition #Microservices
# BFF (Backends For Frontends)


The Backend for Frontend (BFF) is a software architecture pattern that involves creating a separate backend service for each frontend client. Here are some key points about the BFF pattern:

- **Data Transformation Layer**: BFF creates a data transformation layer between a client and the API to prevent over-fetching and under-fetching data. This helps eliminate the Chatty I/O development anti-pattern
- **Decoupling**: BFF is a microservice architecture pattern that provides an extra layer between your backend services and the interfaces that access them. It’s a variation of the API gateway pattern.
- **Optimization**: Each backend is specific to one interface, it can be optimized for that interface. As a result, it will be smaller, less complex, and likely faster than a generic backend that tries to satisfy the requirements for all interfaces.
- **Autonomy**: Each interface team has autonomy to control their own backend and doesn’t rely on a centralized backend development team. This gives the interface team flexibility in language selection, release cadence, prioritization of workload, and feature integration in their backend.
- **Customized APIs**: BFF tailors APIs for different clients or user interfaces, such as web, mobile, or other platforms. Instead of having a single API for all clients, BFFs provide customized APIs that cater to the unique needs and requirements of each client, ensuring efficient communication and an optimized user experience.

In summary, the BFF pattern is a design pattern that helps to streamline data representation and takes up the responsibility of providing a well-focused interface for the frontend.

This is the classic approach where you have a single API that services all of the requests:

![[Pasted image 20240902142358.png]]

And in the BFF approach you have a BFF per front end:

![[Pasted image 20240902142507.png]]

A Microservices design:
![[Pasted image 20240902142423.png]]
### References

https://learn.microsoft.com/en-us/azure/architecture/patterns/backends-for-frontends

[The BFF Pattern (Backend for Frontend): An Introduction | Bits and Pieces](https://blog.bitsrc.io/bff-pattern-backend-for-frontend-an-introduction-e4fa965128bf)

[Introduction - BFF Patterns](https://bff-patterns.com/)