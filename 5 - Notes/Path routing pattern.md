15:44 | 2025-02-04
# Links

[[Architecture Patterns Master Index]]
# Content

Routing by paths is the mechanism of grouping multiple or all APIs under the same hostname, and using a request URI to isolate services; for example, `api.example.com/service-a` or `api.example.com/service-b`.

This pattern simplifies the API architecture. 

However it does involve operational overhead such as configuration, authorization, integrations and additional latency due to multiple hops.

A HTTP Service reverse proxy can be used to create dynamic routing configurations. If using a K8S setup you can also create an ingress rule to match a path to a service.

Reverse proxy method:
![[Pasted image 20250204154725.png]]

API Gateway method - similar to reverse proxy but simpler:
![[Pasted image 20250204154810.png]]
### References

[Path routing pattern - AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/api-routing-path.html)