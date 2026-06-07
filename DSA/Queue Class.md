
![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/txoawjF-1280x357.png)

## Assignment

LockedIn uses a Queue to keep track of the order that recruiters should use to reach out to job seekers.

**Implement the following operations on the `Queue` class**:

- `queue.push(item)`: Adds an item to the tail of the queue (index 0 of list)
- `queue.pop()`: Removes and returns an item from the head of the queue (_last_ index of list)
- `queue.peek()`: Returns an item from the head of the queue
- `queue.size()`: Returns the number of items in the queue

_Note: You'll often hear words used interchangeably in programming. For example, here we're saying `push` and `pop`, but `enqueue` and `dequeue` are also common words for the same ideas_.

|term 1|term 2|description|
|---|---|---|
|Push|Enqueue|Adds an item to the tail of the queue|
|Pop|Dequeue|Removes and returns an item from the head of the queue|

## Tips
- The underlying data type we're using is just a `List`. Don't forget to [guard](https://www.boot.dev/blog/computer-science/guard-clauses/) against [IndexErrors](https://docs.python.org/3/library/exceptions.html#IndexError) by returning 'None' if the queue is empty.
- The [.insert](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists) List method may be helpful.