[[Architecture Patterns Index]] #Resilience #Decentralisation
# Leader Election Pattern

This pattern is used in distributed systems to coordinate tasks among multiple instances by electing one instance as the 'leader'. The leader is responsible for managing and coordinating the actions of other instances.

Various algorithms can be used to 'elect' the leader including the Bully algorithm, Raft consensus algorithm, Ring algorithm.

To offer resilience the system will elect a new leader if there is an outage that means the leader is unavailable.

Considerations
- Failure handling must be properly considered - failures must be quickly detected and a new leader elected if needed
- Avoid making the leader a bottleneck - it is only coordinating tasks not performing them

![[Pasted image 20241206151930.png]]
### References

[Leader Election pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/leader-election)
