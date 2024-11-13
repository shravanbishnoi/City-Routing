# Optimal City Routing
This project demonstrates optimal routing techniques using graph traversal algorithms to find efficient paths between cities. Implementations include A-Star, Depth-First Search (DFS), Breadth-First Search (BFS), and Greedy Best-First Search. Additionally, a map API is used for distance calculations, and custom graph generation scripts create random connected graphs with selectively dropped edges.

## Project Structure
- Algorithms: Notebooks implementing A-Star, DFS, BFS, and Greedy Best-First Search algorithms.
- Distance Calculation: File using a map API to calculate distances between two cities.
- Random Graph Generation:
  - Graph.py: Contains the Graph class for graph creation, adding/removing edges, and generating random graphs.
  - Random Graph Notebook: Notebook for dropping edges to create random connected graphs.
- Data:
  - Datasets: CSV files containing city and route data.
  - Images: Graph visualizations generated from random graphs.

## Key Components
1. Graph Class (Graph.py)
The Graph class provides a custom implementation for creating connected graphs and adjusting edge connectivity. Main functionalities:

- Node and Edge Addition: Methods for adding single/multiple nodes and edges.
- Edge Removal and Connectivity Check: Ensures graph connectivity when edges are removed based on a specified dropout rate.
- Random Graph Creation: Generates a graph with a given dropout rate while retaining connectivity.

2. Routing Algorithms
- A-Star Algorithm: Finds the shortest path using a combination of distance and heuristic cost.
- Depth-First Search (DFS): Explores all paths deeply before backtracking, suitable for unweighted path finding.
- Breadth-First Search (BFS): Explores all paths layer by layer, ideal for unweighted shortest path finding.
- Greedy Best-First Search: Prioritizes paths with the smallest heuristic value.

3. Distance Calculation
A file that uses a map API to compute real-world distances between cities, allowing for accurate routing data.

## Setup
Clone the Repository:

- `git clone https://github.com/shravanbishnoi/City-Routing/`
- Install Required Libraries: Install dependencies listed in requirements.txt, including libraries for graph manipulation, map APIs, and visualization.
- Run Notebooks: Execute each notebook in the provided sequence to generate random graphs, apply routing algorithms, and visualize results.

## Usage
1. Random Graph Creation:
- Use the Random Graph Notebook to generate connected graphs with customizable dropout rates.
2. Algorithm Execution:
- Run the respective notebooks to apply algorithms on generated graphs and compare performance.
