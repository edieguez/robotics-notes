# Cyclic sort

Sort numbers when elements fall within a range

- `use case` finding missing numbers in an array
- `example` find the missing number from 1 to n

``` java
public int findMissingNumber(int[] nums) {
    int i = 0;

    while (i < nums.length) {
        if (numbs[i] != i && nums[i] < nums.length) {
            int temp = nums[numbs[i]];
            nums[numbs[i]] = nums[i];
            nums[i] = temp;
        } else {
            i++;
        }
    }

    // find the missing number
    for (int i = 0; i < nums.length; i++) {
        if (nums[i] != i) {
            return i;
        }
    }

    return nums.length;
}
```
