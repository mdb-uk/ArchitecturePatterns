[[Architecture Patterns Index]]
# Throttling Pattern

This pattern involves controlling the rate at which a resource can be consumed, such as responses via an API.

This avoids the system being overwhelmed by requests from single users and spreads the load over time.

This is an alternative to autoscaling the application (which allows the potential spike but would cost you more).

You should define SLAs (Service level agreements) so that people are aware of rate limits, and use appropriate HTTP response codes such as 429 too many requests or 503 server too busy

![[Pasted image 20250123144431.png]]

This image shows how throttling can be combined with autoscaling:
![[Pasted image 20250123144513.png]]


Considerations:
- Should be considered and planned early in the design of an application because it's harder to add later
- The process of throttling and then de-throttling afterwards must be done quickly
- The retry-after header can be used to help mitigate issues related to throttling

--- 
Also known as rate limiting, the throttling pattern is used to control the rate at which data flows into a target service or process.

This can be for reasons such as ensuring system stability at various loads, DDOS protection etc. It can also assist with cost management.

If not implemented correctly it can degrade system performance. Implementation can be complex so requires the necessary expertise.

"The throttling pattern is difficult to do as a one-off solution implemented in isolation. Often the Throttling architectural pattern is used in conjunction with the [Circuit Breaker pattern](https://redhat.com/architect/circuit-breaker-architecture-pattern) in order to maintain service availability. For example, when a target reaches a threshold that requires throttling, a circuit breaker is used to reroute traffic to another target that has identical functionality, thus reducing the load on the first target. Typically implementing this type of throttling behaviour requires infrastructure management technologies such as [Kubernetes Horizontal Pod Autoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/) or a service mesh solution such as [Istio](https://istio.io/) or [Linkerd](https://linkerd.io/2.10/overview/)."

![[Pasted image 20240807155454.png]]
### References

[Throttling pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/throttling)
[The pros and cons of the Throttling architecture pattern | Enable Architect (redhat.com)](https://www.redhat.com/architect/pros-and-cons-throttling)
