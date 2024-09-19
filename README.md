# Homework 04 - Yujin 
<p align="center">
<img width="623" alt="Dijkstra's shortest path algorithm" src="https://github.com/user-attachments/assets/01ca5c7c-28c5-4930-9430-3184f5670694">
</p>

This project is a `Python package` that implements Dijkstra's shortest path algorithm among other graph-related algorithms. 

This package is designed to work with graph data structures and compute shortest paths between nodes efficiently.

## Features

- **Dijkstra's Algorithm**: Computes the shortest path from a source node to all other nodes.
- Extendable for other graph algorithms in the future.

## Installation

To install this package, follow these steps:

1. Create a virtual environment and activate it:

```
python3 -m venv venv
source venv/bin/activate
```

2. Install the package from PyPi:

```
pip install graphs-yujin-k9
```

3. After installing the package, you can test it by creating a test.py file in the directory outside of the venv folder with the following code:

```python
from graphs_yujin_k9 import sp

graph = {
    0: {1: 4, 7: 8},
    1: {0: 4, 2: 8, 7: 11},
    2: {1: 8, 3: 7, 8: 2},
    3: {2: 7, 4: 9, 5: 14},
    4: {3: 9, 5: 10},
    5: {3: 14, 4: 10, 6: 2},
    6: {5: 2, 7: 1, 8: 6},
    7: {0: 8, 1: 11, 6: 1, 8: 7},
    8: {2: 2, 6: 6, 7: 7}
}

s = 0  
dist, path = sp.dijkstra(graph, s)
print(f'Shortest distances from {s}:')
print(dist)
for d in path:
    print(f'Shortest path to {d}: {path[d]}')
```

4. Run the test file:

```
python test.py
```

## Sample Output

```
Shortest distances from 0:
[0, 4, 12, 19, 21, 11, 9, 8, 14]
Shortest path to 0: []
Shortest path to 1: [0]
Shortest path to 7: [0]
Shortest path to 2: [0, 1]
Shortest path to 6: [0, 7]
Shortest path to 8: [0, 1, 2]
Shortest path to 5: [0, 7, 6]
Shortest path to 3: [0, 1, 2]
Shortest path to 4: [0, 7, 6, 5]
```
