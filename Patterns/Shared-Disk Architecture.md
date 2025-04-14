 [[Architecture Patterns Index]] #DistributedSystems #Resilience
# Shared-Disk Architecture

[[Shared-Nothing Architecture]]

Shared Disk Architecture is an architecture that is used in distributed computing in which the nodes share the same disk devices but each node has its own private memory. The disks have active nodes which share memory in case of any failures. In this architecture, the disks are accessible from all the cluster nodes. This architecture has quick adaptability to the changing workloads. It uses robust optimization techniques.

See table summary in the linked Shared-Nothing Architecture note.

![[Pasted image 20250414101249.png]]
### References

[Shared Disk vs. Shared Nothing Architectures: Understanding the Differences | by Vignesh Pathakamuri | Medium](https://medium.com/@vigneshpathakamuri6/shared-disk-vs-shared-nothing-architectures-understanding-the-differences-93913860d39f)

[Shared Disk Architecture – System Design | GeeksforGeeks](https://www.geeksforgeeks.org/shared-disk-architecture-system-design/)