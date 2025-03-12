[[Architecture Patterns Index]] #Resilience
# Health Endpoint Monitoring Pattern

This pattern is designed to make sure that apps are performing as they should by implementing functional checks that are accessed through specific endpoints (such as "/health") at regular intervals. An http response code will generally indicate the result of the check (200 == OK, 500 == Internal server error etc)

![[Pasted image 20241203115322.png]]

Services and tools are available that monitor application health and typical things they might check include:
- Validation of the response code (i.e. looking for a 2xx code)
- Checking the content of the response
- Measuring response time
- Security checks i.e. TLS cert expiry
- DNS lookup time
- External resource access time
### References

[Health Endpoint Monitoring pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/health-endpoint-monitoring)

