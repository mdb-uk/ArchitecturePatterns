[[Architecture Patterns Index]] #Auth

# Resource-enforcer

An Authorisation pattern where the resource server itself makes API calls to an external authorisation system, which acts as the decision point, evaluating authorisation requests, applying policies and returning a decision.

This is the most flexible way to integrate external authorization as it can be used by most resource types, including legacy apps.

![[ArchitecturePatterns-Resource-enforcer.drawio.png]]

Advantages of this pattern are high compatibility, low complexity. Disadvantages are the introduction of a single point of failure.
### References

[Authorization Design Patterns](https://openid.github.io/authzen/patterns.html#name-external-api-call-resource-)