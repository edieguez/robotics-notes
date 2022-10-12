# Java blocks

A code block is code that is between brackets (`{` and `}`)

## Order of initialization

1. Fields and static/instance initializer blocks are run in the order they appear in the file
2. The constructor runs after all fields and instance initializer blocks have run
3. `static` and instance blocks run **before** an static method. i.e. `main` method

``` java
public class Generic {
    private String name;

    static {
        log.info("Static code executed");
    }

    {
        log.info("Anonymous block executed");
    }

    public static void main(String[] args) {
        Generic generic = new Generic("Generic instance");
        log.info(generic.getName());
    }
}
```

> **Output**<br>
> [main] INFO com.artemisa.Generic - Static code executed<br>
> [main] INFO com.artemisa.Generic - Anonymous block executed<br>
> [main] INFO com.artemisa.Generic - Generic instance

## `static` block

1. It is executed **ONCE** the first time an instance of the class is created
2. You can have multiple static blocks declared in the same class

``` java
public class Generic {
    static {
        log.info("Static code executed A");
    }

    static {
        log.info("Static code executed B");
    }

    static {
        log.info("Static code executed C");
    }
}
```

## Instance block

1. It is executed **every time a new instance is created**
2. You can have multiple instance blocks declared in the same class

``` java
public class Generic {
    {
        log.info("Anonymous/instance block executed A");
    }

    {
        log.info("Anonymous/instance block executed B");
    }

    {
        log.info("Anonymous/instance block executed C");
    }
}
```
