15:57 | 2024-10-30
# Links

[[Architecture Patterns Index]]
# Content

Used often in cloud and distributed systems, this pattern is a communication strategy which allows a client to send a request to a service without waiting for an immediate response. The client carries on with other tasks and the server sends a response in due course.

Key Features:

- Decoupled request and response processes, enhancing efficiency and scalability
- HTTP Polling is often used to implement this pattern, where the client receives a HTTP 202 (Accepted) response and a URL to poll for status updates
- Status updates can be periodically checked for by the client using the provided URL. If the work is still in progress a 200 OK will be returned, and when it is completed a 302 (Found) redirect to the resource it is asking for.
- If an error occurs, the status endpoint can provide appropriate HTTP response codes (e.g. 4xx) and details about the error

Common use cases

- Client-side applications: browsers often make good use of this to keep the GUI responsive when waiting for server side responses
- Service integration: ideal for integrating new services with legacy systems that don't support modern callback technologies

Considerations

- Polling frequency: The Retry-after header should be used to avoid overloading the server with status checks
- Cancellation support: allowing clients to cancel long-running requests can be beneficial for system performance
- Not appropriate when a real-time or near-real-time response is required
- Proper GUI support needs to be put in place so the wait is handled gracefully

![[Pasted image 20241030162004.png]]

Links

[The Asynchronous Request-Reply pattern - DEV Community](https://dev.to/willvelida/the-asynchronous-request-reply-pattern-16ki)
[Asynchronous Request-Reply | Cloud Patterns | Learn | CodeWithStu's Blog](https://im5tu.io/learn/cloud-patterns/asynchronous-request-reply/)