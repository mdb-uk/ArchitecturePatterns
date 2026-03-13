[[Architecture Patterns Index]] #Auth

# Distributed Authorisation Model

The Distributed Authorisation Model can be thought of as "Claims‑based identity with resource‑based authorization", and is an approach to an IAM (Identity & Access Management) where authentication (the act of verifying a user is who they say they are) and some authorisation (verifying what permissions a user has) are handled centrally by an IDP (Identity provider), whilst fine-grained authorisation is delegated to the client applications (web apps, APIs, microservices etc).

This pattern ensures that requests are authenticated by a central, trusted authority and also authorised within the specific context of individual applications. This aligns with zero-trust principles were identity and specific permissions are verified in a decentralised way.

In practice, this could mean that Entra External ID (for example) authenticates a user by asking for credentials and challenging for MFA etc, then issues a token to them and provides some coarse-grained authorisation data (like user identity, group and role membership etc), and then each client application checks that tokens validity and enforces additional context-specific authorisation checks before allowing access to resources.

![[ArchitecturePatterns-Distributed Authorisation.drawio.png]]

Another related option is the [[Resource-enforcer]] pattern, in which the resource server itself makes API calls to an external Dynamic Authorization system.
### References

[Centralized vs. Distributed Authorization: the CAP theorem - Styra](https://www.styra.com/blog/centralized-vs-distributed-authorization-the-cap-theorem/)

[Authorization Design Patterns](https://openid.github.io/authzen/patterns.html#name-user-journeys)