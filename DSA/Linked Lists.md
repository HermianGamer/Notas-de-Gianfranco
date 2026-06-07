Remember how the `push` method on our Queue is `O(n)` instead of `O(1)`?

```python
def push(self, item: str) -> None:
    # everything in self.items has to shift
    # up a position, which takes O(n) time
    self.items.insert(0, item)
```

_Let's fix that_.

To build a faster queue, we'll use a [Linked List](https://en.wikipedia.org/wiki/Linked_list) instead of a regular `List` (array) under the hood. A linked list is where elements are _not_ stored next to each other in memory, instead, each item _references_ the next in a chain.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/7UXPMpU-1280x383.png)

## Nodes

Our nodes will be represented by a simple class with two fields:

- `val` - The raw string value that the node holds (e.g. 'Carla', 'James', etc)
- `next` - A reference to the next node in the list

## Assignment

Let's lock-in and make LockedIn faster!

1. [ ] Complete the `Node`'s constructor.
    1. [ ] Set its `val` field to the provided value.
    2. [ ] Set its `next` field to `None`.
2. [ ] Complete the `Node`'s `set_next` method. It should set the `next` field to the provided node.

Boots