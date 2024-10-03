# Comparing

## Comparing arrays with compare()

### General rules

1. Negative number means the first array is smaller than the second
2. Zero means they are equals
3. Positive number means the first array is larger than the second

### Array specific rules

1. `Return zero`
   1. If both arrays have the same length and all elements are equal and in the same order
2. `Negative number`
   1. If all the elements are the same but the first array is shorter than the second
   2. If the first element that is different is smaller in the first array
3. `Positive number`
   1. If all the elements are the same but the first array is longer than the second
   2. If the first element that is different is larger in the first array
4. When comparing two arrays, they **must be of the same type**

> Check next section to know what *being smaller* means

## compareTo() rules

1. `null` is smaller than any other value
2. For number, numeric comparison applies
3. For `Strings`, numbers are smaller than letters
4. For `Strings`, one is smaller if it is a prefix of another
5. For `Strings`, uppercase is smaller than lowercase

## mismatch()

1. If the arrays are equal, returns -1
2. Otherwise, returns the index of the first mismatch
