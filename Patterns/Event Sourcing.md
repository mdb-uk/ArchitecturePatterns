 [[Architecture Patterns Index]] #EventDriven #Data
# Event Sourcing

This pattern is a way of handling data operations. Rather than just maintaining the current state of data, it keeps a full record (append-only) of all events that have occurred.

Key concepts:

- Event store: this is where the log of all events is kept
- Events: each event represents a single change to the system
- Reconstruction: the event history can be replayed to reconstruct the current state or the state at a point in time
- Audit trail: we have a full history of changes which can be useful for many reasons

![[Pasted image 20240920072509.png]]
# References

[Event Sourcing pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing)

[Event Sourcing (martinfowler.com)](https://martinfowler.com/eaaDev/EventSourcing.html)