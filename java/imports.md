# Imports

- `java.lang` is imported automatically
- Package names contain (usually) the name of the company's website written backwards. i.e. `com.google.guava`
- You can use wildcards to import all the classes in a package. i.e. `import java.util.*`
  - It only matches classes
  - At most only one wildcard is allowed and must be at the end

## Redundant imports

``` java
// Redundant; java.lang is imported automatically
import java.lang.System;
import java.lang.*;

// Redundant; Random is imported using the * notation
import java.util.Random;
import java.util.*;

public class ImportExample {
    public static void main(String[] args) {
        Random r = new Random();
        System.out.println(r.nextInt(10));
    }
}
```

## Name collisions

``` java
import java.util.*;
import java.sql.*; // causes Date declaration to not compile
```

> **Output**
> Date date;
> ^
> both class **java.sql.Date** in java.sql and class **java.util.Date** in java.util match

``` java
import java.util.Date;
import java.sql.Date;
```

> **Output**
> error: reference to Date is ambiguous
> Date date;
> ^
> both class **java.util.Date** in java.util and class **java.sql.Date** in java.sql match

This can be solved using *fully qualified names* or by explicitly importing one `Date` class. In other words, **explicit imports take precedence over wildcard imports**

``` java
import java.util.Date;
import java.sql.*;

public class Conflicts {
    Date date;
    java.sql.Date sqlDate;
}
```
