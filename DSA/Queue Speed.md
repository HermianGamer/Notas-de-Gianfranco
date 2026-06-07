So how fast are queue operations? Well, in an optimized queue, they'd be:

|Operation|Big O|Description|
|---|---|---|
|push|`O(1)`|Add an item to the back of the queue|
|pop|`O(1)`|Remove and return the front item from the queue|
|peek|`O(1)`|Return the front item from the queue without modifying the queue|
|size|`O(1)`|Return the number of items in the queue|

Just like a stack, _all_ operations are `O(1)`! No matter how many items are in the queue, these operations will always take the same amount of time. The reason to choose a queue over a stack is all about _ordering_. Queues should be used when you need to process items in _the order they were added_.

LIFO (stack) vs FIFO (queue).

## A Problem

Our current `Queue` class has a problem... take a look at the `push` method:

```python
def push(self, item: str) -> None:
    self.items.insert(0, item)
```

It's _not_ `O(1)`! The List's `insert` method has to shift all the other items in the list down to make room for the new item.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/lMdF5yz-1211x720.png)

We'll solve this very solvable problem soon...