13:38 | 2025-01-29
# Links

[[Architecture Patterns Master Index]]
# Content

This pattern allows you to deploy the components of an application into a separate container or process in order to provide encapsulation and isolation.

The sidecar will share the same lifecycle as the parent application and provides supporting features.

This pattern is *decomposition* pattern. It is sometimes also known as the "sidekick" pattern.

Services such as logging, config, network services might be decomposed into a Sidecar container. 

When you decompose an app into seperate services the isolation means that if there is a problem in one of the sub services it does not necessarily cause the main app to be affected (depending on how critical the service is and how good the error handling is)

Also decomposing to services also means that the various services decomposed can all be different languages and frameworks if desired.

However, separate services can add complexity, latency etc. The sidecar pattern helps mitigate these issues because the sidecar is co-located with the application. Because they are in the same container/process you can provide a single homogenous interface for applications.

The sidecar pattern does introduce some latency in communication between the app and sidecar, so might not be appropriate if the communication is particularly chatty or is required to be low latency.

![[Pasted image 20250129135502.png]]
### References

[Sidecar pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/sidecar)
