# Eviction policies

The eviction policy is a strategy to determine which key-value pairs to evict when the cache is full

## 1. Least Recently Used (LRU)

The least recently used (LRU) policy discards the least recently used items first. This algorithm requires keeping track of what was used when, which is expensive if one wants to make sure the algorithm always discards the least recently used item.

## 2. Least Frequently Used (LFU)

The least frequently used (LFU) policy discards the least frequently used items first. This algorithm requires keeping track of what was used when, which is expensive if one wants to make sure the algorithm always discards the least frequently used item.

## 3. First In First Out (FIFO)

The first-in, first-out (FIFO) policy discards the oldest items first. This algorithm is easy to implement and efficient in terms of time and space complexity.
