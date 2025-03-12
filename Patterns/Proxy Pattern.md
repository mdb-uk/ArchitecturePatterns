[[Architecture Patterns Index]] #SoftwareEngineering #Structural
# Proxy Pattern

This is a structural design pattern that lets you provide a substitute or placeholder for another object. The eponymous Proxy then controls access to the original object, allowing custom behaviour to be executed before and/or after the request gets routed to the original object.

This pattern can be useful where you might have an expensive resource that occasionally needs to be accessed, and for whatever reason you cannot amend that object to contain lazy initialisation logic (say it's a 3rd party component or an external library).

![[Pasted image 20241120114711.png]]

The proxy pattern lets us create a proxy object with the same interface as the original object. You then update all callers to point to the proxy. The proxy manages an instance of the real destination (including techniques like lazy loading it) and delegates requests to it (and as mentioned before can execute additional logic before or after forwarding the original request).

![[Pasted image 20241120115217.png]]
In this example, the CachedYoutubeClass is the proxy which implements the same interface as the real object (YoutubeManager), but extends the functionality by offering caching for improved performance. When the requested video is not cached it would delegate the request to an actual instance of YoutubeManager.

References

[Proxy](https://refactoring.guru/design-patterns/proxy)