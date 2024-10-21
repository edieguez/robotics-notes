# Tortoise and Hare (Floyd's) algorithm

Two pointers moving at different speeds to detect cycles in sequences

- `use case` detect cycles in linked lists
- `example` check if a linked list has a cycle

``` java
public boolean hasCycle(ListNode head) {
    ListNode slow = head;
    ListNode fast = head;

    while (fast != null && fast.next != null) {
        slow = slow.next;
        fast = fast.next.next;

        if (slow == fast) {
            return true;
        }
    }

    return false;
}
```
