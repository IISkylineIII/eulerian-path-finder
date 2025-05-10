Eulerian Path Finder
This repository provides a Python implementation to find an Eulerian path in a directed graph using recursive depth-first search (DFS).

An Eulerian path is a trail in a finite graph that visits every edge exactly once (but not necessarily every vertex) and starts and ends at different vertices if necessary. This implementation handles unbalanced graphs by identifying an appropriate starting point based on in-degree and out-degree differences.

Algorithm Overview
The graph is represented as an adjacency list (dict[int, list[int]]).

The algorithm calculates in-degrees and out-degrees for each node to determine a valid starting vertex.

A recursive DFS explores all edges, storing the result in reverse order.

Finally, the path is reversed to produce the correct Eulerian path.

Example Usage: 
graph_input = {
    1: [3, 4],
    2: [1],
    4: [5],
    5: [6, 9],
    6: [1],
    7: [8],
    8: [5],
    9: [7],
}

eulerian_path = find_eulerian_path(graph_input)
print("Eulerian Path:", " ".join(map(str, eulerian_path)))

Output:

Eulerian Path: 2 1 3 4 5 6 1 4 5 9 7 8 5 6 1
Requirements
No external dependencies — works with standard Python 3 (collections.defaultdict is used).

📂 Files
eulerian_path.py: Core script to construct and find Eulerian paths.

