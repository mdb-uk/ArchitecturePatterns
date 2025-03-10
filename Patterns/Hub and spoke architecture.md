15:47 | 2025-02-11
# Links

[[Architecture Patterns Index]]
# Content

This network topology involves a central network/VNET (the Hub) and other ones all connected to the central (the Spokes).

In Azure Hubs are typically regional resources.

- The hub enables the following concepts:
    
    - **Cross-premise gateway** - Cross-premise connectivity is the ability to connect and integrate different network environments to one another. This gateway is usually a VPN or an ExpressRoute circuit.
        
    - **Egress control** - The management and regulation of outbound traffic that originates in the peered spoke virtual networks.
        
    - **(optional) Ingress control** - The management and regulation of inbound traffic to endpoints that exist in peered spoke virtual networks.
        
    - **Remote access** - Remote access is how individual workloads in spoke networks are accessed from network location other than the spoke's own network. This could be for the workload's data or control plane.
        
    - **Remote spoke access for virtual machines** - The hub can be a convenient location to build out a cross-organization remote connectivity solution for RDP and SSH access to virtual machines distributed throughout spoke networks.
        
    - **Routing** - Manages and directs traffic between the hub and the connected spokes to enable secure and efficient communication.

![[Pasted image 20250211160710.png]]

![[Pasted image 20250211160730.png]]
### References

https://learn.microsoft.com/en-us/azure/architecture/networking/architecture/hub-spoke