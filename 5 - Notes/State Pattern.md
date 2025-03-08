11:20 | 2025-01-06
# Links

[[Software design patterns Master Index]]
# Content

The State Pattern is a behavioural design pattern that lets an object alter it's behaviour when it's internal state changes. It appears to the outside world as if the object has changed it's Class.

This can be in response to the internal state machine of an application requiring some kind of change based on an event of some kind. Traditionally these changes might be handled with conditional logic, but this gets unwieldy the bigger the state machine gets and the more states there are to reflect.

The State Pattern instead suggests that you create classes for all possible states of an object and extract state specific behaviours into these classes. 

The original object, i.e. the context, stores a reference to one of the State objects to represent it's current state, and delegates all state related work to that object. All state objects must implement the same interface for this to work. 

This pattern is similar to the Strategy pattern, however whilst Strategies would not know about each other in the State pattern the States can know about each other and even include logic to transition to other States etc.

![[Pasted image 20250106112726.png]]
### References

[State](https://refactoring.guru/design-patterns/state)