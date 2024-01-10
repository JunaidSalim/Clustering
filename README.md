# Clustering_Cpp
 This program implemented in C++ extracts clusters from graphs based on thresold density


**Approach:**
The code implements a graph clustering algorithm based on density and common neighbor criteria. It utilizes a `Graph` class with `Node` objects to represent the graph structure. The clustering algorithm aims to create clusters of nodes by selecting a starting node with maximum degree and expanding the cluster based on specified density and common neighbor thresholds.

1. **Node and Graph Representation:**
   - The `Node` class encapsulates information about individual nodes, including an identifier (`id`), node weight (`nodeWeight`), and a flag indicating whether it's added to a cluster (`addedToCluster`). Nodes maintain a vector of neighbors, each represented as a pair of node ID and edge weight.
   - The `Graph` class manages the overall graph structure, using an unordered map to store nodes.

2. **Clustering Algorithm:**
   - The clustering algorithm iteratively selects nodes with the maximum degree, expands clusters based on density and common neighbor criteria, and marks added nodes. The process continues until all nodes are added to clusters.
   - The `MakeClusters` function orchestrates the clustering process.

3. **Density and Common Neighbor Calculations:**
   - Density calculations are performed both for existing clusters and when considering the addition of a new node to a cluster.
   - Common neighbor calculations identify shared neighbors between nodes.

**Data Structure Used:**
- **Classes:**
  - `Node`: Represents individual nodes with attributes such as ID, node weight, and a flag indicating cluster membership.
  - `Graph`: Manages the overall graph structure, including nodes and functions for adding nodes, edges, and performing clustering.

- **Containers:**
  - `unordered_map`: Utilized for efficiently storing nodes in the graph.
  - `vector`: Used for maintaining neighbors and clusters.

- **Algorithms:**
  - **Breadth-First Search (BFS):** Implemented for expanding clusters by traversing neighbors.

**Readme: Graph Clustering Tool**

**Introduction:**
This C++ program provides a graph clustering tool based on density and common neighbor criteria. The graph is represented using the `Graph` class, with nodes encapsulated by the `Node` class. The clustering algorithm starts from nodes with maximum degree, forming clusters based on user-defined density and common neighbor thresholds.

**Usage:**
1. **Input Graph:**
   - The graph is read from a file (`dataSet.txt`), with each line representing an edge between nodes.
   - Node weights and common neighbors are calculated.

2. **Clustering:**
   - Users input threshold density and common neighbor values.
   - Clusters are generated, and results are saved in `clusters.txt`.

**Compilation and Execution:**
1. **Compilation:**
   - The program can be compiled using a C++ compiler (e.g., g++).
   - Ensure the required libraries are available.

2. **Execution:**
   - Run the compiled executable.
   - Input threshold density and common neighbor values.

3. **Output:**
   - Clusters are displayed in `clusters.txt`.
   - Density information for each cluster is provided.

**Dependencies:**
- A C++ compiler with standard libraries.
- Input graph data in `dataSet.txt` format.
