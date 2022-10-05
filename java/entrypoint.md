# Java entrypoint

## `main()` method

This method must exist in order to run a .class using Java

``` java
public class Main() {
    public static void main(String[] args) {
        System.out.println("Hello world");
    }
}
```

## Single-file source-code

From Java 11 you can run a file without compiling it first *«it gets compiled in memory»*

This method has some caveats

- It is slower than running an already compiled file
- The program must consist of a single class
- You can only refer to external classes that come bundled with the JDK

``` shell
java Main.java
```
