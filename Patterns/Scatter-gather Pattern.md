13:35 | 2025-02-05
# Links

[[Architecture Patterns Master Index]]
# Content

This is a message-routing pattern that involves broadcasting similar or related requests to multiple recipients and aggregating their responses back into a single message via an aggregator.

This pattern can helps achieve parallelisation, reduces processing latency and handles async communication.

You can implement it synchronously, and this is easier, but less powerful. The most effective way to employ it async with message routing, either with or without a messaging service.

Useful when you have a large costly message you can break down into smaller messages and handled in parallel, or when you want to send requests to multiple external systems (i.e. APIs). The results are aggregated so an informed decision can be made on what to do next.

Considerations:
- Fault tolerance - faults must be handled gracefully. Redundancy, replication and fault detection can help mitigate the overall impact on the system.
- Scale-out limits - the number of processing nodes comes with extra overheads (load and latency)
- Response-time bottlenecks - For operations that require all recipients to be processed before final processing is done the whole operation will only be as fast as it's slowest response.
- Partial responses - timeouts can mean you get partial responses from clients on occasion, this should be handled gracefully
- Data consistency - synchronisation and consistency of data is important in this pattern

Scatter by distribution:
![[Pasted image 20250205134803.png]]

Scatter by auction (for when the controller, in green, is unaware of the recipients):
![[Pasted image 20250205134814.png]]

### References

[Scatter-gather pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/scatter-gather.html)