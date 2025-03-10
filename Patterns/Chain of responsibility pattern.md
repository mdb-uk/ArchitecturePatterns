11:54 | 2024-11-20
# Links

[[Software design patterns Master Index]]
# Content

This is a behavioural design pattern that allows you to pass requests along a chain of handlers. Each handler makes the decision to either process it itself, or pass it along to the next handler in the chain.

An example of usage of this pattern is auth checks. You might want to check if a user is authenticated first, and only if they are then pass the request to other handlers to check if they are authorised as a user, as an admin etc. 

You might also want to perform security validation checks in the chain as well, such as brute force detection etc. This could be a handler in its own right, and if it detects an attack it would not forward on to the next hander.

![[Pasted image 20241120115740.png]]

There's also a different approach where each handler in the chain might decide if it can handle the request, and if so you wouldn't want it passed on as it should only be handled once:

![[Pasted image 20241120115849.png]]
### References

[Chain of Responsibility](https://refactoring.guru/design-patterns/chain-of-responsibility)