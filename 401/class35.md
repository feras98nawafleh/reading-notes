# Graphs
## What is a graph? 
it's a non linear data structure that can be considered as a group of vertices/nodes connected by edges.
there are two types for graphs, directed and undirected.
## Undirected Graphs:
is a graph where nodes does not have directions on it's edges to other nodes wich makes it bi-directional.
**see example below**
![undirected graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}

## Directed Graphs:
also known as Digraph, where edges have arrow indicating the direction of it, that makes it clear where each node is pointing next.
**see example below**
![directed graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}

## Complete vs Connected vs Disconnected
1. A complete graph is when all nodes are connected to all other nodes.
2. A connected graph is graph that has all of vertices/nodes have at least one edge.
3. A disconnected graph is a graph where some vertices may not have edges.

## Acyclic vs Cyclic
1. An acyclic graph is a directed graph without cycles.
2. A Cyclic graph is a graph that has cycles.

## Traversals
1. Breadth First
2. Depth First

## Real World Uses of Graphs
you may ask yourself what graphs are used for and why is it considered one of the most used and most important data structures, therefore, here's a short list of uses just to mention some:
1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic

