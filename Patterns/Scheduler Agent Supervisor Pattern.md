[[Architecture Patterns Index]]
# Scheduler Agent Supervisor Pattern

This pattern coordinates a set of distributed actions as a single operation. If any of the actions fail it will attempt to handle the failures transparently and if this still does not lead to successful completion then the entire operation will be rolled back in a transaction like manner. This can add resiliency to a distributed system.

The pattern has a Scheduler which arranges the various steps and orchestrates their operation in the correct order. It will record the state of the workflow after each step, and track how long each step takes (and can apply limits to this).

The Scheduler will typically communicate with the Agent using async request/response messaging. This can be via queues for instance.

The Agent contains logic that encapsulates a call to a remote service or access to a remote resource. Each agent will typically wraps calls to a single service or resource. It will use some sort of correlation ID across retry attempts.

The Supervisor monitors the status of the tasks in the steps being performed by the scheduled. It runs on a timer. If it detects timed out or failed steps it arranged for an agent to take any remedial action needed (by instructing the scheduler which instructs agents.

![[Pasted image 20250127152959.png]]

This diagram shows a simplified version of the pattern. In a real implementation, there might be many instances of the Scheduler running concurrently, each a subset of tasks. Similarly, the system could run multiple instances of each Agent, or even multiple Supervisors. In this case, Supervisors must coordinate their work with each other carefully to ensure that they don't compete to recover the same failed steps and tasks. The [[Leader Election Pattern]] provides one possible solution to this problem.

### Considerations

- This pattern can be difficult to implement and requires thorough testing of any possible failure mode of the system
- The recovery/retry logic implemented by the Scheduler is complex and dependent on state information held in the state store. It might also be necessary to record the information required to implement a compensating transaction in a durable data store. A compensating transaction might fail as well.
- How often the Supervisor runs will be important. It should run often enough to prevent any failed steps from blocking an application for an extended period, but it shouldn't run so often that it becomes an overhead.
- The steps performed by an Agent could be run more than once. The logic that implements these steps should be idempotent.

### References

https://learn.microsoft.com/en-us/azure/architecture/patterns/scheduler-agent-supervisor