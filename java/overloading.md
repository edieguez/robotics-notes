# Method overloading

Is having the **same method name** with **different parameters**. Everything but the method name can be different. This includes

- Access modifiers
- Specifiers (like `static`)
- Return types
- Exceptions thrown

## Parameter list

Java does not care about the name of the parameters, only the type. This means that the following is not allowed

```java
public void doSomething(int a, int b) {}
public void doSomething(int b, int a) {} // Not allowed
```

But you can specify different number and type of parameters

```java
public void doSomething(int a, int b) {}
public void doSomething(int a, int b, int c) {}
public void doSomething(int a, String b) {}
```
