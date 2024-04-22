# What is a cache data structure ?

A cache is a temporary data storage structure that stores a subset of data from a larger, slower data source (such as a database or a file system) to provide faster access to frequently used data. Caches are used to improve the performance of applications by reducing the need to fetch data from the slower data source repeatedly.

The main idea behind caching is to keep recently accessed or frequently used data in a fast-access storage area, so that subsequent requests for the same data can be served quickly without having to access the slower data source again.

Caches are typically implemented using data structures such as hash tables, arrays, or specialized cache data structures. These data structures provide efficient storage and retrieval mechanisms for the cached data.

Some key characteristics of cache data structures include:

1. **Capacity**: Caches have a limited capacity, and once the capacity is reached, a cache replacement policy is used to determine which data should be evicted to make room for new data.
2. **Caching Policy**: The caching policy determines which data should be cached and for how long. Examples of caching policies include Least Recently Used (LRU), Least Frequently Used (LFU), and Time-Aware Least Recently Used (TLRU).
3. **Eviction Policy**: When the cache reaches its capacity, an eviction policy is used to determine which data should be removed from the cache to make room for new data. Common eviction policies include LRU, LFU, and First-In-First-Out (FIFO).
4. **Look-up Efficiency**: Cache data structures are designed to provide efficient look-up operations, typically with an average time complexity of O(1) for well-designed caches.
5. **Write Policy**: The write policy determines how data is written to the cache and the underlying data source. Write-through caches write data to both the cache and the underlying data source simultaneously, while write-back caches write data to the cache first and then periodically update the underlying data source.

Caches are widely used in various applications, such as web browsers (caching web pages and resources), databases (caching query results), file systems (caching file data), and CPU caches (caching frequently accessed memory regions). Proper use of caching can significantly improve application performance by reducing the number of expensive operations required to fetch data from slower data sources.

# What is LRU cache and how is it implemented ?

LRU (Least Recently Used) cache is a cache data structure that keeps track of the most recently used items in the cache. It is designed to evict the least recently used items when the cache reaches its capacity, making room for new items.

The LRU cache is particularly useful in scenarios where you have a limited amount of memory or storage and want to keep the most relevant data in the cache while discarding the least recently accessed data.