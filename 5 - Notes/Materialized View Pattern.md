06:46 | 2024-12-13
# Links

[[Architecture Patterns Master Index]]
# Content

This is a design approach used to optimise data querying and retrieval.

It generates pre-computed views of data, stored in a query optimised format. Materialized views store the results of complex queries, improving query time and reducing repeated computations.

### How it works

1. Data is precomputed and stored in a materialized view (the view contains only the data required for specific queries, potentially including derived data columns, aggregated values and transformed data)
2. Read-only: views are not editable, updated when the underlying source tables change
3. Materialized views can be optimised for specific queries

### Considerations

- Deciding when to update can be crucial (timed schedule, when data changes, manually)
- Storage overheard - you will incur extra storage for the materialized views

This pattern is widely used in environments where query performance is critical (i.e. Data warehousing or real-time analytics)

![[Pasted image 20241213065150.png]]
### References

[Materialized View pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/materialized-view)