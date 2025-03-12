[[Architecture Patterns Index]] #EventDriven
# Event Driven Architecture (EDA)


### Overview

Typified by an Event Producer, Potentially Event Ingestion and One or many Event consumers.

Can follow two sub-patterns, publish-subscribe and event streaming.

Example Azure services for pub-sub are Event Grid, Service Bus. 

Example Azure services for event streaming is Event Hubs.

### Common variations on the consumer side

- Simple event processing - an event immediately triggers an event in the consumer
- Basic correlation - a consumer needs to process a small number discrete events usually correlated by some identifier
- Complex event processing - processing a stream of events looking for patterns/insights using something like Azure Stream Analytics
- Event stream processing - Use a data streaming platform, such as Azure IoT Hub or Apache Kafka, as a pipeline to ingest events and feed them to stream processors. The stream processors act to process or transform the stream.

### When to use this architecture

- Multiple subsystems must process the same events
- real-time (or near-real-time) processing with minimal lag
- Complex event processing, such as pattern matching or aggregation over time windows.
- High volume and high velocity of data, such as IoT.

### Benefits

- Producers and consumers are decoupled.
- No point-to-point integrations. It's easy to add new consumers to the system.
- Consumers can respond to events immediately as they arrive.
- Highly scalable and distributed.
- Subsystems have independent views of the event stream.

### Drawbacks

- Guranteed delivery can be an issue
- Order of operations or only-once can be challenging
- Coordinating messages across services (workflow patterns such as choreography or saga orchestration can help with this)