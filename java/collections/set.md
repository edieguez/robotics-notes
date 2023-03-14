# [Set](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Set.html)

`public interface Set<E> extends Collection<E>`

Is a `Collection` that cannot contain duplicate elements. It extends from `Collection`. It is the reason why `add(E e)` and `addAll(Collection<? extends E> c)` return `boolean`. If the element already exists, it will not be added and the method will return false.

The two main implementations of `Set` are [HashSet](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/HashSet.html) and [TreeSet](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/TreeSet.html)

- `HashSet` is backed by a `HashMap` and `TreeSet` is backed by a `TreeMap`
- `HashSet` is faster than `TreeSet` because it does not need to sort the elements
- `HashSet` is not sorted and `TreeSet` is sorted
