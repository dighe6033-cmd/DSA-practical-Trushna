## Problem Statement:

Develop a C++ program to perform Breadth First Search (BFS) on a graph.

Accept a starting vertex and display the BFS traversal order.

Identify the vertices reachable from the starting vertex, display the unvisited vertices, count the reachable vertices, and display their BFS levels.

## Approach:

The graph is represented using an adjacency list, where vertices represent nodes and edges represent connections between them. 

The BFS algorithm is implemented using a queue to traverse the graph from a user-selected starting vertex.

A visited array is used to avoid visiting the same vertex multiple times, while a level array stores the BFS level of each vertex.

The starting vertex is assigned level 0, and its neighbouring vertices are assigned level 1. 

The levels of other reachable vertices are calculated based on their distance from the starting vertex.

After completing the traversal, the program displays the BFS traversal order, the reachable vertices with their levels, the total number of reachable vertices, and the unvisited vertices.

## Complexity:

Time Complexity: O(V + E)

Where:

V = Number of vertices in the graph.

E = Number of edges in the graph.

BFS visits each reachable vertex and examines its adjacent edges.

Space Complexity: O(V + E)

The adjacency list requires O(V + E) space, while the visited array, level array, and queue require O(V) additional space.

## Conclusion:

The modified C++ program successfully implements BFS to traverse a graph from a user-selected starting vertex.

It displays the traversal order, identifies reachable and unvisited vertices, counts the reachable vertices, and determines the BFS level of each reachable vertex. This experiment helps in understanding graph traversal, vertex connectivity, and level-based exploration.

If you want, I can:
