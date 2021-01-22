# Graphs

## Vocabulary

  - Vertex - A vertex, also called a "node", is a data object that can have zero or more adjacent vertices

  - Edge - an edge is a connection between two nodes

  - Neighbor - the neighbors of a node are its adjacent nodes. they are connected via an edge.

  - Degree - the degree of a vertex is the number of edges connected to that vertex 

## What is it?

  - A non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

## Directed vs Undirected

### Undirected Graphs

Is a graph where each edge is undirected or bi-directional. It does not move in any direction.

    Undirected graph:
    a--c--b
    |  |  |
    d--e--f

    6 vertices and 7 undirected edges

    vertices/nodes: {a,b,c,d,e,f}
    edges: {(a,b), (a,d), (b,c), (b,f), (c,e), (d,e), (e,f)}

### Directed Graphs (Digraph)

a graph where every edge is directed. each node is directed at another node with a specific requirement of what node should be referenced next

    Directed Graph:
    a --→ c ←-- b
    ↑     ↑     |
    |     |     |
    |     ↓     ↓
    d --→ e --→ f   

    6 vertices and 8 edges

    vertices: {a,b,c,d,e,f}
    edges: {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}

## Complete vs Connected vs Disconnected

### Complete Graphs

A complete graph is when all nodes are connected to all other nodes.

### Connected

All vertices/nodes have at least one edge.
  -  A Tree is a form of a connected graph

### Disconnected

some vertices may not have edges
  - It is complelty possible to have standalone nodes or edges (also known as islands) in a graph data structure.

## Acyclic vs Cyclic

### Acyclic Graph

a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.
  - A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

### Cyclic Graphs

A Cyclic graph is a graph that has cycles

A cycle is defined as a path of a positive length that starts and ends at the same vertex.