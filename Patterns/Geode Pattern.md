11:22 | 2024-11-29
# Links

[[Architecture Patterns Master Index]]
# Content

This architecture involves deploying a collection of backend service into a set of geographical nodes, the geodes, each of which can service any request for any client in any region.

Traffic is routed to the nearest geode using a load balancer.

Each geode is an independently operating self-contained unit.

This enables an active-active style, improving latency and increasing availability by distributing request processing geographically.

![[Pasted image 20241129134635.png]]

### References

[Geode pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/geodes)
