# [Map](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Map.html)

Data structure with key-value pairs. The most common implementation is [HashMap](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/HashMap.html). It shares some methods with `ArrayList` like `clear()`, `isEmpty()` and `size()`. It also has its unique methods

| Method                                | Description                                                       |
|---------------------------------------|-------------------------------------------------------------------|
| `V get(Object key)`                   | Returns the value mapped by `key` or `null` if none is mapped     |
| `V getOrDeafult(Object key, V other)` | Returns the value mapped by `key` or `other` if none is mapped    |
| `V put(K key, V value)`               | Adds or repaces key/value pair. Returns previous value or `null`  |
| `V remove(Object key)`                | Removes and returns value mapped to `key`. Returns `null` if none |
| `boolean containsKey(Object key)`     | Returns whether `key` is in map                                   |
| `boolean containsValue(Object key)`   | Returns whether `value` is in map                                 |
| `Set<K> keySet()`                     | Returns a set of all keys                                         |
| `Collection<V> values()`              | Returns `Collection` of all values                                |
