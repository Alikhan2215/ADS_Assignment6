# ADS_Assignment6
## Vertex class

The Vertex class represents a vertex in a graph. Each vertex contains a piece of data of type V and maintains a map of its adjacent vertices with corresponding edge weights.

**Constructors**

- **Vertex(V data):** *Constructs a new vertex with the given data.*

**Methods**

- **addAdjacentVertex(Vertex<V> destination, double weight):** *Adds an adjacent vertex with the specified destination and edge weight to the current vertex.*
- **getData():** *Returns the data associated with the vertex.*
- **getAdjacentVertices():** *Returns a map of adjacent vertices with their corresponding edge weights.*
- **toString():** *Returns a string representation of the vertex.*


## WeightedGraph class
  
The WeightedGraph class represents a weighted graph data structure, where each vertex is associated with a piece of data of type V. This implementation allows the addition of vertices, the creation of weighted edges between vertices, and provides methods to retrieve adjacent vertices and all vertices in the graph.

**Constructors**
  
- **WeightedGraph():** *Constructs an empty weighted graph.*
  
**Methods**
  
- **addVertex(Vertex<V> vertex):** *Adds a vertex to the graph.*
- **addEdge(Vertex<V> source, Vertex<V> destination, double weight):** *Adds a weighted edge between the source and destination vertices with the specified weight.*
- **getAdjacentVertices(Vertex<V> vertex):** *Returns a list of adjacent vertices of the given vertex.*
- **getAllVertices():** *Returns a set of all vertices in the graph.*
  
  
## BFS class
The BreadthFirstSearch class implements the breadth-first search algorithm for a weighted graph. It performs a breadth-first traversal from a given source vertex to discover all reachable vertices in the graph, following the rules of breadth-first search.

**Methods**
- **search(WeightedGraph<V> graph, Vertex<V> source, Vertex<V> destination):** *Performs a breadth-first search on the specified weighted graph, starting from the source vertex and stopping at the destination vertex. It returns a list of vertices visited during the traversal.*


## DijkstraSearch class
The DijkstraSearch class implements the Dijkstra's algorithm for finding the shortest path in a weighted graph from a given source vertex to a destination vertex. It calculates the shortest distance from the source vertex to all other vertices in the graph, taking into account the weights of the edges.

**Methods**
- **search(WeightedGraph<V> graph, Vertex<V> source, Vertex<V> destination):** *Performs Dijkstra's algorithm on the specified weighted graph, starting from the source vertex and stopping at the destination vertex (if specified). It returns a list of vertices that form the shortest path from the source to the destination (if a path exists).*


## Search interface

The Search interface defines the contract for classes that implement graph search algorithms in a weighted graph. It provides a method for performing a search operation in the graph to find a path between a source vertex and a destination vertex.

**Methods**
- **search(WeightedGraph<V> graph, Vertex<V> source, Vertex<V> destination):** *Performs a search operation on the specified weighted graph, starting from the source vertex and stopping at the destination vertex (if specified). It returns a list of vertices that form the path from the source to the destination (if a path exists).*
