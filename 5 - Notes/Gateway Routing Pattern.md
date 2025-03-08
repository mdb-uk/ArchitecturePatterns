10:46 | 2024-11-28
# Links

[[Architecture Patterns Master Index]]
# Content

This pattern allows you to handle requests via a Gateway and then route it to one of many possible options based on the request itself.

Particularly useful in microservices architectures where clients need to interact with multiple services.

Key Characteristics

- Single endpoint for clients to interact with
- Layer 7 routing - based on URL paths, headers or other HTTP attributes
- Load balancing - distributes requests across multiple backend services
- Versioning - supports multiple versions of a service, useful for canaries or blue/green deployments
- Reduced attack surface means improved security
- Centralised management

Considerations
- Single point of failure
- Performance

![[Pasted image 20241128151316.png]]

![[Pasted image 20241128151324.png]]
![[Pasted image 20241128151333.png]]
### References

[Gateway Routing pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-routing)