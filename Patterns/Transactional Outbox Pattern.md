[[Architecture Patterns Index]] #EventDriven #DistributedSystems #Transactional
# Transactional Outbox Pattern

This pattern aims to solve the dual write operations issue that occurs in distributed systems when a single operation involves a datastore write operation and a message or event notification to other systems (which may perform processing off the back of it). If either of these operations in the dual write, then the system might be left in an inconsistent state.

This pattern is useful when:
- You're building an event driven application where DB updates initiate events to other parts of the system (or other systems)
- You want to ensure atomicity in operations involving multiple services
- You are using [[Event Sourcing]]

Considerations
- You need to deal with the possibility of duplicate messages, making the service idempotent is a good practice
- Order of notification - send messages in the same order which the service updates the database. This is critical for the event sourcing pattern (which offers point in time restore). Eventual consistency and rollback can compound the issue if order is not maintained
- Transaction rollback - don't send event notifications in the event of a rollback
- Service-level transaction handling - if the transaction spans multiple services that require data store updates, use the [[Saga Pattern]] to orchestrate and preserve data integrity

![[Pasted image 20250206074748.png]]
![[Pasted image 20250206074806.png]]![[Pasted image 20250206074813.png]]

### References

[Transactional outbox pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/transactional-outbox.html)