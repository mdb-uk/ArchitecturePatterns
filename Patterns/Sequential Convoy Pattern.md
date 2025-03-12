[[Architecture Patterns Index]] #Communication #DistributedSystems
# Sequential Convoy Pattern

This pattern allows you to process a group of related messages in order. Multiple groups of messages can be processed simultaneously.

In a distributed architecture, workers can scale independently so it's not easy to ensure messages get processed in order. Also consumers can often pull messages from the queue independently such as the [[Competing Consumers Pattern]].

The solution to this problem is to push messages into categories within the queueing system, so the consumers can lock and pull from one category only, preserving the FIFO system.

![[Pasted image 20250129132211.png]]

Messages for different categories might be interleaved within the queue:
![[Pasted image 20250129132230.png]]

Issues and considerations

- What property of the incoming messages to scale out on? E.g. order Id, so each unique order gets it's own consumer spun up
- Throughput - What is your target message throughput? If it is very high, you may need to reconsider your FIFO requirements. For example, can you enforce a start/end message, sort by time, then send a batch for processing?
- Service capabilities. Does your choice of message bus allow for one-at-a-time processing of messages within a queue or category of a queue?
- How can you add a new category of message if needed?
- It's possible that consumers might receive a message out of order, due to variable network latency when sending messages. Consider using sequence numbers to verify ordering. You might also include a special "end of sequence" flag in the last message of a transaction. Stream processing technologies such as Spark or Azure Stream Analytics can process messages in order within a time window.

On Azure, this pattern can be implemented using Azure Service Bus [message sessions](https://learn.microsoft.com/en-us/azure/service-bus-messaging/message-sessions). For the consumers, you can use either Logic Apps with the [Service Bus peek-lock connector](https://learn.microsoft.com/en-us/azure/connectors/connectors-create-api-servicebus) or Azure Functions with the [Service Bus trigger](https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-service-bus).

In this example the messages are received batched then fanned out by the Ledger processer:

![[Pasted image 20250129132527.png]]

The ledger processor takes care of:

1. Walking the ledger one transaction at a time.
2. Setting the session ID of the message to match the order ID.
3. Sending each ledger transaction to a secondary queue with the session ID set to the order ID.

The consumers listen to the secondary queue where they process all messages with matching order IDs _in order_ from the queue. Consumers use [peek-lock](https://learn.microsoft.com/en-us/azure/service-bus-messaging/message-transfers-locks-settlement#peeklock) mode.

When considering scalability, the ledger queue is a primary bottleneck. Different transactions posted to the ledger could reference the same order ID. However, messages can fan out _after_ the ledger to the number of orders in a serverless environment.
### References

[Sequential Convoy pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/sequential-convoy)
