# Longest-Path-with-Limited-Jumps

Description
This project solves the problem of finding the longest path in an undirected, weighted graph with a restriction on the number of jumps (edges) that can be traversed. The goal is to calculate the longest possible path from node 1 to any other node, given a maximum number of allowed jumps (edges).

The graph is represented as an adjacency list, where each edge has a weight. The solution uses a combination of Dynamic Programming (DP) and Priority Queue (max-heap) to efficiently explore all possible paths while respecting the jump constraint.

Approach
Key Concepts:
Priority Queue: A max-heap is used to explore nodes in the order of the longest distance, ensuring that the most promising paths are explored first.

Dynamic Programming (DP): A DP table is used to store the longest path distance for each node, considering each possible number of jumps (from 0 to K).

Relaxation: For each node, we explore its neighbors and update the DP table with the new maximum distances that can be reached by traversing an edge.

Algorithm:
Graph Representation: The graph is represented using an adjacency list. Each edge is bidirectional (since the graph is undirected).

DP Table: A table dp[node][jumps] holds the maximum distance to node using exactly jumps edges. The table is initialized with -1 to indicate unvisited nodes.

Priority Queue: A priority queue is used to process nodes in the order of their longest distance, ensuring that we explore the most promising paths first.

Edge Relaxation: For each edge, the DP table is updated with the maximum distance, and the priority queue is updated accordingly.

Final Result: After processing all nodes, the longest path is found by inspecting the DP table for each node, considering all possible jumps (0 to K).

Requirements
Java 8 or higher

A basic understanding of graph traversal algorithms (Dijkstra's, Priority Queue, Dynamic Programming)


How to Run

1. Clone this repository:
Command is :   git clone https://github.com/your-username/longest-path-with-limited-jumps.git
cd longest-path-with-limited-jumps

2. Compile and run the Java code:
Command is: javac LongestPathWithLimitedJumps.java
            java LongestPathWithLimitedJumps

