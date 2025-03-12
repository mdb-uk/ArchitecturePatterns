[[Architecture Patterns Index]] #Decoupling #Resilience
# Master-Slave

This design approach  is used to distribute tasks and improve system performance and reliability.

The master node, i.e. the central unit, controls things and delegates tasks to multiple slave units. The slave units execute the tasks assigned to them and report back with the results. The master aggregates the responses together.

Benefits of this design:
- Parallel processing: tasks processed simultaneously speeding up overall execution time
- Fault tolerance: one slave node failing does not impact the overall system much
- Scalable: more slave nodes can easily be added

This pattern is often used in Data processing use cases, and distributed computing scenarios.

The downsides are overheads of splitting and merging tasks, the complexity of managing comms and synchronisation, and the single point of failure the master node represents.

![[Pasted image 20240924101154.png]]
### References

[Master-Slave Architecture - GeeksforGeeks](https://www.geeksforgeeks.org/master-slave-architecture/)