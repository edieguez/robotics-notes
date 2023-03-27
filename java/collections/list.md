# [List](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/List.html)

The most popular `List` implementation is `ArrayList`. It is a resizable array, which means that it can grow or shrink as needed to accommodate adding or removing items. It is not thread-safe, so it is not recommended to use it in a multi-threaded environment.

## Array to List

Both of the following methods return a `Serializable` and `RandomAccess` list backed by the specified array. The returned list is fixed-size, which means that you cannot add or remove elements from it. If you try to do so, you will get an `UnsupportedOperationException`. Both support the [varargs](../methods/varargs.md) syntax.

### Backed List

The `Arrays.asList()` method returns a fixed-size list backed by the specified array. You can modify the array or the list itself. It will modify the other one as well. **It is a bidirectional binding**

```java
String[] array = {"a", "b", "c"};
List<String> list = Arrays.asList(array);

list.add("d"); // UnsupportedOperationException
list.remove(0); // UnsupportedOperationException
list.set(0, "e"); // ["e", "b", "c"]
```

### Inmutable List

The `List.of()` method returns an immutable list containing the specified elements. If you modify the array, the list will not be modified

```java
List<String> list = List.of("a", "b", "c");

list.add("d"); // UnsupportedOperationException
list.remove(0); // UnsupportedOperationException
list.set(0, "e"); // UnsupportedOperationException
```
