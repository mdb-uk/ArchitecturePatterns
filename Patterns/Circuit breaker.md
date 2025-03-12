[[Architecture Patterns Index]] #ErrorHandling #Resilience
# Circuit breaker

![[Pasted image 20240729100320.png]]

An intermediary service (the "circuit breaker") is placed between a calling service and a target service. It observes conditions in the target. If a specific condition is met, the circuit breaker trips and re-routes traffic to an alternative target service.

#### Pros

- Using a circuit breaker to respond to the onset of a hazardous condition in a fault tolerant manner is an excellent way to prevent accidents before they happen. 
- Provides a good way to make systems fault-tolerant at a fine level of activity.

#### Cons

- Testing can be harder than it appears. More is required than simply having the circuit breaker close down access to a particular service. A variety of failure responses need to be in force and these responses need to be tested.
- Circuits are difficult to do as a one-off. They require an infrastructure management technology such as a service mesh that can manage the switching on and off.