[[Architecture Patterns Index]]
# Claim Check Pattern

This is an architectural approach used to handle large messages in messaging systems.

Steps
1. The large message is stored in an external data store (rather than being sent through a messaging system)
2. Claim check generation: a claim check token is generated for the stored payload
3. The messaging system sends a message with the claim check token to the destination application
4. The destination application received the claim check message and uses the claim check token to retrieve the large message from the external data store

Advantages
- Performance improvement by not sending large messages through the messaging system
- Scalability - by avoiding overloading the bus the system scales better
- Security - sensitive messages and data can be handled by this pattern because they are secured with the claim check token whilst they are in the external data store

Disadvantages
- Adds potential points of failure (the bus and the external data store) and increases support load
- Adds maintenance (clean up of the external data store)
- Potential latency of reading/writing the large messages

Use cases
- Large message handling - when the message size is too big for the message bus
- Sensitive data - by using this pattern you limit the potential exposure
- Complex routing - using this pattern reduces load on intermediary components

![[Pasted image 20241105153420.png]]

References

[Claim-Check pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/claim-check)
[Claim-Check Pattern: When To Split a Large Message Into a Claim-Check and a Payload | AKF Partners](https://akfpartners.com/growth-blog/claim-check-pattern)