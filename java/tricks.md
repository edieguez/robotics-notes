# [Java tricks](https://blog.devgenius.io/java-pro-tips-rare-tricks-to-supercharge-your-programming-d4290c100d56)

## Double brace initialization

```java
Map<String, String> map = new HashMap<>() {{
    put("key1", "value1");
    put("key2", "value2");
    put("key3", "value3");
}};

map.forEach((key, value) -> log.info("{}: {}", key, value));
```

> **Output**\
> key1: value1\
> key2: value2\
> key3: value3
