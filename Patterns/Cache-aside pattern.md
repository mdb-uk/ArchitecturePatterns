[[Architecture Patterns Index]]
# Cache-aside pattern

This pattern is used to improve the performance and scalability of an application by loading data into the cache on demand.

Key concepts
- Cache miss / Cache hit- when the app requests data it always goes to the cache. If the data is not in the cache (cache miss), it then goes to the main datastore, retrieves the information, and stores it in the cache. If it's already in the cache (cache hit), it uses that
- Lazy loading - data is only loaded into the cache when it is requested the first time, keeping the cache size manageable and ensuring only frequently accessed data is stored
- Write-through / Write-behind - when the data is updated, it is written to both the main datastore and the cache simultaneously (write-through) or, when data is updated, updates are written to the cache first and then to the main data store in an async way

Benefits
- Improved performance
- Scalability

Use cases
- You don't have a cache that provides native functionality read-through and write-through operations
- Resource demand is unpredictable

Might not be suitable when:
- Cached dataset is static - in this case priming the cache with the dataset at start up can yield better performance and set to infinite TTL
- Caching session state information in a web application hosted on some kind of load balanced environment, introducing client-server affinities is not a good strategy in this case

![[Pasted image 20241031144936.png]]

References 
[Cache-Aside pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/cache-aside)
[Cache-Aside Pattern - GeeksforGeeks](https://www.geeksforgeeks.org/cache-aside-pattern/)