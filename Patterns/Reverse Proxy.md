09:03 | 2025-02-19
# Links

[[Architecture Patterns Master Index]]
# Content

This pattern involves a server, the reverse proxy, sitting between a client and backend servers. The server forwards client requests to the appropriate backend server and then returns the server's response to the client.

Typically a client on the internet makes a request to the reverse proxy server. The Proxy server inspects the request, checks validity and forwards it to the appropriate backend server if the required data is not already in it's cache. It then returns any response from the server to the client, and caches it. The client has no knowledge or vision of the internal network, only seeing the reverse proxy server.

The reverse proxy can help with security, validation, load balancing etc.

A major risk is that the reverse proxy becomes a single point of failure. It can also introduce more latency to the overall system/network.

![[Reverse Proxy.png]]

### References

https://en.wikipedia.org/wiki/Reverse_proxy