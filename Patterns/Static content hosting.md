[[Architecture Patterns Index]]
# Static content hosting

This pattern is designed to efficiently serve static content such as HTML pages, images, CSS/JavaScript files and documents by leveraging cloud based storage services.

To enhance performance and availability a CDN can be used to cache static content in multiple locations worldwide. This ensures faster delivery to users regardless of their location.

Benefits:
- Better Performance
- Scalability
Considerations:
- Managing separate deployments for static and dynamic content can be challenging, versioning and synchronisation are therefore critical.
- Security - you must ensure the content containers are correctly permissioned for read only access to the public to prevent unauthorised uploads
- Custom domains - some storage services may not support these and require full URLs for static resources
- Not useful if the static content needs to be customised before delivery
- Not efficient for small volumes of static data due to overheads

![[Pasted image 20240808120352.png]]

References

[Static Content Hosting pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/static-content-hosting)
[The pros and cons of the Static Content Hosting architecture pattern | Enable Architect (redhat.com)](https://www.redhat.com/architect/pros-and-cons-static-content-hosting-architecture-pattern)
