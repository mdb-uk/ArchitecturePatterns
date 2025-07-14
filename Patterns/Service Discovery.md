[[Architecture Patterns Index]] #Microservices #Decoupling #Decentralisation 

# Service Discovery

This pattern is a key aspect of distributed systems or microservice architectures. It enables potential clients of the various services to dynamically discover the available services in an environment that features change or evolution.

In a traditional monolithic application the components are fixed and static so this is not a concern, however in a microservice (or other distributed) architecture you don't want references to other services hardcoded, and that is where Service Discovery comes in. When a service moves or changes you can simply update the registry in there, so the client apps will be simply pointed to the new service when they look up Auth, or whatever other functionality they need.

## Key components

- Service registry - a central database/datastore of some kind that keeps track of all the services and their instances. Services register themselves when they start and de-register themselves when they stop
- Service provider - a microservice (for example) that offers a particular service which registers itself with the service registry on startup
- Service consumer - any app that wants to consume services, and looks up a given service in the service registry
- Service discovery mechanism:
	- Client side discovery: The Service Consumer looks up the service they need in the Service Registry
	- Server side discovery: The Service Consumer calls the load balancer as normal and the load balancer looks up the service in the Service Registry