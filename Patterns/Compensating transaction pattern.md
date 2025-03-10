[[Architecture Patterns Index]]
# Compensating transaction pattern

This pattern is used to maintain data consistency in distributed systems, especially when dealing with eventual consistency.

In distributed systems, operations often span multiple services or data stores. Making sure that strong transactional consistency happens can be difficult and impact performance. Therefore eventual consistency is often used where a temporary inconsistency might be acceptable as long as the system eventually returns to a consistent state (once all operations have been completed).

The Compensating Transaction pattern addresses failures in such operations by allowing steps to be undone if subsequent steps fail. The compensating transactions are operations that reverse the original transactions. Steps in a compensating transaction should be idempotent (they can be repeated without causing unintended effects).

![[Pasted image 20241108164012.png]]

### References

[Compensating Transaction pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/compensating-transaction)