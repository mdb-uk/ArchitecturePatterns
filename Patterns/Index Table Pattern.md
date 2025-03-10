[[Architecture Patterns Index]]
# Index Table Pattern

This pattern is used to improve query performance in data stores, particularly when the data store doesn't support secondary indexes. The pattern creates indexes to cover fields that are often queried.

If you have a Customer table with columns ID (PK), Name, Address 1, Address 2, Post Code and City and an app needs to look up Customers based in a certain city, the Primary index is not going to help. A secondary index on the City field (and potentially Post Code) will allow the app to do more performant lookups.

If you are using a data store which does not natively support Secondary Indexes you can manually create index tables. 

![[Pasted image 20241203154903.png]]
Above: An Index Table sorted by City

![[Pasted image 20241203155504.png]]
Above: an example where the data has been normalised to use Fact and Index Tables

### References

[Index Table pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/index-table)