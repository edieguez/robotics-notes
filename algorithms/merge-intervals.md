# Merge intervals

- It is a problem of merging overlapping intervals. Given a collection of intervals, merge all overlapping intervals.
- It is used in many problems like scheduling, time management, etc.

``` java
public class MergeIntervals {
    public int[][] merge(int[][] intervals) {
        if (intervals.length <= 1) {
            return intervals;
        }

        // Sort the intervals by start time
        Arrays.sort(intervals, (a, b) -> a[0] - b[0]);

        List<int[]> merged = new ArrayList<>();

        for (int[] interval : intervals) {
            // merged.isEmpty():
            //  if the list is empty, add the interval. This is the first interval.
            // merged.get(merged.size() - 1)[1] < interval[0]:
            //  if the end of the last interval is less than the start of the current interval, add the interval.
            if (merged.isEmpty() || merged.get(merged.size() - 1)[1] < interval[0]) {
                merged.add(interval);
            } else {
                // If the end of the last interval is greater than the start of the current interval, merge the intervals.
                merged.get(merged.size() - 1)[1] = Math.max(merged.get(merged.size() - 1)[1], interval[1]);
            }
        }

        return merged.toArray(new int[merged.size()][]);
    }
}
```
