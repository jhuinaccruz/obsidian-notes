__Priority Queue__: A data structure where each element is ordered by its "priority"

__Binary Heap__: Represented as a heap composed of nodes, such that
- The first node is the root node, with children but no parent
- Every node under it has a parent and child, except for the leaves towards the bottom (last nodes), which have no children
- A binary heap is a complete binary tree whose children are less than or equal to its parent on both sides
- Represented in an array by level
- __Push__:
	1. Add element to the end of the array (bottom-rightmost of the tree visually)
	2. Sift up the array if the parent is larger (min-heap) or smaller (max-heap)
- __Pop__:
	1. Replace the root node with the last element
	2. Sift down the array if the larger child is larger (max-heap) or smaller (min-heap) than the parent node

__Heap__ (Data structure): A property that dictates the parent nodes are the greatest/least its descendants

__Complete Tree__: All levels filled except the last, which is filled from left to right

__Heapsort__: Builds a heap from an array (`O(n)`) then iteratively removes the root and places it at the end of the array
- Time: `O(n log n)`
- Space: `O(n)`