# Variable scope

Lambda is allowed to reference some variables from the surrounding code.

| Variable type     | Rule                         |
|-------------------|------------------------------|
| Instance variable | Allowed                      |
| Static variable   | Allowed                      |
| Local variable    | Allowed if effectively final |
| Method parameter  | Allowed if effectively final |
| Lambda parameter  | Allowed                      |

Within a lambda, the following rules apply

1. Lambda parameters **can** be modified
2. Instance variables **can** be modified
3. Method variables **cannot** be modified

``` java
class Access {
    private String instance = "instance";

    public void method() {
        String method = "method";

        Consumer<String> lambda = parameter -> {
            String local = "local";

            log.info("Variables accessible within lambda:");
            log.info(instance);
            log.info(method);
            log.info(local);
            log.info(parameter);
        };

        lambda.accept("argument");
    }
}
```

> **Output**\
> Variables accessible within lambda:\
> instance\
> method\
> local\
> argument
