# Autoboxing and unboxing

> **Autoboxing** convert a primitive in its wrapper class
> **Unboxing** convert a wrapper into its primitive type

``` java
List<Integer> list = new ArrayList<>();
list.add(1); // Autoboxing
list.add(2); // Autoboxing
list.add(3); // Autoboxing

log.info("{}", list);

list.remove(2);

log.info("{}", list);

list.remove(Integer.valueOf(2));

log.info("{}", list);
```

> **Output**
> [1, 2, 3]
> [1, 2]
> [1]
