__Kinds of Binary Trees__:
- Full: Every node has either 0 or 2 children
- Complete: All levels filled (leave's parents can be empty, as long as all the leftmost parents are filled)
- Perfect: All internal nodes have two children, all have leaves at the same depth

__Binary Search Tree__: A binary tree with an additional property: For every parent node, the left node (and its resulting subtree) are less than the parent, and the left node and its subtree's values are greater than the parent's
- This specific property allows for binary search
- Insertion: Creates a new node if the tree is empty, otherwise traverses through the tree left/right until it finds an empty space
- Finding minimum: Traverses the tree left until finding the lowest leftmost value
- Finding maximum: Traverses the tree right until finding the lowest rightmost value
- Deletion: Removes the node if its a leaf, replaces it with its child otherwise.
	- If it has two children, gets the smallest value in right subtree and replace it with that
- Insertion, deletion, min/max, and search functions all operate at `O(log n)`

__Binary Search__: 
- Time: `O(height)` (`O(log n)` if the tree is balanced)
- Space: `O(1)`

__Unbalanced Binary Search Tree__: Happens when inputting sorted data, such that its operations become `O(n)`

__B-Trees__: Guarantee `O(log n)` operations