The building blocks of a [[Binary Search Tree]] are _Nodes_. In our implementation, we will only use a single class, the `BSTNode` class. Any `BSTNode` is technically also a full Binary Search Tree, with itself as the root node (it's not aware of any potential parents). Most of the [[Method]]s that traverse the tree will do so [recursively](https://en.wikipedia.org/wiki/Recursion)... have fun!

## Our LockedIn `BSTNode`

Throughout this chapter we'll be building a binary search tree to power LockedIn's custom database. LockedIn's management doesn't trust so called "open-source"... _so here we are_. One of the primary features of databases is the ability to look up records by a single key, and binary search trees are the most common way to implement these fast lookups.

Each node in our BST will represent a LockedIn user. A `BSTNode` has three properties:

- `value`: The value of the node, a `User` object in our case (see `user.py`). You'll notice that `User`s have a name and an ID. Comparison operators are already implemented for you on the class, so you should be able to compare `User` objects with `==`, `<`, and `>` directly. The ID is the value that we'll use to determine the order of the nodes in the tree.
- `left`: The left child of the node, another `BSTNode` or `None`
- `right`: The right child of the node, another `BSTNode` or `None`

## Assignment

**Complete the `insert` method of the `BSTNode` class**. It takes a `User` object as input and adds it to a new node if the value doesn't already exist in the tree.

1. [ ] If the node doesn't have a value yet, store the given value and return
2. [ ] If the node's value is _equal_ to the given value, just return, no duplicates allowed
3. [ ] If the given value is less than the node's value and the node _doesn't_ have a `left` child, create a new `left` child node with the given value and return
4. [ ] If the given value is less than the node's value and the node _does_ have a `left` child, [recursively](https://realpython.com/python-thinking-recursively/) call `insert` off of that left child with the given value and return
5. [ ] Since we already checked if the given value is equal to or less than the node, the value must be greater than the node. Handle whether or not the node already has a `right` child

# Insert Review

Inserting into a binary search tree (like most of its operations) is _very_ fast. Picture the algorithm that you just wrote in your head: _how many comparisons does it take to find the right spot for a new node_?

It only requires one comparison for each _level_ of the tree, making it `O(log(n))`! (At least in a balanced tree, we'll talk about this later).

Order `log(n)` is _very_ fast - it's practically as good as `O(1)` in most cases. If our tree has `1,000,000` nodes, we only need to make `20` comparisons to find the right spot for a new node. If our tree is 2x larger (`2,000,000` nodes), we only need to make _one more comparison per insert_, `21` total.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/SzKm7OW-1263x635.png)

The average Big O complexity of the .insert method is O(log(n)).