# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

This is a database Architecture pattern where a database is partitioned into smaller, more manageable parts called Shards. Sharding is particularly useful for managing large-scale databases, offering significant improvements in performance, maintainability, and scalability. 

Each shard operates independently. Therefore, a query on one shard doesn’t affect the performance of another. Each Shard is a distinct database, but collectively all the shard databases make up the entire database. 

The Shards of the data are known as logical shards. Each Shard is stored on a separate node - known as a physical shards. Adding further shards on additional storage nodes allows you to scale out the system in a controlled manner.

## Sharding types

### Horizontal Sharding

Sharding *typically* involves horizontal partitioning, where rows of a database table are held separately, rather than dividing the table itself (vertical partitioning).

Horizontal sharding:
![[Pasted image 20240802140248.png]]

### Vertical Sharding

Vertical Sharding is also possible though, and involved splitting up the columns between shards. This might be suited when certain tables are accessed more often than others.

Vertical sharding
![[Pasted image 20240802140417.png]]

## Sharding strategies

### Hash-Based Sharding

Uses a hash function to determine the shard that each record goes into. The function takes a key, typically a specific column(s) from the row, and the resulting hash determines which Shard the record goes into.

It is ideal when uniform distribution of data is important such as Session based web apps.

![[Pasted image 20240802140840.png]]
### Range-Based Sharding

Sorts records based on where in a range the shard key falls. Suitable for time-series or sequential data such as log events.

![[Pasted image 20240802140928.png]]
### Directory-Based Sharding

Uses a lookup service or directory to keep track of which Shard holds given data. Maps via the Shard Key.

Can be effective where data distribution is non-uniform or when dealing with complex partitioning criteria.

![[Pasted image 20240802141059.png]]

### Geo-Sharding

Data is Sharded based on geographic locations. Ideal for services that require data locality to be maintained.

## References

[Architecture Patterns: Sharding - DZone](https://dzone.com/articles/architecture-patterns-sharding)
[Sharding pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/sharding)
