[[Architecture Patterns Index]] #API #Cybersecurity
# Rate Limiting Pattern

"Many services use a [[Throttling Pattern]] to control the resources they consume, imposing limits on the rate at which other applications or services can access them. You can use a rate limiting pattern to help you avoid or minimize throttling errors related to these throttling limits and to help you more accurately predict throughput.

A rate limiting pattern is appropriate in many scenarios, but it is particularly helpful for large-scale repetitive automated tasks such as batch processing."

A service may throttle based on different metrics over time, such as:

- The number of operations (for example, 20 requests per second).
- The amount of data (for example, 2 GiB per minute).
- The relative cost of operations (for example, 20,000 RUs per second).

### References

[Rate Limiting pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/rate-limiting-pattern)
