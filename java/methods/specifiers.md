# Opcional specifiers for methods

| Modifier       | Description                                                                                                   |
|----------------|---------------------------------------------------------------------------------------------------------------|
| `static`       | Indicates the method is a member of the shared class object                                                   |
| `abstract`     | Used in an abstract class or interface when the method body is excluded                                       |
| `final`        | Specifies that the method may not be overridden in a sub-class                                                |
| `default`      | Used in an interface to provide a default implementation of a method for classes that implement the interface |
| `synchronized` | Used with multithreaded code                                                                                  |
| `native`       | Used when interacting with code written in another language, such as C++                                      |
| `strictfp`     | Used for making floating-point calculations portable                                                          |

> **Specifiers can appear in any order**, but **they must appear before the return type**.

## See also

- [Method declaration](./readme.md)
