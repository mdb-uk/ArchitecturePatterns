[[Architecture Patterns Index]] #Reuse #Decoupling
# Gateway Offloading Pattern

This pattern involved offloading shared or specialised service functionality to a centralised gateway proxy.

This pattern simplifies application development by moving common functionalities, such as SSL termination, authentication, and monitoring, from individual services to a centralized gateway.

Key benefits
- Simplified development - managing access to the centralised resources is easier
- Specialised teams can handle the special centralised resources
- Consistency - logging and monitoring etc is unified in the central service for consistency
- Scalability and management is simpler when it's a single centra service

Common use cases
- SSL Termination - Managing SSL certificates centrally to avoid the complexity of distributing them across services
- Auth
- Monitoring and logging

 Considerations
 - Availability - the Gateway is a single point of failure so proper consideration must be given to it's resilience and availability, scaling requirements etc
 - Only offload features that are used widely and are generic, not business logic+

![[Pasted image 20241128103418.png]]

![[Pasted image 20241128103414.png]]

### References

[Gateway Offloading pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-offloading)
[API gateways - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/microservices/design/gateway)