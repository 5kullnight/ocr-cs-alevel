Caching is the process of storing instructions or values in cache memory after they have been used, as they may be used again. This saves time that would have been needed to store and retrieve the instructions from secondary storage again. Caching is very common in the storage of web pages. The web pages that a user frequently accesses are cached, so the next time one of these pages is accessed, content can be loaded without any delay. This also means images and text do not have to be downloaded again multiple times, freeing up bandwidth for other tasks on a network.
A more advanced variation of caching and thinking ahead is **prefetching**, in which algorithms predict which instructions are likely to soon be fetched. The instructions and data which are likely to be used are then loaded and stored in cache before they are fetched. By thinking ahead, therefore, less time is spent waiting for instructions to be loaded into RAM from the hard disk.
Clearly, one of the biggest limitations to this is the accuracy of the algorithms used in prefetching, as they can only provide an informed prediction as to the instructions which are likely to be used, and there is no guarantee that this will be right. Similarly, the effectiveness of caching depends on how well a caching algorithm is able to manage the cache. Larger caches still take a long time to search, and so cache size limits how much data can be stored. In general, this form of thinking ahead can be difficult to implement but can significantly improve performance if implemented effectively.