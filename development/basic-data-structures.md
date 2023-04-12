# Basic data structures

## Array

Arrays are a collection of values. They are ordered and can be accessed by index. The index starts at 0.

- `Search` O(1)
- `Insert end` O(1)
- `Remove end` O(1)
- `Insert start/mid` O(n)
- `Remove start/mid` O(n)

## Linked list

A linked list is a collection of nodes. Each node has a value and a pointer to the next node. The first node is called the `head` and the last node is called the `tail`

- `Search` O(n)
- `Insert end` O(1)
- `Remove end` O(1)
- `Insert start/mid` O(1)
- `Remove start/mid` O(1)

## Hashmap

A hashmap is a collection of `key-value` pairs. It **is unordered and can be accessed by key**. The key is hashed to an index.

- `Search` O(1)
- `Insert` O(1)
- `Remove` O(1)

## Deque (Double-ended queue)

A queue is a collection of values. It is ordered and can be accessed by index. The index starts at 0. The first value is called the `front` and the last value is called the `back`.

- `Search` O(n)
- `Push front` O(1)
- `Pop front` O(1)
- `Push back` O(1)
- `Pop back` O(1)

## Binary tree

A binary tree is a collection of nodes. Each node has a value and a pointer to the left and right node. The first node is called the `root`.

- `Search` O(log n)
- `Insert` O(log n)
- `Remove` O(log n)

## Trie/Prefix tree

A trie is a collection of nodes. It is used to store strings and retrieve strings by prefix. Each node has a value and a pointer to the next node. The first node is called the `root`.

- `Search` O(n)
- `Insert` O(n)

## Heap

A heap is a collection of values. It is ordered and can be accessed by index. The index starts at 0. The first value is called the `root`.

- `Insert` O(log n)
- `Pop` O(log n)
- `Min/max` O(1)

## Graph

Is the general node structure on which trees, tries and binary trees are based. Due to its generality, it is the most complex node-related structure
