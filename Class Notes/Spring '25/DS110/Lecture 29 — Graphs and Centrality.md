__Graph__: Consists of things (vertices) and connections between those things (edges)
- __Directed__: Connections are asymmetric
- __Undirected__: Connections are symmetric

__A graph G consists of__:
- A set of vertices of vertices V (nodes)
- A set of edges (E)

__The number of vertices/edges is referred to as__: |V| and |E|

__In an undirected graph, the edges are __ and __ are drawn__: Two element subsets of V {u, v}, No arrows

__In a directed graph, the edges are __ and __ are drawn__: Ordered pairs of vertices, Arrows

__The degree of a vertex is__: The number of edges it touches

__Path__: A sequence of vertices that lead from A to B

__Cycle__: A path from a vertex to itself that contains at least one other vertex and doesn't repeat other vertices

__Graphs can be represented as__
- Adjacency Matrices
- Adjacency Lists

__Adjacency Matrix__: A |V| x |V| array that is 1 at u, v if fthere is an edge from u to v, otherwise 0
>*Good for checking whether arbitrary edges exist, but a lot of memory spend on 0's for edges that don't exist.*


__Adjacency List__: |V| lists of vertices, where each list contains the vertices of a particular vertex has an edge to (In Python it can be a dictionary of lists)
>*Good for retrieving full neighbor lists quickly — no time wasted on non-existing edges*
## Centrality
__Centrality__: Can be measured through degree, closeness, and betweenness algorithms
### Degree
__Degree Centrality__: The number of neighbors of the vertex
### Closeness
__Closeness Centrality__: The inverse of the average number of steps in a closest path to each other node
$$
C(x) = \frac{|V| - 1}{\sum_yd(y,x)}
$$
where:
- |V| - 1 is a count of all the other nodes besides x
- d(y, x) is a shortest path distance

### Betweenness
__Betweenness Centrality__: Finds nodes that connect one community to another as the sum over start and end locations of proportion of shortest paths that pass through it
$$
\sum_{s≠v≠t} \frac{\sigma_{svt}}{\sigma_{st}}
$$
where:
- sigma_svt is a count of the shortest paths from s to t to v
- sigma_st is a count of shortest pasths from s to t

## Finding Shortest Paths
__The two fundamental algorithms for finding a path from one node to another on an unweighted graph are__: Breadth-first and depth-first searches

### Breadth-First Search
__Breadth-first Search__: Visit all nodes one step away, then all nodes two steps away, and so forth

__For BFS, you can build__:
- A tree, where the nodes at depth *i* are *i* hops away from the start using a shortest path
- A queue, where new elements go to the end of the line

__Steps for BFS with a queue__:
1. Add start node s to the queue of nodes to explore
2. Initialize discovered set, tracking which nodes have been seen before, to s
3. Create empty parent table (acts as tree, lets us remember how to get there)
4. While the queue of nodes to explore is not empty:
	1. Remove the node p from the front of the queue
	2. For each neighbor n of p
		1. If n is not in the discovered set
			1. Add p as n's parent in parent table
			2. If n is the target t, return the path to t (following parent table from t back to s)
			3. Add n to the end of the queue and add to "discovered" set
5. Return "no path"

