[[Architecture Patterns Index]] #ErrorHandling
# Retry Pattern

The Retry pattern enables an application to handle transient failures by transparently retrying a failed operation.

Faults can include temporary loss of network connectivity, a service being temporarily unavailable, or timeouts that can occur when a service is too busy.

These faults are usually transient, and in the cloud particularly they should be expected. The applications should be built to handle these problems elegantly and transparently to minimize the effects upon the business tasks the app is performing. 

Example of a retry mechanism: 
![[Pasted image 20250124143848.png]]

Many services and applications, specifically SaaS and PaaS for example, already have retry features built in that you can configure.

There are various retry strategies:

- Cancel - if the fault indicates it is not transient or there is another reason to expect it's unlikely to be solved soon the operation can be cancelled
- Retry immediately - If the specific fault reported is unusual or rare, like a network packet becoming corrupted while it was being transmitted, the best course of action may be to immediately retry the request.
- Retry after delay - some times you might want to leave a period for a fault, such as a rate limit being hit, to settle down.
- Incremental/Exponential backoff - with this pattern the wait between retries gets larger and larger until it eventually cancels
- Dynamic retry - you can alter the retry time based on the type of exception

Considerations

- Performance - using retry policies can have an impact on App performance
- API load - multiple retry requests can cause further load on an API
- Idempotency - if a request is inherently idempotent it's safe to retry, but if not you need to deal with this in some way because if you retry blindly it could get executed more than once.

### References

[Retry pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/retry)
[Retry with backoff pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/retry-backoff.html)