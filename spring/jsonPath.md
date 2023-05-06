# JSON path

## Dependencies

1. [jsonpath](https://mvnrepository.com/artifact/com.jayway.jsonpath/json-path)
2. [jackson](https://mvnrepository.com/artifact/com.fasterxml.jackson.core/jackson-core)

## Configuration

By default, the jsonpath library uses the `json-smart` library to parse json. The `json-smart` library does not support `TypeRef`. The following code will throw an exception

```java
DocumentContext context = JsonPath.parse(response);
context.read("$[0].phonetics[?(@.audio)].audio", new TypeRef<>() { });
```

> `java.lang.UnsupportedOperationException: Json-smart provider does not support TypeRef! Use a Jackson or Gson based provider`

To fix the issue, you need to [configure the jsonpath library to use jackson/gson](https://stackoverflow.com/questions/34111276/jsonpath-with-jackson-or-gson)

```java
@Configuration
public class BeanConfig implements InitializingBean {

    @Override
    public void afterPropertiesSet() {
        com.jayway.jsonpath.Configuration.setDefaults(new com.jayway.jsonpath.Configuration.Defaults() {
            private final JsonProvider jsonProvider = new JacksonJsonProvider();
            private final MappingProvider mappingProvider = new JacksonMappingProvider();

            @Override
            public JsonProvider jsonProvider() {
                return jsonProvider;
            }

            @Override
            public MappingProvider mappingProvider() {
                return mappingProvider;
            }

            @Override
            public Set<Option> options() {
                return EnumSet.noneOf(Option.class);
            }
        });
    }
}
