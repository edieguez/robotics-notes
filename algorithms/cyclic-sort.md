# Cyclic sort

- It is a problem of sorting an array of numbers from 1 to n.
- It is used in many problems like finding the missing number, finding the duplicate number, etc.
- It is a simple and efficient in-place sorting algorithm.
  - It has less swaps than other sorting algorithms.

``` java
public int findMissingNumber(int[] nums) {
    int index = 0;

    while (index < nums.length) {
        if (nums[index] != index && nums[index] < nums.length) {
            int temp = nums[nums[index]];
            nums[nums[index]] = nums[index];
            nums[index] = temp;
        } else {
            index++;
        }
    }

    for (int i = 0; i < nums.length; i++) {
        if (nums[i] != index) return i;
    }

    // There is no missing number. Returning default value
    return -1;
}
```
