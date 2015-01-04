Learning Objectives for MTH 325: Discrete Mathematics for Computer Science 2
============================================================================

This document can also be found online: 

+ At the course Blackboard site under `Course Documents > MTH 325 Learning Objectives`
+ On Github Gists at: [https://gist.github.com/RobertTalbert/00b1103d27c6e00c9b73](https://gist.github.com/RobertTalbert/00b1103d27c6e00c9b73)
+ On the MTH 325 Github repository 

Legend: 

+ CC = Learning objectives to be assessed through Concept Checks. 
+ M = Learning objectives to be assessed through Learning Modules.
+ (CORE) = Learning objectives designated as belonging to the 20 CORE-M learning objectives for Modules, assessed during timed assessment periods. 


MTH 325 Learning Objectives in order of appearance 
==================================================

## Chapter 8: Relations

### 8.1: Relations and their properties

+ CC.1: State the definitions of the following terms: binary relation from A to B; relation on a set A; reflexive relation; symmetric relation; antisymmetric relation; transitive relation; composite of two relations. 
+ M.1 (CORE): Determine whether a given relation is reflexive, symmetric, antisymmetric, or transitive. 
+ M.2 (CORE): Given a relation from A to B and a relation from B to C, determine the ordered pairs in the composite of the two relations. 

### 8.3: Representing Relations

+ CC.2: State the definitions of the following terms: Directed graph (digraph); initial and terminal nodes (vertices) of an edge in a digraph
+ CC.3: Given a relation represented as a matrix or a digraph, determine whether two elements are related. 
+ M.3 (CORE): Given a relation represented as a set of pairs, a symbolic relationship, a matrix, or a directed graph, convert it to another representation. 
+ M.4: Find matrices representing the union, intersection, and composition of two relations. 

_Note_: Objective M.1 from Section 8.1 will be assessed using different representations of relations. 

### 8.4: Closures of Relations

+ CC.4: State the definitions of the following terms: Transitive closure; reflexive closure; diagonal relation on A; symmetric closure; path between two nodes in a digraph; length of a path; circuit or cycle in a digraph; connectivity relation. 
+ CC.5: Identify paths and circuits in a digraph. 
+ M.5: Determine the reflexive and symmetric closures of a relation on a set. 
+ M.6: Apply Theorem 1 to determine whether a pair of points belongs to R^n where R is a relation; conversely use Theorem 1 to interpret membership in R^n in terms of paths in digraphs. 
+ M.7 (CORE): Determine the transitive closure of a relation using Algorithm 1 and using Warshall's Algorithm, and explain the practical significance of the transitive closure of a relation. 

### 8.5: Equivalence Relations

+ CC.6: State the definitions of the following terms: Equivalence relation; equivalence class; partition of a set. 
+ CC.7: Given an equivalence relation on a set A, determine if two elements of A belong to the same equivalence class. 
+ M.8 (CORE): Determine whether a relation on a set is an equivalence relation. 
+ M.9 (CORE): Given an equivalence relation on a set A and a point x in A, determine the equivalence class of x. 
+ M.10: Given an equivalence relation on a set, determine a partition of the set using the equivalence relation. Conversely, given a partition of a set, use it to define an equivalence relation on that set. 

### 8.6 Partial Orderings

+ CC.8: State the definitions of the following terms: Partial ordering; partially ordered set (poset); comparable elements in a poset; totally ordered set; total ordering; well-ordered set; lexicorgaphic ordering; maximal, minimal, greatest, and least elements of a poset; upper bound, lower bound, least upper bound, and greatest lower bound of a subset of a poset; lattice.
+ CC.9: Given a poset, determine whether two elements are comparable; find the maximal, minimal, greatest, and least elements; and find the upper bound, lower bound, least upper bound, and greatest lower bound of a subset of a poset. 
+ CC.10: Draw the Hasse diagram for a poset. 
+ M.11 (CORE): Determine whether a relation on a set is a partial ordering or total ordering, and whether the set is a lattice under the relation. 
+ M.12 (CORE): Use the topological sorting algorithm to find a compatible total ordering for a poset. 

## Chapter 9: Graphs

### 9.1: Graphs and Graph Models

+ CC.11: State the definitions of the following terms: Graph; nodes; edges; simple graph; multigraph; pseudograph; undirected and directed graph. 
+ M.13 (CORE): Use a graph to model a system of interconnected nodes.

### 9.2: Graph Terminology and Special Kinds of Graphs

+ CC.12: State the definitions of the following terms: Adjacent nodes; incident; degree of a vertex in an undirected graph; initial and terminal vertices of a directed edge; in-degree and out-degree of a vertex in a digraph; complete graph on n vertices; cycle graph; wheel graph; n-cube graph; bipartite graph; complete bipartite graph; subgraph. 
+ CC.13: Given an undirected graph, determine if two nodes are adjacent; determine if an edge is incident with two nodes; and find the degree of a vertex. 
+ CC.14: Given a directed graph, determine if two notes are adjacent from each other; and find the in- and out-degree of a vertex. 
+ CC.15: Draw examples of the cycle, wheel, n-cube, and complete bipartite graphs. 
+ CC.16: State the Handshaking Theorem and Theorem 2. 
+ M.14: Explain how the Handshaking Theorem is proven and how it is used to prove Theorem 2. 
+ M.15 (CORE): Use the Handshaking Theorem and Theorem 2 to draw conclusions about edges and nodes in a graph. 

### 9.3: Representing Graphs and Graph Isomorphism

+ CC.17: State the definitions of the following terms: Isomorphic graphs; isomorphism of graphs.
+ CC.18: Given a graph represented as an adjacency list, Python dictionary, adjacency matrix, or incidence matrix, determine whether two nodes are connected and calculate the degree of a node. 
+ M.16 (CORE): Given a graph represented as an adjacency list, Python dictionary, adjacency matrix, or incidence matrix, write it in one of the other representations and use the representation to determine information about the graph. 
+ M.17: Determine whether two graphs are isomorphic; if they are, state the isomorphism. 

### 9.4: Connectivity

+ CC.19: State the definitions of the following terms: Path of length n (undirected and directed versions); circuit (undirected and directed versions); simple path/circuit; connected (undirected) graph; connected component of a graph; strongly connected digraph; weakly connected digraph
+ CC.20: Given a graph (directed or undirected), find a path of a specified length, and find a circuit. 
+ M.18 (CORE): Determine if an undirected graph is connected, and find the connected components of a disconnected graph.
+ M.19: Determine the number of paths of length $r$ between two nodes in a graph by using the graph's adjacency matrix. 

### 9.5: Euler and Hamilton Paths

+ CC.21: State the definitions of the following terms: Euler circuit; Euler path; Hamilton path; Hamilton circuit. 
+ CC.22: State Dirac's Theorem and Ore's Theorem. 
+ CC.23: State whether a given path or circuit in a graph is Eulerian or Hamiltonian. 
+ M.20 (CORE): Determine whether a graph (directed or undirected) has an Euler path or an Euler circuit, or a Hamilton path or Hamilton circuit. 
+ M.21 (CORE): Use Dirac's Theorem and Ore's Theorem to draw conclusions about the existence of Hamilton circuits. 

### 9.6: Shortest-Path Problems

+ CC.24: Find the length (total weight) of a path in a weighted graph. 
+ M.22: Use Dijkstra's Algorithm to find the shortest path in a weighted graph. 

### 9.7: Planar Graphs

+ CC.25: State the definitions of the following terms: Planar graph. 
+ CC.26: State Euler's formula and use it to determine information about regions, nodes, or edges in a connected planar simple graph. 
+ M.23 (CORE): Use the three Corollaries to Euler's Formula to determine information about the planarity of a graph or about nodes or edges in a planar graph. 

### 9.8: Graph Coloring

+ CC.27: State the definitions of the following terms: Coloring of a simple graph; chromatic number of a graph. 
+ CC.28: Given a simple graph, find a coloring of the graph using a specified number of colors. 
+ CC.29: State the Four Color Theorem. 
+ M.24 (CORE): Determine the chromatic number of a graph. 
+ M.25: Apply graph coloring to problems in scheduling and other related area. 

## Chapter 10: Trees 

### 10.1: Introduction to Trees

+ CC.30: State the definitions of the following terms: tree, rooted tree; m-ary (and binary) tree; full m-ary tree. 
+ CC.31: Given a tree, do the following: Determine its root, if it has one; Given a node in the tree, determine its parent and all of its children, siblings, and descendants, and determine whether the node is a leaf or an internal vertex; and state whether the tree is m-ary or full m-ary for some integer m. 
+ CC.32: Given a binary tree and a node, find the left and right children of that node and the left and right subtrees at those children.
+ M.26: Use trees to model various kinds of networks. 
+ M.27: Use the formulas in the "Properties of Trees" subsection to draw conclusions about the edges and nodes in a tree.

### 10.2: Applications of Trees

+ M.28 (CORE): Construct a binary search tree for an ordered set of objects and then use Algorithm 1 to find and add items into the binary search tree. 
+ M.29: Use Huffman coding to encode a list of symbols with associated frequencies. 

### 10.3: Tree Traversal

+ CC.33: Perform preorder, postorder, and inorder traversals of an ordered rooted tree. 
+ M.30: Represent and evalaute a mathematical expression in infix, prefix, and postfix notation. 

### 10.4: Spanning Trees

+ CC.34: State the definition of the term _spanning tree_ and identify whether a subgraph of a given graph is or is not a spanning tree. 
+ M.31 (CORE): Find a spanning tree within a graph using depth-first and breadth-first search. 

### 10.5: Minimum Spanning Trees

+ CC.35: State the definition of the term _minimum spanning tree_ and identify whether a subgraph of a weighted graph is or is not a minimum spanning tree. 
+ M.32 (CORE): Find a minimum spanning tree in a connected weighted graph using Prim's algorithm. 
+ M.33 (CORE): Find a minimum spanning tree in a connected weighted graph using Kruskal's algorithm.


MTH 325 Learning Objectives by type 
===================================

## Concept Check (CC) objectives 

+ CC.1: State the definitions of the following terms: binary relation from A to B; relation on a set A; reflexive relation; symmetric relation; antisymmetric relation; transitive relation; composite of two relations. 
+ CC.2: State the definitions of the following terms: Directed graph (digraph); initial and terminal nodes (vertices) of an edge in a digraph
+ CC.3: Given a relation represented as a matrix or a digraph, determine whether two elements are related. 
+ CC.4: State the definitions of the following terms: Transitive closure; reflexive closure; diagonal relation on A; symmetric closure; path between two nodes in a digraph; length of a path; circuit or cycle in a digraph; connectivity relation. 
+ CC.5: Identify paths and circuits in a digraph. 
+ CC.6: State the definitions of the following terms: Equivalence relation; equivalence class; partition of a set. 
+ CC.7: Given an equivalence relation on a set A, determine if two elements of A belong to the same equivalence class. 
+ CC.8: State the definitions of the following terms: Partial ordering; partially ordered set (poset); comparable elements in a poset; totally ordered set; total ordering; well-ordered set; lexicorgaphic ordering; maximal, minimal, greatest, and least elements of a poset; upper bound, lower bound, least upper bound, and greatest lower bound of a subset of a poset; lattice.
+ CC.9: Given a poset, determine whether two elements are comparable; find the maximal, minimal, greatest, and least elements; and find the upper bound, lower bound, least upper bound, and greatest lower bound of a subset of a poset. 
+ CC.10: Draw the Hasse diagram for a poset. 
+ CC.11: State the definitions of the following terms: Graph; nodes; edges; simple graph; multigraph; pseudograph; undirected and directed graph. 
+ CC.12: State the definitions of the following terms: Adjacent nodes; incident; degree of a vertex in an undirected graph; initial and terminal vertices of a directed edge; in-degree and out-degree of a vertex in a digraph; complete graph on n vertices; cycle graph; wheel graph; n-cube graph; bipartite graph; complete bipartite graph; subgraph. 
+ CC.13: Given an undirected graph, determine if two nodes are adjacent; determine if an edge is incident with two nodes; and find the degree of a vertex. 
+ CC.14: Given a directed graph, determine if two notes are adjacent from each other; and find the in- and out-degree of a vertex. 
+ CC.15: Draw examples of the cycle, wheel, n-cube, and complete bipartite graphs. 
+ CC.16: State the Handshaking Theorem and Theorem 2. 
+ CC.17: State the definitions of the following terms: Isomorphic graphs; isomorphism of graphs.
+ CC.18: Given a graph represented as an adjacency list, Python dictionary, adjacency matrix, or incidence matrix, determine whether two nodes are connected and calculate the degree of a node. 
+ CC.19: State the definitions of the following terms: Path of length n (undirected and directed versions); circuit (undirected and directed versions); simple path/circuit; connected (undirected) graph; connected component of a graph; strongly connected digraph; weakly connected digraph
+ CC.20: Given a graph (directed or undirected), find a path of a specified length, and find a circuit.
+ CC.21: State the definitions of the following terms: Euler circuit; Euler path; Hamilton path; Hamilton circuit. 
+ CC.22: State Dirac's Theorem and Ore's Theorem. 
+ CC.23: State whether a given path or circuit in a graph is Eulerian or Hamiltonian. 
+ CC.24: Find the length (total weight) of a path in a weighted graph. 
+ CC.25: State the definitions of the following terms: Planar graph. 
+ CC.26: State Euler's formula and use it to determine information about regions, nodes, or edges in a connected planar simple graph. 
+ CC.27: State the definitions of the following terms: Coloring of a simple graph; chromatic number of a graph. 
+ CC.28: Given a simple graph, find a coloring of the graph using a specified number of colors. 
+ CC.29: State the Four Color Theorem. 
+ CC.30: State the definitions of the following terms: tree, rooted tree; m-ary (and binary) tree; full m-ary tree. 
+ CC.31: Given a tree, do the following: Determine its root, if it has one; Given a node in the tree, determine its parent and all of its children, siblings, and descendants, and determine whether the node is a leaf or an internal vertex; and state whether the tree is m-ary or full m-ary for some integer m. 
+ CC.32: Given a binary tree and a node, find the left and right children of that node and the left and right subtrees at those children.
+ CC.33: Perform preorder, postorder, and inorder traversals of an ordered rooted tree.
+ CC.34: State the definition of the term _spanning tree_ and identify whether a subgraph of a given graph is or is not a spanning tree. 
+ CC.35: State the definition of the term _minimum spanning tree_ and identify whether a subgraph of a weighted graph is or is not a minimum spanning tree. 

## Module (M) Objectives 

+ M.1: Determine whether a given relation is reflexive, symmetric, antisymmetric, or transitive. 
+ M.2: Given a relation from A to B and a relation from B to C, determine the ordered pairs in the composite of the two relations. 
+ M.3: Given a relation represented as a set of pairs, a symbolic relationship, a matrix, or a directed graph, convert it to another representation. 
+ M.4: Find matrices representing the union, intersection, and composition of two relations. 
+ M.5: Determine the reflexive and symmetric closures of a relation on a set. 
+ M.6: Apply Theorem 1 to determine whether a pair of points belongs to R^n where R is a relation; conversely use Theorem 1 to interpret membership in R^n in terms of paths in digraphs. 
+ M.7: Determine the transitive closure of a relation using Algorithm 1 and using Warshall's Algorithm, and explain the practical significance of the transitive closure of a relation.
+ M.8: Determine whether a relation on a set is an equivalence relation. 
+ M.9: Given an equivalence relation on a set A and a point x in A, determine the equivalence class of x. 
+ M.10: Given an equivalence relation on a set, determine a partition of the set using the equivalence relation. Conversely, given a partition of a set, use it to define an equivalence relation on that set. 
+ M.11: Determine whether a relation on a set is a partial ordering or total ordering, and whether the set is a lattice under the relation. 
+ M.12: Use the topological sorting algorithm to find a compatible total ordering for a poset. 
+ M.13: Use a graph to model a system of interconnected nodes.
+ M.14: Explain how the Handshaking Theorem is proven and how it is used to prove Theorem 2. 
+ M.15: Use the Handshaking Theorem and Theorem 2 to draw conclusions about edges and nodes in a graph. 
+ M.16: Given a graph represented as an adjacency list, Python dictionary, adjacency matrix, or incidence matrix, write it in one of the other representations and use the representation to determine information about the graph. 
+ M.17: Determine whether two graphs are isomorphic; if they are, state the isomorphism. 
+ M.18: Determine if an undirected graph is connected, and find the connected components of a disconnected graph.
+ M.19: Determine the number of paths of length $r$ between two nodes in a graph by using the graph's adjacency matrix. 
+ M.20: Determine whether a graph (directed or undirected) has an Euler path or an Euler circuit, or a Hamilton path or Hamilton circuit. 
+ M.21: Use Dirac's Theorem and Ore's Theorem to draw conclusions about the existence of Hamilton circuits. 
+ M.23: Use the three Corollaries to Euler's Formula to determine information about the planarity of a graph or about nodes or edges in a planar graph.
+ M.24: Determine the chromatic number of a graph. 
+ M.25: Apply graph coloring to problems in scheduling and other related area. 
+ M.26: Use trees to model various kinds of networks. 
+ M.27: Use the formulas in the "Properties of Trees" subsection to draw conclusions about the edges and nodes in a tree.
+ M.28: Construct a binary search tree for an ordered set of objects and then use Algorithm 1 to find and add items into the binary search tree. 
+ M.29: Use Huffman coding to encode a list of symbols with associated frequencies. 
+ M.30: Represent and evalaute a mathematical expression in infix, prefix, and postfix notation. 
+ M.31: Find a spanning tree within a graph using depth-first and breadth-first search. 
+ M.32: Find a minimum spanning tree in a connected weighted graph using Prim's algorithm. 
+ M.33: Find a minimum spanning tree in a connected weighted graph using Kruskal's algorithm.

## CORE Module (CORE-M) Objectives 

This is a subset of the M Objectives. These will be assessed both in Learning Modules and in timed assessments. There are 20 of these. 

+ M.1: Determine whether a given relation is reflexive, symmetric, antisymmetric, or transitive. 
+ M.2: Given a relation from A to B and a relation from B to C, determine the ordered pairs in the composite of the two relations. 
+ M.3: Given a relation represented as a set of pairs, a symbolic relationship, a matrix, or a directed graph, convert it to another representation. 
+ M.7: Determine the transitive closure of a relation using Algorithm 1 and using Warshall's Algorithm, and explain the practical significance of the transitive closure of a relation.
+ M.8: Determine whether a relation on a set is an equivalence relation. 
+ M.9: Given an equivalence relation on a set A and a point x in A, determine the equivalence class of x. 
+ M.11: Determine whether a relation on a set is a partial ordering or total ordering, and whether the set is a lattice under the relation. 
+ M.12: Use the topological sorting algorithm to find a compatible total ordering for a poset. 
+ M.13: Use a graph to model a system of interconnected nodes.
+ M.15: Use the Handshaking Theorem and Theorem 2 to draw conclusions about edges and nodes in a graph. 
+ M.16: Given a graph represented as an adjacency list, Python dictionary, adjacency matrix, or incidence matrix, write it in one of the other representations and use the representation to determine information about the graph. 
+ M.18: Determine if an undirected graph is connected, and find the connected components of a disconnected graph.
+ M.20: Determine whether a graph (directed or undirected) has an Euler path or an Euler circuit, or a Hamilton path or Hamilton circuit. 
+ M.21: Use Dirac's Theorem and Ore's Theorem to draw conclusions about the existence of Hamilton circuits. 
+ M.23: Use the three Corollaries to Euler's Formula to determine information about the planarity of a graph or about nodes or edges in a planar graph.
+ M.24: Determine the chromatic number of a graph. 
+ M.28: Construct a binary search tree for an ordered set of objects and then use Algorithm 1 to find and add items into the binary search tree. 
+ M.31: Find a spanning tree within a graph using depth-first and breadth-first search. 
+ M.32: Find a minimum spanning tree in a connected weighted graph using Prim's algorithm. 
+ M.33: Find a minimum spanning tree in a connected weighted graph using Kruskal's algorithm.
