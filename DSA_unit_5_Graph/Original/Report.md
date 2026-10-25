## Problem Statement:

Develop a C++ program to represent bus stops as vertices and direct bus routes as edges in a graph. 

Apply Breadth First Search (BFS) from a selected bus stop, display the traversal order, and count the number of stops reachable from the starting stop.

## Approach:

The bus route system is represented using a graph, where bus stops are vertices and direct bus routes are edges. 

An adjacency list is used to store the connections between bus stops.

The Breadth First Search (BFS) algorithm is implemented using a queue to traverse the graph from the selected starting bus stop.

A visited array is used to avoid visiting the same stop multiple times.

During traversal, each visited stop is displayed, and a counter is maintained to calculate the total number of reachable stops, including the starting stop.

## Complexity:

Time Complexity: O(V + E)

Where:

V = Number of bus stops (vertices).

E = Number of direct bus routes (edges).

BFS visits each reachable vertex and examines its outgoing edges.

Space Complexity: O(V + E)

The adjacency list stores the graph, while the visited array and queue require additional space proportional to the number of vertices.

## Conclusion:

The C++ program successfully represents bus stops and direct bus routes using a graph and applies BFS to traverse the connected stops.

It displays the traversal order and counts the number of reachable stops from the selected starting point.

This experiment helps understand graph representation, BFS traversal, and their applications in transportation systems.
