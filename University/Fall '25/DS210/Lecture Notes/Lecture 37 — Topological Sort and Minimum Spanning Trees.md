__Topological Sorting__: Given a directed acyclic graph, find an ordering of vertices such that for every edge `{u, v}`, `u` comes before `v`

__Spanning Tree__: A subgraph that
- Invdes all vertices
- Has no cycles (can be represented as a tree)
- Has exactly `V-1` edges

__Minimum Spanning Tree__: A tree with a minimum total edge weight
- Multiple MSTs can exist with the same weight
- Used in network design, approximation algorithms, clustering, and image segmentation

__Kruskal's Algorithm__: Adds edges in order of increasing weight, skipping edges that can create cycles
- Time: `O(E log E)`
- Space: `O(V + E)`

__Prim's Algorithm__: Creates a minimum spanning tree from a starting vertex, always adding the cheapest edge to a new vertex using a priority queue
- Time: `O(E log E)`
- Space: `O(E)`
