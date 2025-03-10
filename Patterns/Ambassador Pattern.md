[[Architecture Patterns Index]]
# Ambassador Pattern

"The main purpose of the Ambassador Pattern is to reduce the complexity of communication between microservices."

This pattern is used in Microservice architecture to handle tasks such as logging, monitoring, routing, security and resiliency.

Key aspects:

- Proxy service - this is known as the Ambassador which acts as an out of process proxy, co-located with the client service and handles network requests on it's behalf
- Offloading - the ambassador service offloads common connectivity tasks from the client service such as monitoring, logging, routing, security (i.e. TLS) and implementing resiliency patterns
- Language agnostic - the ambassador service is designed to be language agnostic
- Enhanced security and resiliency - by centralising these tasks in the ambassador service it's easier manage and update security features (auth, encryption etc) and implement resiliency features (retries, circuit breakers etc)
- Use cases - Ambassador pattern is particularly useful for legacy applications that are hard to modify as it lets them get modern supporting features without changing their code. Also beneficial in environments where multiple services need to share common service features.
- Deployment - The Ambassador service can be deployed in a sidecar container in a K8S environment or as a separate process on the same host as the client service.

Some disadvantages:
- Added complexity
- Performance overhead
- Additional management
- Potential single point of failure


![[Pasted image 20241028121301.png]]
![[Pasted image 20241028121603.png]]
![[Pasted image 20241028121628.png]]
### References

[Design Patterns for Microservices - DZone](https://dzone.com/articles/design-patterns-for-microservices-ambassador-anti)
[Ambassador pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/ambassador)