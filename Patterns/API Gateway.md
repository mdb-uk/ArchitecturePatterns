[[Architecture Patterns Index]] #API
# API Gateway

This pattern involves a service that acts as a reverse proxy between clients and services behind the gateway.

The gateway will do things like rate limiting, routing, auth etc to take the responsibility away from the backend services.

![[Pasted image 20250211161441.png]]

Steps of an API gateway:

- Routing
- Protocol translation
- Request aggregation
- Auth
- Rate limiting/throttling
- Load balancing
- Caching
- Monitoring and logging

The API gateway pattern works differently in a monolithic architecture to how it does in a microservices architecture:

- Routing - internal parts of the monolith application / various microservices
- Service discovery - not a concern as all part of the same app / a mechanism will be needed to discover microservices
- Auth - In both architectures the API gateway would handle auth but microservices might have more complex requirements as each microservice would authorise requests
- Load balancing - Same as auth
- Fault tolerance and logging - Same as auth, microservices have more critical needs for good fault handling and logging

API Gateway with microservices:![[Pasted image 20250211161941.png]]

### References

https://www.geeksforgeeks.org/what-is-api-gateway-system-design/
https://cloud.google.com/api-gateway/docs/architecture-overview