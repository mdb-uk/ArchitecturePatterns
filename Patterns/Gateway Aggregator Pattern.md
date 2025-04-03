[[Architecture Patterns Index]] #Routing
# Gateway Aggregator Pattern

### Overview

This pattern is used to optimise communications between clients and backend services.

### How it works

- Client request - client sends single request to the gateway
- Gateway processing - the gateway decomposes the request into multiple requests to various backend services
- Backend services - all receive and process their individual requests from the gateway and return a response to the gateway when ready
- Aggregation - the gateway compiles the responses into a single response
- Client response - once all the responses from backend services are received the gateway sends a single response to the client

### Benefits

- Less network chatter
- Improved performance (less overhead from network requests)
- Simplified client side logic, only have to manage 1 request

### Considerations

- Single point of failure (gateway)
- Latency - gateway should be located close to the backend services
- Scalability - the gateway must be scalable to prevent bottlenecks

This pattern can be particularly useful in MSA (Micro service architecture).

Without gateway aggregation:
![[Pasted image 20241121142653.png]]

With Gateway Aggregation:
![[Pasted image 20241121142729.png]]
### References

[Gateway Aggregation pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-aggregation)