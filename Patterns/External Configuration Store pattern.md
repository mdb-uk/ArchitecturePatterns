11:18 | 2024-11-19
# Links

[[Architecture Patterns Index]]
# Content

This pattern involves moving configuration out of the application code / deployment package entirely and storing it in a centralised location (such as Azure Configuration Manager).

Benefits

- Easier management and control - easier to update and maintain settings without redeploying the application
- Shared configuration - multiple apps and instances can share configuration, ensuring consistency and reducing redundancy
- Dynamics updates - settings can be updated on the fly without application redeployment or restarting, particularly useful in cloud environments where apps need to scale and adapt quickly
- Versioning and flexibility - the pattern supports versioning of config settings allowing different environments to have their own configurations

Considerations
- Availability
- Backup
- Flexibility (types of information)
- Caching

![[Pasted image 20241119114135.png]]
### References

[External Configuration Store pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/external-configuration-store)