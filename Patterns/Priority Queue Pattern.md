[[Architecture Patterns Index]]
# Priority Queue Pattern

This pattern enables a workload to prioritise certain tasks and have them dealt with before lower priority tasks.

A typical FIFO queue structure does not allow for any prioritisation to take place.

In the priority queue pattern, the sending application assigns a priority to the message, and the consumers process the messages by priority.

This can be achieved either with a single queue or multiple queues (in the latter case a separate queue is used for each priority level).

Single queue
![[Pasted image 20250106144759.png]]

Multiple queue
![[Pasted image 20250106144815.png]]

Single consumer pool variant:
![[Pasted image 20250106145019.png]]
The single consumer pool variant is suitable for applications where ease of setup and maintenance is a priority.

### References

[Priority Queue pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/priority-queue)