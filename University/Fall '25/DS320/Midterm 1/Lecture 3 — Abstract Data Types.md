__Linked List__: Can be separated into two types, where their operations take at most *O(n)* time
- __Singly-Linked List__: Has pointer to the first element of a list, and one pointing to the next
- __Doubly-Linked LIst__: Has a pointer to the first element of a list, one pointing to the next, and one pointing to the previous one

__Queues__: A kind of First-In, First Out linked list with methods;
- `enqueue(q,x)`: Insert element x to the back of a queue `q`
- `dequeue(q)`: Delete the element at the front of the queue `q` and returns it

__Stack__: A kind of Last-In, First-Out linked list with methods;
- `push(s,x)`: Insert element `x` to the top of stack `s`
- `pop(s)`: Deletes the topmost element of the stack and returns it

__Graph__: A directed graph `G = (V,E)` is defined by:
- A set of vertices `V`
- A set of ordered edges `E` as a subset of `V x V`

__Directed Edge__: An ordered pair of vertices `(u, v)` usually indicated by a line between `u` and `v` with an arrow pointing towards `v`

__Undirected Edge__: An unordered pair of vertices `{u, v}` usually indicated by a line between `u` and `v`

>[!important]
>*Some conventions:*
>- *We will refer to the number of vertices (or the size of the vertex set |V|) as n.*
>- *We will refer to the number of edges (or the size of the edge set |E|) as m.*
>- *Often we will simply name the vertices `V = {1, . . . , n}` so an edge `(i, j)` is an edge from the `i`th vertex to the `j`th vertex.*
>- *You may also hear vertices referred to as “nodes” or edges referred to as “arcs.”*

__Adjacency__ (neighbors): Defined as
$$
(i, j) \in E
$$
- In directed graphs, can be explicitly referred as out-neighbors, where
$$
j : (i, j) \in E
$$
	... or as in-neighbors, where
$$
J : (j, i) \in E
$$
where
- `(i, j)` is an edge
- `E` is a set of ordered edges

__Vertex Degree__: The number of neighbors a vertex has, defined as
$$
(d_v = |\{u : v, u\}|
$$
where:
- d_v is the degree of a vertex
- |{u: v, u}| is the number of neighbors for all `u` related to `v`

__Path__: Defined as a sequence of edges
$$
e_1, e_2, ... e_k.\ e_1 = (u, v_1), e_i = (v_{i - 1}, v_i)\ \forall\ i \in \{2,..., k-1\}\\,\ e_k = (v_{k - 1}, w)
$$
where:
- The first edge (e_1) starts at u
- The last edge  (e_k) ends at w
- Each proceeding edge (e_i) ends where the next edge starts

__Connectedness__: A pair of vertices is connected when a path exists between them

## Abstract Data Types for Graphs

__There are two main ways of representing graphs__:
- Adjacency Matrices
- Adjacency Lists

__Adjacency Matrix__: Represented as;
$$
A(G): |A| = n * n, A_{ij} = 1 \iff (i, j) \in E
$$
where:
- `A(G)` is the matrix representing graph `G`
	- The graph is a square binary matrix of dimensions `n^2` or `|V|^2` 


__Adjacency Matrix Uses__:
- Useful when looking up a specific edge at `A_ij` (*O(1)*)
- Least useful when considering;
	- *Space*: Since its size will always be `n*n`, regardless of `m`
		- Wasteful when `m` is small
	- *Listing `i`'s edges*: Will at minimum be *Ω(n)*
		- Wasteful when `i` is small

__Adjacency List__: Represented as;
$$
A(G): |A| = n. j \in A[i] \iff (i, j) \in E
$$
where:
- `A(G)` is a one dimensional array
	- The array is of length n
	- The `i`th entry in `A` contains a linked list of `i`'s neighbors

__Adjacency List Uses__:
- Useful when considering
	- *Listing `i`'s edges*: Results in *O(d_i)* which can be simplified to O(1) per neighbor
	- *Space*: Results in an array of *O(n+m)*
- Least useful when looking up a specific edge `(i, j)`
	- Said procedure takes O(d_i), which simplifies to O(n)

