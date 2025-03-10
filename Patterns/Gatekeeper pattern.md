14:07 | 2024-11-20
# Links

[[Architecture Patterns Master Index]]
# Content

### Overview

This pattern enhances security of apps and services by using a dedicated host instance to broker requests between clients and the app/service.

### Key aspects

- It acts as a security layer that validates and sanitises incoming requests
- It isolates internal logic, thereby limiting the potential exposure of sensitive data and credentials

### How it works

1. Request handling - the Gatekeeper receives the request and performs additional validation and sanitisation
2. Broker - it then forwards the request to the trusted app/service to perform the actual processing
3. Limited privileges - because it only has very limited privileges it limits the exposure if it is compromised

### Considerations

- Performance impact - additional processing and network comms
- Single point of failure - redundancy and resilience of the gatekeeper must be considered

### Use cases

- Apps handling sensitive information
- Services requiring high levels of protections from malicious attacks
- Mission-critical operations that cannot be disrupted
- Cloud environments
- Interaction with the [[Valet Key]] pattern

![[Pasted image 20241120141310.png]]

### References

[Gatekeeper pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/gatekeeper)

[Cloud design patterns that support security - Microsoft Azure Well-Architected Framework | Microsoft Learn](https://learn.microsoft.com/en-us/azure/well-architected/security/design-patterns)