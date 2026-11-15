---
Created: 10/13/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/14/26
State: "5"
Action: Study
---
__Disc Accessing__: The reading of a single block (or series of concurrent blocks as a page)
- The most time-consuming process due to the fact that seeking processes take the longest

__Index__ (Dictionary/Map): A structure that stores `key, value` pairings (as *items*)
- Allows for efficient access to a record
- Structures can be
	- __Clustered__ (Primary): Stores full records based on some primary key
		- Also called a heap file due to management similar to the heap
	- __Unclustered__ (Secondary): Enable for quick record retrieval of items within records

__B-Tree__: Search tree data structure characterized that functions like a binary search tree with multiple children per node
- *Definitions*:
	- *Order* (Height): $m$
	- *Nodes* (Leaves): At least $m$ and at most $2m$
		- For *internal nodes* (within its branches), at least $m+1$ and at most $2m+1$
		- Minima/Maxima ensure each block read gets *as much information as possible* while also ensuring information *does not exceed a given block*
		- Leaves and their pointers correspond to a specific page
	- *Root*: (Topmost node): As few as $1$ item
- Important Functions: Given an item with a key $k$
	- *Search*:
		1. Traverse through the root until you find an item that is greater than $k$
			- If $k$ is greatest, drop onto the n
	- *Insertion*:
		1. Search for $k$ through the tree until reaching a leaf node
			- If the leaf has less than $2m$ items, add item to the node
			- Otherwise, split the node
				1. Smallest $m$ items remain in the leaf
				2. Largest $m$ items drop down into a new leaf
				3. Middlemost item goes into previous leaf, acting as a pointer to the parent
	- *Deletion*: Given node $N$
		1. Search for the item and remove
			- If $N$ ends up with less than $m$ items:
				- If adjacent node has more than $m$ items, take some items and add it to $N$
				- Otherwise, merge with sibling
			- If $N$ is an internal node, do not remove it
				- Wait until the associated child node is merged later on
- Efficiency:
	- Traversal: $O(m + 1) \implies O(m)$ 
	- Search/Insertion: $O(\log_mn)$
- ==🟢Solves some of the deficiencies in Hash Tables==

__B+Tree__: Similar to B-Trees, except data items are only found in leaf nodes, and internal nodes contain keys and child pointers
- ==🟢Compared to B-Trees, B+Trees have more space for child pointers leading to shorter trees (and less disk read/writes)==

__Hashing__: Generalizes keys into integers, such that no matter the data type, the indices (keys) are all the same type
- __Hash Function__: Converts items into hash values (keys), ==🔵Denoted as some function $h(\text{item}) = k$==
- __Hash Table__: Index structure resulting from hashing items and their corresponding keys and pages
	- Stored as an array in memory
	- __Collision__: Two values hashed to the same value
		- Partially solved through buckets, but ==🔴must account for when the *bucket* is full==
	- *Efficiency*:
		- ==🟢Best==: $O(1)$
		- ==🔴Worst==: $O(k)$ where $k$ is the length of the largest bucket
	- ==🔴*Limitations*==:
		- Hard to create a reliable hash function
		- Unordered keys mean sorts and. range/rank searches are difficult
- __Static Hashing__: Number of buckets remains constant, instead relying on "overflow" buckets
	- ==🔴Overflow bucket access requires extra disk read==
- __Dynamic Hashing__: Number of buckets fluxuates as items increase and buckets fill
	- ==🔴Can result in large space expenses==
	- *Simple Approach*: Assuming keys are strings, take their length and use modulo to get a valid bucket number $$\text{bucket index} = h(k) \% \text{number of buckets}$$
		- If hash table fills up, *double the number of buckets and rehash all items*
- __Linear Hashing__: Hash value is a binary number read as $i$-rightmost bits and placed in its corresponding bucket $$\text{bucket index} = i = \text{ceiling}(log_2n)$$
	- If bucket index does not exist, *subtract by one*
	- *Important metadata*:
		- $n$: Number of buckets
		- $i$: Number of bits used to assign keys to buckets
		- $f$: Value of how full the buckets are
	- When $f$ is exceeded, add one more bucket, and update $n$ and $i$ as necessary
		- *Rehash the previous bucket index*

__Working Set__: Frequently accessed pages stored in cache

__Choosing an Index Structure__

| B/B+Tree                                                                                                 | Hash Table                          |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| Working set fits in memory                                                                               | Working set is large and spread out |
| Working set is local (queries result in searches close to each other) (e.g. rank/count/range operations) |                                     |
