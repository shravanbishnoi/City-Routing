# Optimal City Routing

## Introduction
	While we were studying the classical AI algorithms, our professor Dr. Kushal Shah told that whole world is using just one dataset to teach AI algorithms. Everybody is using just one and only one dataset which is road map of Romania. So, we curated a dataset to study AI algorithms. This data collection is the combined efforts of Batch 2026 and 2027 of Sitare University. This dataset contains widely spreaded and well connected cities of Bharat.

## Dataset Collection
	The cities in the data are the birth places of students of Sitare University. The students of 2026 and 2027 batch are asked to enter their cities in a shared excel sheet. Then, duplicate cities were removed while reviewing the data before further processing on it.

## Processing of data
	After collection of data there were around 50 cities.Some of cities were not well suited for the structuring of dataset. Since when we plotted cities on the map they were so much congested on the graph and graph was complex to see.As the raw data, there left only 45 cities with no additional information except name. Data has been further processed to add additional information. This has been done with help of following steps:

	For rough idea of graph, we plotted all the cities on the google map to see how it looks like.
	Need to calculate road distance and straight line distance between every two cities. To do this we searched on google for APIs which can make our job easy. Hopefully, we found an API which can do this with high accuracy.
	Now plotted a graph with route distances between any two cities on Paint as well as on a chart with help of an artist.
	Created a csv file to record that how many cities are connected to a particular city.
	Created a script which will give a randomized connected sub graph by dropping some of edges from whole graph.

## About DataSet
	We have created a dataset for complete graph and for the simpl implementation of the code we made some changes in representation of the dat in  
	our dataset. Our dataset is of the following type:

		If we have two cities city A and city B then in our data set there will be a row which have (A, B, Route_Distance, Heuristic_distance) as well as a other row for (B, A, Route_Distance, Heuristic_distance).
		Also if we have a city A then our dataset also contains a row (A, A, 0, 0) for simple implementation of code.

## Challenges
	Since there was huge data collection so it was very difficult to calculate distance of every city from other cities manually. Furthermore, it was challenging to enter 2025 entries in excel sheets manually.

## Solutions
	These challenges were addressed with the help of our programming skills, we used some APIs and wrote our own programs to make work more easy.

## Code Example:-
	>>> G = Graph.Graph()          # Created Graph object.
	>>> G.add_nodes(df['nodes'])         # Adding the edges to the graph object.
	>>> G.randomGraphCreater(dropout)    # Creating the random connect graph from the complete graph.
	### Dropout means how much fraction of edges you want to drop from the Graph. 
	### ( Note:- For randomGraphCreater first you should have complete graph in the graph object G.)

## Project Structure
- **Algorithms**: Notebooks implementing A-Star, DFS, BFS, and Greedy Best-First Search algorithms.
- **Distance Calculation**: File using a map API to calculate distances between two cities.
- **Random Graph Generation**:
      - Graph.py: Contains the Graph class for graph creation, adding/removing edges, and generating random graphs.
      - Random Graph Notebook: Notebook for dropping edges to create random connected graphs.
- **Data**:
      - Datasets: CSV files containing city and route data.
      - Images: Graph visualizations generated from random graphs.

## Key Components
1. **Graph Class (Graph.py)**
The Graph class provides a custom implementation for creating connected graphs and adjusting edge connectivity. Main functionalities:

    - **Node and Edge Addition**: Methods for adding single/multiple nodes and edges.
    - **Edge Removal and Connectivity Check**: Ensures graph connectivity when edges are removed based on a specified dropout rate.
    - **Random Graph Creation**: Generates a graph with a given dropout rate while retaining connectivity.

2. **Routing Algorithms**
     - **A-Star Algorithm**: Finds the shortest path using a combination of distance and heuristic cost.
     - **Depth-First Search (DFS)**: Explores all paths deeply before backtracking, suitable for unweighted path finding.
     - **Breadth-First Search (BFS)**: Explores all paths layer by layer, ideal for unweighted shortest path finding.
     - **Greedy Best-First Search**: Prioritizes paths with the smallest heuristic value.

3. **Distance Calculation**
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
