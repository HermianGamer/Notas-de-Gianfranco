A [stack](https://en.wikipedia.org/wiki/Stack_\(abstract_data_type\)) is a data structure that stores ordered items. It's _like_ a list, but its design is more restrictive. It only allows items to be added or removed from the top of the stack:

Click to hide video

It's called a "stack" because it behaves just like a stack of physical items. Imagine a stack of plates: it's easy to take an item off the _top_ of the stack, but you can't really get to the items in the middle or at the bottom without removing the items on top first. You'll often hear a stack referred to as a `LIFO` (last in, first out) data structure.

Whoever decided to take this simple concept and slap a nasty acronym on it should be forced to program in [Prolog](https://en.wikipedia.org/wiki/Prolog) for the rest of their days.

## Assignment

In this chapter we'll build a stack from scratch! A stack will be useful at LockedIn when we need undo/redo functionality. For example, a user can add other users to their "connections" list, and then undo the last connection they added. _Stacks are a great way to implement undo functionality._

For now, we'll just focus on two methods: `push` and `size`. Notice that the Stack class already has a constructor and the underlying [`List`](https://docs.python.org/3/tutorial/datastructures.html) that we'll use to store items.

1. [ ] Complete the `push` method. It should add an item to the top of the stack. The "top" of the stack is the end of the list in our implementation.
2. [ ] Complete the `size` method. It should return the number of items in the stack.

# Stack Review
- All supported operations are `O(1)` by themselves. However, some tasks, like getting to an item at the bottom of the stack have a higher time complexity because they require multiple `pop` operations.
- Stack operations are limited: no searching, no sorting, no random access
- Stacks, like all [abstract data types](https://en.wikipedia.org/wiki/Abstract_data_type), can store items of any type. What makes it a stack is the behavior of the operations, not the type of data it stores.
- Stacks are often used in the real world for:
    - Function call management
    - Undo/redo functionality
    - Expression evaluation
    - Browser history