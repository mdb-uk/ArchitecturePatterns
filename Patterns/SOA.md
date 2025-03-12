 [[Architecture Patterns Index]] #Decoupling #ApplicationArchitecture
# SOA 


[Service-Oriented Architecture (SOA) is an architectural style in software engineering that focuses on organizing software systems as a collection of services](https://medium.com/cloud-native-daily/system-design-patterns-service-oriented-architecture-151d6354a21)[1](https://medium.com/cloud-native-daily/system-design-patterns-service-oriented-architecture-151d6354a21). Here are some key points about SOA:

- [**Discrete Services**: SOA focuses on discrete services instead of a monolithic design](https://medium.com/cloud-native-daily/system-design-patterns-service-oriented-architecture-151d6354a21)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture). [These services are provided to other components by application components, through a communication protocol over a network](https://medium.com/cloud-native-daily/system-design-patterns-service-oriented-architecture-151d6354a21)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture).
    
- [**Service Properties**: A service in SOA has four properties](https://en.wikipedia.org/wiki/Service-oriented_architecture)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture):
    
    1. It logically represents a repeatable business activity with a specified outcome.
    2. It is self-contained.
    3. It is a black box for its consumers, meaning the consumer does not have to be aware of the service’s inner workings.
    4. It may be composed of other services.
- [**Loose Coupling**: The related buzzword service-orientation promotes loose coupling between services](https://en.wikipedia.org/wiki/Service-oriented_architecture)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture). [SOA separates functions into distinct units, or services, which developers make accessible over a network in order to allow users to combine and reuse them in the production of applications](https://en.wikipedia.org/wiki/Service-oriented_architecture)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture).
    
- [**Interoperability**: SOA defines a way to make software components reusable and interoperable through service interfaces](https://www.ibm.com/topics/soa)[3](https://www.ibm.com/topics/soa). [Services use common interface standards and an architectural pattern so they can be rapidly incorporated into new applications](https://www.ibm.com/topics/soa)[3](https://www.ibm.com/topics/soa).
    
- [**Service Governance**: Service governance controls the lifecycle for development and at the appropriate stage that the services are published in a registry that enables developers to quickly find them and reuse them to assemble new applications or business processes](https://www.ibm.com/topics/soa)[3](https://www.ibm.com/topics/soa).
    
- [**Independence**: SOA is intended to be independent of vendors, products, and technologies](https://en.wikipedia.org/wiki/Service-oriented_architecture)[2](https://en.wikipedia.org/wiki/Service-oriented_architecture). [Applications behind the service interface can be written in Java, Microsoft .Net, Cobol or any other programming language](https://www.ibm.com/topics/soa)[3](https://www.ibm.com/topics/soa).
    

[In summary, SOA is a design principle that supports loose coupling and reusability of different components in a distributed system](https://www.talend.com/uk/resources/service-oriented-architecture/)[4](https://www.talend.com/uk/resources/service-oriented-architecture/).