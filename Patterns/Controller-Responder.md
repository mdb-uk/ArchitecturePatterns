# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

This pattern is used to manage and distribute tasks efficiently. It is also/formerly known as the Master-Slave pattern.

The Controller is responsible for receiving requests and dividing the work into smaller tasks, then is assigns these tasks to the responder components. It also collects and aggregates the results from the Responders.

The Responder components handle the tasks assigned by the Controller.

This pattern is useful in situations where tasks can be parallelised, such as multi-threaded applications or distributed systems.

![[Pasted image 20240913104847.png]]