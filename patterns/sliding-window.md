# Sliding window

Used to track a subset of elements in an array or string. The subset is usually a contiguous sub array or substring.

- `use case` maximum sum of sub arrays
- `example` maximum sum of sub array of size k

``` java
public int maxSubArraySum(int[] array, int k) {
    int maxSum = 0;
    int windowSum = 0;

    for (int i = 0; i < array.length; i++) {
        windowSum += array[i];

        if (i >= k - 1) {
            maxSum = Math.max(maxSum, windowSum);
            windowSum -= array[i - (k - 1)];
        }
    }

    return maxSum;
}
```
