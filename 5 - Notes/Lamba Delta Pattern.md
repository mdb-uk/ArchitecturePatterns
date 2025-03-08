15:09 | 2024-09-23
# Links

[[Architecture]] [[Architecture Patterns Master Index]]
# Content

### Overview

This pattern is primarily used in data processing and analytics systems. It combines two distinct processing methods: batch processing (Delta) and stream processing (Lambda).

The pattern is particularly useful for handling large volumes of data in real-time while also allowing for historical data analysis.

### Key components

#### Lambda

- Speed Layer - processes real-time data streams and provides low-latency access to the most recent data. Typically uses something like Apache Kafka, Apache Flink or Apache Storm.
- Batch Layer - handles large volumes of historical data and performs batch processing. Responsible for generating the master data set. Can use tools like Apache Hadoop or Apache Spark.
- Serving Layer - merges the outputs from the Speed & Batching layers to provide a unified view of the data. It serves the data to consumers.

#### Delta

- Focuses on the incremental processing of data, emphasising the use of CDC (change data capture) and allows for updated to be made to the data more efficiently
- Often uses a single storage layer like a Delta Lake that supports both batch and streaming data, enabling users to perform operations on the data
- It is scalable and offers ACID transactions

![[Pasted image 20240923153740.png]]
### References

[Lambda Architecture Basics | Databricks](https://www.databricks.com/glossary/lambda-architecture)
[What is Lambda architecture | System Design - GeeksforGeeks](https://www.geeksforgeeks.org/what-is-lambda-architecture-system-design/)