__Graph__: A collection of nodes (vertices) connected by edges
- Vertex: A node
- Edge: Connection between vertices
- Neighbors: A measure of adjacency between nodes
- Degree: Number of neighbors
- Path: Sequence of vertices connected by edges
- Cycle: Path that starts and ends at the same vertex
- Undirected: Edges that have no direction
- Directed: Edges with direction
- Unweighted: All edges have the same value
- Weighted: Edges have different values

__Adjacency List__: For each vertex, store a list of neighbors

__Adjacency Matrix__: In a square grid where `matrix[i][j]`≠ 0 if an edge between i and j exists

__Breadth First Search__: Explores a graph by level with a queue
- Uses include finding shortest path in an unweighted graph, find connected nodes, test for bipartiteness, and for social networks
- Time: `O(V + E)`
- Space: `O(V)`

```text
FUNCTION SimpleBFS(Graph G, StartVertex s):
    
    // 1. Setup: Use a set to track visited nodes to prevent cycles
    SET Visited
    ADD s TO Visited
    
    // 2. Setup Queue (FIFO)
    Queue Q
    ENQUEUE(Q, s)
    
    // 3. Main Traversal Loop
    WHILE Q IS NOT EMPTY:
        u = DEQUEUE(Q)
        
        // Process the current node (u) here
        // e.g., print(u) or check if it is the target node
        
        // Explore all neighbors of u
        FOR EACH neighbor v IN G.Neighbors(u):
            IF v IS NOT IN Visited:
                ADD v TO Visited
                ENQUEUE(Q, v)

END FUNCTION
```

__Depth-First Search__: Explores a graph by its branches with a stack
- Uses include finding paths and connected nodes, testing for cycles, topological sorting, and solving puzzles
```text
FUNCTION IterativeDFS(Graph G, StartVertex s):
    
    // 1. Setup
    SET Visited
    Stack S
    
    PUSH(S, s)
    ADD s TO Visited
    
    // 2. Main Traversal Loop
    WHILE S IS NOT EMPTY:
        u = POP(S)
        
        // Process the current node (u) here
        // e.g., print(u)
        
        // Explore neighbors
        // Note: For deterministic output, iterate neighbors in a specific order
        FOR EACH neighbor v IN G.Neighbors(u):
            IF v IS NOT IN Visited:
                ADD v TO Visited
                PUSH(S, v)

END FUNCTION
```