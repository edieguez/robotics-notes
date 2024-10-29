# In-place linked list reversal

Used to reverse a linked list in place. That is without using extra space

- `use case` reversing a sublist of a linked list
- `example` reverse a linked list

```java
public ListNode reverseList(ListNode head) {
    ListNode prev = null;
    ListNode current = head;

    while (current != null) {
        ListNode next = current.next;
        current.next = prev;
        prev = current;
        current = next;
    }

    return prev;
}
```
