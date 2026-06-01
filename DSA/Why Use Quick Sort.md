Pros:

- **Very fast**: At least it is in the average case
- **In-Place**: Saves on memory, doesn't need to do a lot of copying and allocating

Cons:

- **Typically unstable**: changes the relative order of elements with equal keys
- **Recursive**: can incur a performance penalty in some implementations
- **Pivot sensitivity**: if the pivot is poorly chosen, it can lead to poor performance

All this said, quicksort is widely used in the real world because the trade-offs are often worth it. For example, it's a [default in PostgreSQL](https://airbyte.com/blog/postgresql-query-plans-for-sorting-data#:~:text=few%20different%20algorithms.-,Quicksort,-This%20is%20the), a popular open-source database.

I'd also like to shoutout [Timsort](https://en.wikipedia.org/wiki/Timsort), a hybrid of merge sort and insertion sort that was Python's default from version 2.3 to 3.10. As of Python 3.11, it's been replaced by Powersort, which makes _small but meaningful_ improvements.