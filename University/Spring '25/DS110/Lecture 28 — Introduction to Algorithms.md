__Algorithm__: Any well defined computational procedure that takes some value(s) ans input and produces some value(s) as output
>*A good algorithm produces the best possible output and avoids excess computation or use of memory*

__Main criteria for an algorithm__;
- Is it correct (always producing a valid output)?
- Is it asymptotically fast (running time scales well with input size)?
- Is it optimal (produces the best solution)?
- Does its memory use grow reasonably with the size of the input?

## Array Sorting
### Insertion
>Insertion sort works from left to right, taking an item and moving to the left until the item to its left is smaller or tied. This creates a growing "sorted region" on the left hand side that eventually covers the whole array

__The best case for insertion sort is__: The array is already sorted, resulting in a linear time for the algorithm

__The worst case for insertion sort is__: The array is in reverse order, resulting in a quadratic time for the algorithm

### Mergesort
>Mergesort divides an array in two, sorting each half recursively and merges the sorted lists

__There are two main functions working for mergesort__:
- merge()
- mergesort()

__merge() has a __ time operation__: Linear, every round a constant amount c of work is done (with one comparison)

__mergesort() has a constant __ time operation__: Logarithmic, as drawing a tree of the operations used has log_2N levels, where each level of the tree sums to the same value N, resulting in the runtime of Nlog_2N

