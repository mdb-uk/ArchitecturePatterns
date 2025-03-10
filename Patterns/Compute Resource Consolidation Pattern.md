15:53 | 2024-11-12
# Links

[[Architecture Patterns Index]]
# Content

This pattern is a strategy used to optimise the use of compute resource in cloud environments.

Cloud apps perform a variety of operations which can be separated into different computational units (i.e. VMs or Containers). Whilst this separation can simplify the design it can also lead to increased costs and complexity (especially when resources are underutilized).

This pattern involves consolidating multiple tasks or operations into a single computational unit. This can:
- Increase resource utilisation - by grouping tasks with similar resource needs
- Reduce costs - by reducing computational unit requirements
- Improve and simplify management

Considerations:
- Scalability and elasticity: ensure that tasks with similar scaling needs are grouped together
- TTL: long running tasks should be managed to avoid disruptions
- Security: tasks within the same unit should have a high level of trust and security measures in place
- Fault tolerance: be aware that a failure in one task can affect others within the same unit

![[Pasted image 20241112160729.png]]

References

[Compute Resource Consolidation pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/compute-resource-consolidation)