Overview

This repository contains C++ implementations of two fundamental graph traversal algorithms:

Breadth-First Search (BFS)

Depth-First Search (DFS)

These algorithms are essential for exploring graphs and trees and are widely used in various applications, such as pathfinding, cycle detection, and network analysis.

Features

Implementation of BFS using a queue (iterative approach)

Implementation of DFS using both recursive and iterative methods

Support for both directed and undirected graphs

Input handling for adjacency list representation

Example test cases to demonstrate functionality

BFS Algorithm

Breadth-First Search (BFS) explores all nodes at the present depth level before moving on to nodes at the next depth level. It is implemented using a queue.

BFS Pseudocode

BFS(Graph, start):
    Create a queue and enqueue the start node
    Mark start node as visited
    While queue is not empty:
        Dequeue a node from the front
        Process the node
        Enqueue all unvisited adjacent nodes and mark them as visited

DFS Algorithm

Depth-First Search (DFS) explores as far as possible along each branch before backtracking. It can be implemented using recursion or an explicit stack.

DFS Pseudocode (Recursive)

DFS(Graph, node, visited):
    Mark node as visited
    Process the node
    For each adjacent unvisited node:
        Call DFS recursively on the adjacent node

DFS Pseudocode (Iterative)
