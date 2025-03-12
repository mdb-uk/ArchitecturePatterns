[[Architecture Patterns Index]] #SoftwareEngineering #Behavioural
# Strategy Pattern

The Strategy Pattern is a behavioural design pattern that lets you define a related family of algorithms, put each into a separate class, and make their objects interchangeable.

The original class, or Context, has a field for storing a composed reference to one of the Strategies (which all implement the same interface), then the specific choice of strategy can be selected at execution time based on the appropriate decisions.

![[Pasted image 20250106114222.png]]

### References

[Strategy](https://refactoring.guru/design-patterns/strategy)