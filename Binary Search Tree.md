[[Tree]]s aren't particularly useful [[Data Structure]]s unless they're _ordered_ in some way. One of the most common types of ordered tree is a [Binary Search Tree](https://en.wikipedia.org/wiki/Binary_search_tree) or `BST`.

A binary tree node has _at most_ 2 children. A `BST` adds a few more constraints:

1. The left child's value must be _less than_ its parent's value
2. The right child's value must be _greater than_ its parent's value
3. No two nodes in the `BST` can have the same value

By ordering the tree like this, we can traverse the tree to find the node we want much faster.