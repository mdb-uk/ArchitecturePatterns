14:29 | 2024-11-14
# Links

[[Architecture Patterns Index]]
# Content

This pattern involves creating multiple independent copies of your application, which are individually referred to as "stamps" or "scale units".  Each stamp operates independently and can serve a customer subset.

Benefits
- Scalable - you can scale horizontally by adding and removing stamps
- Isolation - helps in containment of failures
- Flexibility - stamps can be deployed in different geographical regions to meet data security requirements or reduce latency for users
- Customisable - different stamps can be configured or updated independently 

Use cases
- Multi-tenant SaaS applications - different stamps can be set up to handle different groups of customers
- HA and DR - stamps can be deployed in different regions to help with these
- Performance optimisation - load can be distributed across multiple stamps to improve performance

Considerations
- Traffic Routing - Proper DNS configuration is required to properly route traffic around to the stamps properly

![[Pasted image 20241114144204.png]]


### References

[Deployment Stamps pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/deployment-stamp)

[Architecting multitenant solutions on Azure - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/overview)
[Deployment Stamps Pattern - System Design - GeeksforGeeks](https://www.geeksforgeeks.org/deployment-stamps-pattern-system-design/)