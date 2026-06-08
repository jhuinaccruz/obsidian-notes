__Graph-Search Algorithms__: Used to explore graphs, determine whether two nodes are connected or some other properties regarding the ordered structure of a directed graph

__Depth-First Search__ (DFS): A graph search algorithm that "shoots" as far away from a node as possible to see if it results in a successful path, otherwise turning around
- `previsit(v)`: Assigns a vertex a time `i` when the vertex is pushed onto the stack
- `postvisit(v)`: Assigns a vertex a time `i` when the vertex is popped off the stack

__Graph `G` can be partitioned into four different edge types__:
- *Tree edges*: When `v` is an unvisited neighbor of `u`
	- This is the edge that builds the actual tree in DFS
- *Back Edge*: When `v` is an ancestor of `u`
	- This occurs when a cycle is made in a tree
- *Forward Edge*: When `v` is a descendant of `u`, but not explicitly its child
- *Cross Edge*: When `v` is neither an ancestor nor a descendant of `u`
	- Occurs when two nodes are connected from separate branches or different trees

__Cycle__:
- In an undirected graph, it is a sequence of at least 3 different vertices that are connected where `v1` and `vk` are connected by an edge
- In a directed graph, it is a sequence of at least 2 different vertices that are connected where `v1` and `vk` are connected by an edge