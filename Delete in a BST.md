We also need a way to remove users from our BST if a user decides to delete their account.

## Assignment

**Implement the recursive [delete](https://en.wikipedia.org/wiki/Binary_search_tree#Deletion) method**. It takes a value as an input and deletes the node with that value _if it exists_. Each call `return`s the _new_ root of the tree (or subtree) after the deletion.

Notice that in the test suite the `delete` method is called like this:

```python
bst = bst.delete(character)
```

1. [x] Check if the current node is empty (has no value). If it is, return `None`. This represents an empty tree or a leaf node where deletion has already occurred.
2. [x] If the value to delete is less than the current node's value:
    1. [ ] If there's a left child, recursively delete the value from the left subtree and update the left child reference with the result.
    2. [ ] Return the current node.
3. [x] If the value to delete is greater than the current node's value:
    1. [x] If there's a right child, recursively delete the value from the right subtree and update the right child reference with the result.
    2. [x] Return the current node.
4. [ ] If the value to delete equals the current node's value, we've found the node to delete:
    1. [x] If there is no right child, return the left child. This bypasses the current node, effectively deleting it.
    2. [x] If there is no left child, return the right child, accomplishing the same thing.
    3. [ ] If there are both left and right children:
        1. [ ] Start at the right child.
        2. [ ] Walk left until you find the smallest node in that right subtree. This is the next-largest value after the current node's value.
        3. [ ] Copy the next largest _value_ into the current node's _value_.
        4. [ ] Delete the successor value from the right subtree by calling delete on it, and save the returned node as the new right child.
        5. [ ] Return the current node.


# Deletion Review

The `delete` method is `O(log(n))` because, like most binary tree operations, we _don't_ have to search the entire tree. We only have to search _one path_ from the root to the leaf node we want to delete.

The depth of the tree on average is equal to `log base 2` of the number of nodes in the tree. For example:

|Nodes|Depth|
|---|---|
|1|0|
|2|1|
|4|2|
|8|3|
|16|4|
|32|5|
|64|6|
|128|7|
|256|8|
|512|9|
|1024|10|
|2048|11|
|4096|12|

**We only need to use ~10 steps to delete a node from a tree of ~1000 nodes**.