[[Architecture Patterns Index]]
# HTTP Header routing pattern

Header based routing allows you to target the right service for each request by specifying an HTTP header. The path of the request is still important, but the header allows further routing options.

As well as using it for actions, you can also user header routing to cover version routing, feature flags, a/b testing etc.

Header routing is often combined with other types of routing to create robust APIs (i.e. [[Path routing pattern]], [[Hostname routing pattern]]).

The architecture for Http header routing often has some thin routing layer in front of microservices or similar.
![[Pasted image 20250205132803.png]]

This pattern gives you agility for quick changes and can be automated easily.

You do need full control of the client and the ability to manipulate custom http headers though. Things like proxies, CDNs, load balancers etc can limit header availability and size.

### References

[HTTP header routing pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/api-routing-http.html)