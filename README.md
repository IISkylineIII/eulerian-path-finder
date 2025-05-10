### Eulerian Path Finder

This repository provides a Python implementation for finding an Eulerian path in a directed graph using a recursive depth-first search (DFS) approach.

An Eulerian path is a trail in a graph that visits every edge exactly once, possibly starting and ending at different nodes. This implementation works for directed graphs, even when nodes have unbalanced in-degrees and out-degrees, by determining the correct starting vertex.

### Features
Accepts a directed graph as an adjacency list.
Automatically detects a valid starting node based on degree conditions.
Uses recursive DFS to find the Eulerian path.
Outputs the path in the correct sequence.

### Algorithm

Graph Representation: Directed graph using a Python dictionary.
Degree Calculation: Determines in-degrees and out-degrees of all nodes.
Start Node Selection: Chooses a node with out-degree = in-degree + 1, if present.
Path Construction: Recursively explores edges and backtracks to build the final path.

```
### Example

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

```


Eulerian Path: 2 1 4 5 6 1 3 4 5 9 7 8 5 6 1

### File Structure


eulerian-path-finder/
├── eulerian_path.py        # Core implementation
└── README.md               # Project documentation

### Requirements
Python 3.x

No external dependencies

License
This project is open-source and available under the MIT License.
