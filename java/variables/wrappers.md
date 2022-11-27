# Wrappers

Primitive types have wrapper classes. They're useful when we need to store a primitive value but there's also the possibility that the value is `null`

| Wrapper   | String to primitive            | String to wrapper         |
|-----------|--------------------------------|---------------------------|
| Boolean   | `Boolean.parseBoolean("true")` | `Boolean.valueOf("TRUE")` |
| Byte      | `Byte.parseByte("1")`          | `Byte.valueOf("2")`       |
| Short     | `Short.parseShort("1")`        | `Short.valueOf("2")`      |
| Integer   | `Integer.parseInt("1")`        | `Integer.valueOf("2")`    |
| Long      | `Long.parseLong("1")`          | `Long.valueOf("2")`       |
| Float     | `Float.parseFloat("1")`        | `Float.valueOf("2.2")`    |
| Double    | `Double.parseDouble("1")`      | `Double.valueOf("2.2")`   |
| Character | Use `charAt()` method          | Use `charAt()` method     |
