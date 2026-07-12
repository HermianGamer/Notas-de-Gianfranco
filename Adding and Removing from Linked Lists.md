# Add to Tail

Time to allow our `LinkedList` to add new nodes to the end of the list. Kind of like a regular Python List's `.append` method.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/HdLqUc2-1271x380.png)

## Assignment

**Complete the `add_to_tail` method**. It adds a new node to the end of the list and returns nothing.

1. [ ] If there isn't a `head` node, set the new node as the `head` and return.
2. [ ] Otherwise, keep a reference to the "last" node in the list - start with it set to the `head`.
3. [ ] Iterate over the linked list (you can use a `for` loop now that you've added your own `__iter__`!)
    - Update your "last" node reference to the current node
4. [ ] Once you've iterated over the entire list, your "last" reference should be the last node in the list (the "tail"). Set the `next` field of the "last" node to the new node.

# Add to Head

For added flexibility, let's allow users to add items to the _front_ of our linked list as well.

## Assignment

**Implement the `add_to_head` method**. It should add a new node to the front of the list and return nothing.

1. [ ] Set the "next" field of the given node to the current head node.
2. [ ] Update the head reference to the given node.


# Linked List Queue

To use our Linked List as a fast queue (`O(1)` pushes _and_ pops) we need our `add_to_tail` function to be `O(1)`. Currently, it iterates over the entire list before appending an item. We can fix this by _keeping track_ of the last item with a new data member: `tail`.

_Note: It's common in algorithms to make this kind of trade-off. By using a little extra memory (keeping track of `tail`), we can make our operations faster. Sometimes you might need to go the other way, and use more computation time to save memory._

## Assignment

LockedIn's queue was working just fine on small datasets, but appending items once the list has 100,000+ items has started to take a toll on our servers. **Implement these changes to speed up our Linked List's inserts** to `O(1)`:

1. [ ] Update the constructor to set `self.tail` to `None`.
2. [ ] Update `add_to_head` to also set the `tail` reference to the given node if the list is empty.
3. [ ] Update `add_to_tail`:
    1. [ ] Set the head _and_ tail to the given node if the list is empty.
    2. [ ] Instead of iterating through the list to find the last node, use the `tail` node to append the new node (for example, set `self.tail.next` to the new node).
    3. [ ] Update the `tail` reference to new node.

# Remove from Head

We're one method away from having a fully functioning `O(1)` Queue! We just need a way to remove the first element from the linked list in _constant_ time. When we're finished, our `LinkedList` will fulfill the basic requirements of a Queue:

- `add_to_tail`: Constant time insert
- `remove_from_head`: Constant time pop

Let's rename the `LinkedList` class to `LLQueue` and remove the `add_to_head` functionality because Queues don't allow inserting into the wrong end.

_We've also flipped the arrows in the printed representation to reflect the change_.

## Assignment

**Complete the `remove_from_head` method**. It should remove the first node from the list (the head) and return it.

1. [ ] If the list is empty, just return `None`.
2. [ ] Assign the head to be removed to a variable.
3. [ ] Set the list's head to the next node in the list.
4. [ ] If the list became empty, set the list's tail to `None`.
5. [ ] Detach the removed head by setting its `next` to `None`.
6. [ ] Return the removed head.

Boots