### Caching Project Tasks

| Task              | Description                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Basic dictionary**  | Implement a basic caching system using a dictionary with no size limit.                                                               |
| **FIFO caching**      | Implement a caching system that discards the first item added when the cache limit is reached (FIFO).                                   |
| **LIFO caching**      | Implement a caching system that discards the last item added when the cache limit is reached (LIFO).                                    |
| **LRU caching**       | Implement a caching system that discards the least recently used item when the cache limit is reached (LRU).                            |
| **MRU caching**       | Implement a caching system that discards the most recently used item when the cache limit is reached (MRU).                             |
| **LFU caching**       | Implement a caching system that discards the least frequently used item when the cache limit is reached, using LRU if frequency ties.  |

#### Task Details

**0. Basic dictionary**
- **File**: [0-basic_cache.py](0-basic_cache.py)
- **Description**: 
  - This task involves creating a `BasicCache` class that inherits from `BaseCaching`.
  - The cache is implemented using a dictionary `self.cache_data`.
  - It has no limit on the number of items it can store.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the key or item is `None`, the method does nothing.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.

**1. FIFO caching**
- **File**: [1-fifo_cache.py](1-fifo_cache.py)
- **Description**: 
  - This task involves creating a `FIFOCache` class that inherits from `BaseCaching`.
  - The cache uses a dictionary `self.cache_data` and follows the FIFO (First In, First Out) eviction policy.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the cache exceeds `BaseCaching.MAX_ITEMS`, it discards the oldest item added. If the key or item is `None`, the method does nothing. It prints `DISCARD: ` followed by the discarded key.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.

**2. LIFO caching**
- **File**: [2-lifo_cache.py](2-lifo_cache.py)
- **Description**: 
  - This task involves creating a `LIFOCache` class that inherits from `BaseCaching`.
  - The cache uses a dictionary `self.cache_data` and follows the LIFO (Last In, First Out) eviction policy.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the cache exceeds `BaseCaching.MAX_ITEMS`, it discards the most recently added item. If the key or item is `None`, the method does nothing. It prints `DISCARD: ` followed by the discarded key.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.

**3. LRU caching**
- **File**: [3-lru_cache.py](3-lru_cache.py)
- **Description**: 
  - This task involves creating a `LRUCache` class that inherits from `BaseCaching`.
  - The cache uses a dictionary `self.cache_data` and follows the LRU (Least Recently Used) eviction policy.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the cache exceeds `BaseCaching.MAX_ITEMS`, it discards the least recently used item. If the key or item is `None`, the method does nothing. It prints `DISCARD: ` followed by the discarded key.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.

**4. MRU caching**
- **File**: [4-mru_cache.py](4-mru_cache.py)
- **Description**: 
  - This task involves creating a `MRUCache` class that inherits from `BaseCaching`.
  - The cache uses a dictionary `self.cache_data` and follows the MRU (Most Recently Used) eviction policy.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the cache exceeds `BaseCaching.MAX_ITEMS`, it discards the most recently used item. If the key or item is `None`, the method does nothing. It prints `DISCARD: ` followed by the discarded key.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.

**5. LFU caching**
- **File**: [100-lfu_cache.py](100-lfu_cache.py)
- **Description**: 
  - This task involves creating a `LFUCache` class that inherits from `BaseCaching`.
  - The cache uses a dictionary `self.cache_data` and follows the LFU (Least Frequently Used) eviction policy.
  - **Methods**:
    - `put(self, key, item)`: Adds the item to the cache using the specified key. If the cache exceeds `BaseCaching.MAX_ITEMS`, it discards the least frequently used item. If there are multiple items with the same frequency, it uses the LRU policy to discard the least recently used item among them. If the key or item is `None`, the method does nothing. It prints `DISCARD: ` followed by the discarded key.
    - `get(self, key)`: Retrieves the item associated with the specified key from the cache. If the key is `None` or doesn't exist in the cache, it returns `None`.
