# Maps

Is a data structure to store key-value pairs

1. The keys must be unique and of the same type
2. If a key is repeated, the last value will be stored
3. The values must be of the same type

 ``` go
// map[keyType]valueType
myMap := map[string]int{
    "one": 1,
    "two": 2,
    "three": 3,
}
```

## Iterating over a map

You can iterate over a map using the `range` keyword

``` go
colors := map[string]string{
    "red":   "#ff0000",
    "green": "#4bf745",
    "blue":  "#0000ff",
}

for key, value := range colors {
    fmt.Println("Key:", key, "Value:", value)
}
```

## See also

- [for loop](./loops/for.md)
