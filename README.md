# Assignment 3: Optimization of a City Transportation Network (Minimum Spanning Tree)

## Project Overview

This project implements Prim’s and Kruskal’s algorithms to determine the Minimum Spanning Tree (MST) of a weighted graph. The idea is inspired by a real-world scenario where a city aims to connect all its districts with roads in the most cost-effective way.

## Implementation Details

### Kruskal's Algorithm:

#### Data Structure for Union-Find (DSU):

- The DSU (Disjoint Set Union) data structure is used to track connected components of the graph to avoid cycles. Each node has a parent, and the components are merged using union by rank.

#### Edge Sorting:

- The edges of the graph are sorted in ascending order of weight. Kruskal's algorithm adds edges to the MST starting with the lightest ones, ensuring the tree has the minimum possible weight.

#### Disconnection Check:

- After adding edges to the MST, the algorithm checks if the number of edges is less than V-1 (where V is the number of vertices). If so, the graph is disconnected, and a warning is printed.

### Prim's Algorithm:

#### Priority Queue for Edge Selection:

- A priority queue is used to select the edge with the minimum weight at each step. This ensures the greedy nature of Prim's algorithm, selecting the smallest possible edge at every step, thus constructing the minimum spanning tree.

#### Adjacency List Traversal:

- The algorithm uses an adjacency list to represent the graph. As each new node is added to the MST, all its adjacent edges are checked, and those leading to unvisited nodes are added to the priority queue.

#### Disconnection Check:

- If the number of edges in the MST is less than V-1, the graph is considered disconnected, and a warning is printed, indicating that the MST is incomplete.

#### MSTResult (Common Class for Both Algorithms):

### Storing Results:

- The MSTResult includes the list of edges that form the minimum spanning tree, the total cost of these edges, and the number of operations performed during the process.

### Operations Counting:

- Both algorithms track the number of operations, such as unions (for Kruskal) and edge extractions (for Prim), which helps evaluate the efficiency of each algorithm.

### Execution Time:

- The execution time of the algorithm is measured in milliseconds, which is crucial for performance analysis.
