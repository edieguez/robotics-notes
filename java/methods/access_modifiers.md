# Access modifiers

From **more to less restrictive**

| Keyword   | Can be called...                                    |
|-----------|-----------------------------------------------------|
| private   | Only from within the same class                     |
| _default_ | Only from classes in the same package               |
| protected | Only from classes in the same package or subclasses |
| public    | From any class                                      |

## `private`

Can only be called only from within the same class.

## _default_ (no modifier, package-private)

Can only be called from a class in the same package. **It does not have a keyword**.

## `protected`

Can only be called from classes in the same package or subclasses.

## `public`

Can be called from anywhere.
