# Merge intervals

This pattern works with multiple intervals. Then it merges all the overlapping intervals

- `use case` schedule meetings
- `example` merge overlapping intervals

``` java
public int[][] merge(int[][] intervals) {
    if (intervals.length < 2) {
        return intervals;
    }

    // Sort the intervals by start time
    Arrays.sort(intervals, (a, b) -> Integer.compare(a[0], b[0]));

    List<int[]> merged = new ArrayList<>();
    int start = intervals[0][0];
    int end = intervals[0][1];

    for (int[] interval : intervals) {
        if (merged.isEmpty() || merged.get(merged.size() - 1)[1] < interval[0]) {
            merged.add(interval);
        } else {
            merged.get(merged.size() - 1)[1] = Math.max(merged.get(merged.size() - 1)[1], interval[1]);
        }
    }

    return merged.toArray(new int[merged.size()][]);
}
```
