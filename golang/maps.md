# Maps

Is a data structure to store key-value pairs

1. The keys must be unique and of the same type
2. If a key is repeated, the last value will be stored
3. The values must be of the same type
4. A comma is required after the last value

 ``` go
// map[keyType]valueType
myMap := map[string]int{
    "one": 1,
    "two": 2,
    "three": 3,
}
```

## Accessing values

``` go
fmt.Println(myMap["one"])
```

## Adding values

> **If the key already exists, the value will be updated**

``` go
myMap["four"] = 4
```

## Deleting values

``` go
delete(myMap, "four")
```

## Checking if a key exists

``` go
value, exists := myMap["four"]

if exists {
    fmt.Println("Value:", value)
} else {
    fmt.Println("Key not found")
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
