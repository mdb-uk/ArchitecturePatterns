[[Architecture Patterns Index]]
# Edge Workload Configuration Pattern

This pattern is used to manage and configure workloads at the edge of a network, such as IoT devices or edge servers.

This pattern is particularly useful in environments where devices need to have the ability to work independently from the cloud, ensuring continued functionality for the business even when the device is offline and therefore has no connection to the cloud.

Key features
- Multiple configuration points - configurations can be grouped into layers (e.g. software source, CI/CD pipeline, cloud tenant, and edge location). Each layer can be updated by different people
- Offline access - configurations must be accessible offline at the edge to ensure continuous operation
- Global view - a global view of configurations should be available in the cloud for centralised management purposes

Considerations
- Complexity - allowing edits when disconnected from the cloud increases complexity (particularly with auth and conflict resolution)
- Network constraints in edge environments - these constraints need to be managed carefully
- Configuration management - it's important to track and audit configuration changes in edge environments