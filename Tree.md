[Trees](https://en.wikipedia.org/wiki/Tree_\(abstract_data_type\)) are a widely used [[Data Structure]]s that simulate a hierarchical... well... _tree_ structure. That said, they're typically drawn upside down - the "root" node is at the top, and the "leaves" are at the bottom.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/lvDMp11-424x490.png)

Trees are kind of like linked lists in the sense that the root node simply holds references to its child nodes, which in turn hold references to their children, but Tree's nodes can have _multiple_ children instead of just one. A generic tree structure has the following rules:

- Each node has a value and _may_ have a list of "children"
- Children can only have a single "parent"

## Linked List

```
node -> node -> node
```
## Tree

_Drawn from left to right in this case:_

```
         > node
      > node
   > node
> node
         > node
      > node
         > node
      > node
   > node
      > node
```