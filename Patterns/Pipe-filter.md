[[Architecture Patterns Index]] #Data #DevOps
# Pipe-filter

This pattern is used to process data in a series of steps, where each step (filter) transforms the data and passes it to the next step through a connector (pipe). This pattern is particularly useful for stream processing and data transformation tasks.

Filters:
- Independent processing units: each filter performs specific transformation/processing on the data
- Stateless
- Modular

Pipes:
- Data channels - connects filters together and allows data to flow between them
- Async

Advantages:
- Modular
- Reusable
- Scalable

Disadvantages:
- Latency - the multiple layers of filters & pipes can introduce latency
- Complexity - the more pipes & filters are introduced the more complexity can creep in

Commonly used in ETL pipelines, LLM Compilers and Image processing.

### References

[Pipe and Filter Architecture - System Design - GeeksforGeeks](https://www.geeksforgeeks.org/pipe-and-filter-architecture-system-design/)