A linked list is a collection of ordered items, so it's similar to a "normal" list (also called an "array" or "slice" in other languages).

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/3hQ1f0A-1270x720.png)

Items in a "normal" list are stored next to each other in memory, and to get an item from a normal `List` we have to use a numbered index:

```python
car = cars[3]
```

You can think of the "index" as simply an offset from the start. The `cars` list in this example refers to the start of the list, and `3` is just the 4th item in that section of memory. With a normal list, all the data is stored in the same place in memory and the index is just a way to find the right spot.

In a linked list, _there are no indexes_! Each node contains two things: the data itself, and a _reference_ to the next node in the list. Iterating over a linked list requires starting at the head node and following the `next` references until you reach the end.

```python
current_car_node = head_car_node
while current_car_node is not None:
    print(current_car_node.val)
    current_car_node = current_car_node.next
```

Frankly, linked lists can be annoying to use and incur more overhead, **so why use a linked list at all**? It's because _sometimes_ linked lists are much faster to make updates to, _particularly when inserting or deleting items from the middle_.

In a normal list, if you insert an item in the middle, you have to shift _all_ the items after it down one spot, which takes `O(n)` time:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/PmWhmiC-1280x656.png)

In a linked list, once you've traversed to a given node, insertion is `(O(1))` because you can simply update _two_ references:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/c9kHujM-1280x650.png)