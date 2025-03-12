[[Architecture Patterns Index]] #Routing #API
# Hostname routing pattern

This pattern is a mechanism for isolating API services by giving each API it's own hostname, such as `service-a.api.example.com` or `service-a.example.com`.

This reduces the amount of friction in releases because nothing is shared between the teams deploying their respective services.

Each team manages everything their service needs including the DNS entries.

Considerations:
- Consumers have to remember different hostnames to interact with each API, which can be mitigated by providing a client SDK.
- Registering the subdomain or domain is required every time a new service is created

![[Pasted image 20250131134028.png]]
### References

[Hostname routing pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/api-routing-hostname.html)