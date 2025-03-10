10:25 | 2024-10-18
# Links

[[Architecture Patterns Master Index]]
# Content

[Valet Key pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/valet-key)

![[Pasted image 20241018102557.png]]

1. User requests a resource
2. Application processes the request 
3. Application returns a SAS token minted for the user to access the specific resource
4. User directly accesses the resource

N.B. Step 3 could either return the token to the user with an HTTP redirect to the correct blob URL so the client does not need to know the url.
