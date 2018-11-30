# Graph

In the case of adjacency lists, a graph is a dynamic array of vertex values, each paired with a corresponding dynamic array of edges. Vertices are points on graphs with stored variables. Vertices can be connected to any other vertices in the same graph by edges.

# In Memory

In memory, a graph looks like this:

![Image of Graph in Memory](images/graph_memory.png)

\[description of diagram\]

# Operations

A \[widget\] supports the following operations:

* **Add Vertex** puts a new vertex variable as well as a new, corresponding, dynamic array for edges at the end of the adjacency list. This happens in O(1) constant time because there is a pointer stored that leads the operation straight to the end of the adjacency list.
* **Add Edge** makes two additions to vertex edge arrays. Each of the two verticies selected to be connected will have the value of the other vertex stored in their own edge array. This happens in O(n) linear time because even though the two vertex arrays have pointers for their first open spaces, the operation still must search through the main adjacency list to find the two verticies.
* **Remove Vertex** goes through an adjacency list to find the specified vertex, then deletes it and its edge array, forcing the following data in the adjacency list to move over. Searching through the adjacency list and moving an arbitrary amount of the graph's data gives this operation an O(n) linear complexity.
* **Remove Edge** goes through an adjacency list to find the verticies of the specified edge. It then goes through each of these verticies' edge arrays to find the two values creating the edge and deletes them, often forcing data in each of the two edge arrays to move over and fill in the gap. Because of the searching and data moving that could go on for an arbitrary amount of time in this operation, the operation has a complexity of O(n).

# Use Cases

A graph is useful when data points need to have many different connections represented between them, as they are built with verticies and edges that are naturally able to connect each other.

Graphs are not helpful for handling collections of data points that have no need to be interconnected. Graphs do not have all the same operations as other data structures, so using one when it is not needed would be limiting the number of useful operations available for such a situation for no reason.

# Example

```
my_graph = graph()
my_graph.add_vertex('a')
my_graph.add_vertex('b')
my_graph.add_edge('a', 'b')
my_graph.remove_edge('a', 'b')
my_graph.remove_vertex('b')
```

(c) 2018 Amber Kolar. All rights reserved.