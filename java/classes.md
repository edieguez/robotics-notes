# Classes

- A file can contain multiple classes
- At most, only one class per file can be public
- The public class **must** match the filename

## Definition

`public`|*`default`* [`abstract`|`final`] `class` *ClassName* [`extends` *AnotherClass*] [`implements` *InterfaceName*] { /\* class body */ }

## Basic class structure (PIC)

1. **P**ackage
2. **I**mport
3. **C**lass

``` java
package structure; // If present, must be the first non-comment

import java.util.*; // If present, must be outside a class and after 'package'

public class Meerkat { // Class declaration after 'package' and imports
    // Fields and methods can go in any order
    double weight;

    public double getWeight() {
        return this.weight;
    }

    double height;
}
```

## Inner classes

- Is any class whose declaration occurs within the body of another class or interface
- Can contain `final static` fields but not static methods

## Anonymous classes

- Cannot have explicitly defined constructors since they don't have a name

## Static classes

- A class defined inside an interface is implicitly static
