Merge sort is a [recursive](https://en.wikipedia.org/wiki/Recursion) sorting algorithm and it's quite a bit faster than bubble sort. It's a [divide and conquer algorithm.](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm):

- **Divide**: divide the large problem into smaller problems, and recursively solve the smaller problems
- **Conquer**: Combine the results of the smaller problems to solve the large problem

In merge sort we:

- Divide the array into two (equal) halves (divide)
- Recursively sort the two halves
- Merge the two halves to form a sorted array (conquer)

Click to hide video

## Algorithm

The algorithm consists of two separate functions, `merge_sort()` and `merge()`.

`merge_sort()` divides the input array into two halves, calls itself on each half, and then merges the two sorted halves back together in order.

The `merge()` function merges two already sorted lists back into a single sorted list. At the lowest level of recursion, the two "sorted" lists will each only have one element. Those single element lists will be merged into a sorted list of length two, and we can build from there.

_In other words, all the "real" sorting happens in the `merge()` function._

### merge_sort() pseudocode

Input: `A`, an unsorted list of integers

1. If the length of `A` is less than `2`, it's already sorted so return it
2. Split the input array into two halves down the middle
3. Call `merge_sort()` twice, once on each half
4. Return the result of calling merge(`sorted_left_side`, `sorted_right_side`) on the results of the `merge_sort()` calls

### merge() pseudocode

Inputs: `A` and `B`. Two sorted lists of integers

1. Create a new `final` list of integers.
2. Set `i` and `j` equal to zero. They will be used to keep track of indexes in the input lists (`A` and `B`).
3. Use a loop to compare the current elements of `A` and `B`:
    - While `i < len(A)` and `j < len(B)`, compare `A[i]` and `B[j]`.
    - Append the smaller value to `final`.
    - Increment the index for the list you just took from.
    - Stop when either list is exhausted.
4. After comparing all the items, there may be some items left over in either `A` or `B`. Add those extra items to the final list.
5. Return the final list.

## Assignment

Our LockedIn influencers are complaining that when they sort their followers by follower count, it gets really slow if they have more than `1,000` followers (because we're using Bubble Sort). Let's speed it up for them with merge sort.

Complete the `merge_sort` and `merge` functions according to the described algorithms.