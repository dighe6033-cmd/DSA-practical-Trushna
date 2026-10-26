## Algorithm:

Step 1: Start the program.

Step 2: Enter the number of vertices and edges in the graph.

Step 3: Create an adjacency list to represent the graph.

Step 4: Enter the edges connecting the vertices.

Step 5: Accept the starting vertex from the user.

Step 6: Initialize all vertices as unvisited and set their BFS levels to -1.

Step 7: Mark the starting vertex as visited, set its level to 0, and insert it into the queue.

Step 8: Repeat the following steps until the queue becomes empty:

Remove the front vertex from the queue.

Display the vertex in the BFS traversal order.

Visit all its unvisited neighbouring vertices.

Mark each neighbour as visited.

Set the neighbour's level to one more than the current vertex's level.

Insert each neighbour into the queue.

Step 9: Display the BFS traversal order and the BFS level of each reachable vertex.

Step 10: Count and display the total number of reachable vertices.

Step 11: Display all unvisited vertices.

Step 12: Stop the program.
