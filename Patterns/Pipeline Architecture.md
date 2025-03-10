14:12 | 2025-01-29
# Links

[[Architecture Patterns Index]]
# Content

This pattern is commonly used in big data processing and software engineering. There are a series of data processing steps where each step performs it's task and then passes information on to the next step.

There are several sub patterns you could use:

- **Batch Processing Pattern**: This involves processing data in large, discrete sets or batches. It is suitable for scenarios where data does not need to be processed in real-time.
- **Stream Processing Pattern**: This involves processing data in real-time as it arrives. It is suitable for scenarios where timely processing is critical.
- **Lambda Architecture Pattern**: This combines both batch and stream processing to provide a balance between real-time processing and comprehensive batch processing. [[Lamba Delta Pattern]]
- **Microservices-based Pattern**: This involves breaking down the pipeline into smaller, independent services that can be developed, deployed, and scaled independently. [[Microservices]]
- **Event-driven Architecture Pattern**: This involves processing data based on events or triggers. It is suitable for scenarios where actions need to be taken in response to specific events. [[Event Driven Architecture (EDA)]]

[[Pipe-filter]] is also related.
### References

[What Data Pipeline Architecture should I use? | Google Cloud Blog](https://cloud.google.com/blog/topics/developers-practitioners/what-data-pipeline-architecture-should-i-use)
[Message from Monte Carlo](https://www.montecarlodata.com/blog-data-pipeline-architecture-explained/)