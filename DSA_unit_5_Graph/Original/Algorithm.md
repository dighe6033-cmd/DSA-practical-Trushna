## Algorithm:

Step 1: Start the program.

Step 2: Read the number of bus stops and the number of direct bus routes.

Step 3: Represent each bus stop as a vertex and each direct bus route as an edge using an adjacency list.

Step 4: Read the bus routes and store them in the graph.

Step 5: Select the starting bus stop.

Step 6: Initialize all bus stops as unvisited.

Step 7: Insert the starting bus stop into a queue and mark it as visited.

Step 8: Repeat the following steps until the queue becomes empty:

Remove the front bus stop from the queue.

Display the bus stop.

Increase the reachable stop count.

Visit all its unvisited neighbouring bus stops.

Mark each neighbour as visited and insert it into the queue.

Step 9: Display the BFS traversal order and the total number of reachable stops, including the starting stop.

Step 10: Stop the program
