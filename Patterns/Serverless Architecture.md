07:38 | 2024-10-25
# Links

[[Architecture Patterns Index]]
# Content

This pattern involves building and running applications without managing the underlying infrastructure. A cloud provider such as Azure or AWS handles provisioning, scaling and maintenance of the servers that are actually running the code under the hood. They are usually stateless (although exceptions to this exist like Azure Durable functions)

### Core principles
- Function as a Service (FaaS) - The functions developers write are executed in response to events. Examples are AWS Lambdas and Azure Functions.
- Backend as a Service (BaaS) - Utilises third party services for backend functionality, such as databases and auth

#### Benefits
- Cost efficiency
- Scalability
- Reduced operational overhead (no management of servers)

### Common Patterns
- API Gateway & Lambda - API Gateway routes requests to Lambda functions, which handle the application logic
- Fan-Out Pattern: A single event triggers multiple functions to handle different parts of a task in parallel
- Messaging Pattern: Functions communicate asynchronously via message queues, decoupling their execution
- Schedule based tasks
- Asynchronous processing
- Real time data processing (structured or unstructured data)

### Best practices
- Keep functions small and focused
- Implement robust error handling
- Optimize costs (using concepts like throttling and timeouts)
- Ensure observability is considered properly

![[Pasted image 20241029152619.png]]

### References
- [What is Serverless Architecture | Google Cloud](https://cloud.google.com/discover/what-is-serverless-architecture?hl=en)
- [Serverless Architecture Patterns and Best Practices](https://www.freecodecamp.org/news/serverless-architecture-patterns-and-best-practices/)
- [Serverless Architectures](https://martinfowler.com/articles/serverless.html)