# Method declaration

![Method declaration](assets/method_basic_syntax.png)

Method names follow the same rules for naming as [variables](../variables/naming.md)

This is named `method declaration` and defines all the information required to call the method. The method parameters are known as the `method signature`

> Method signature **only involves name and parameter list**, **not the return type or exceptions thrown**. This is important when overloading methods (`@Override`) and when calling methods with the same name but different parameters. Also really useful when using *reflection*.

## Parts of method declaration

| Element                 | Value in nap() example      | Required?                         |
|-------------------------|-----------------------------|-----------------------------------|
| Access modifier         | public                      | No                                |
| Optional specifier      | final                       | No                                |
| Return type             | void                        | Yes                               |
| Method name             | nap                         | Yes                               |
| Parameter list          | (int minutes)               | Yes, but can be empty parentheses |
| Optional exception list | throws InterruptedException | No                                |
| Method body             | { // take a nap }           | Yes, but can be empty braces      |

## See also

- [Optional specifiers for methods](./specifiers.md)
