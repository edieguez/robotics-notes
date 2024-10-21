# Two pointer

Two pointers work towards a solution by converging from different ends of an array

- `use case` find pairs in a sorted array
- `example` find pairs in a sorted array that sum to a target value

``` java
public int[] twoSum(int[] array, int target) {
    int left = 0;
    int right = array.length - 1;

    while (left < right) {
        int sum = array[left] + array[right];

        if (sum == target) {
            return new int[] {left, right};
        } else if (sum < target) {
            left++;
        } else {
            right--;
        }
    }

    return new int[] {-1, -1};
}
```
