# Learning Outcomes for MTH 325

## Global notes 

+ "State all the definitions and mathematical results from this section" is a learning outcome for _every_ section. 

## Chapter 8: Relations

### 8.1: Relations and their Properties

+ Determine the ordered pairs in a relation from A to B (or from A to A) if the relation is given as a set in set-builder notation, in symbolic form, or in a diagram form. 
+ Determine whether a given relation is reflexive, symmetric, antisymmetric, or transitive. 
+ Given a relation from A to B and a relation from B to C, determine the ordered pairs in the composite of the two relations. 

### 8.2: n-ary Relations and their Applications

Potentially skip this section or save it for the application project. 

### 8.3: Representing Relations

Will need to review matrices (3.8) and do some Sage work before this. 

+ Given a relation from A to B, write the relation as a matrix. Conversely given the matrix for a relation from A to B, write out the ordered pairs in the relation. 
+ Determine whether a relation from A to B is symmetric or antisymmetric using its matrix. 
+ Find matrices representing the union and intersection of two relations. 
+ Find a matrix representing the composite of two relations. 
+ Given a relation from A to B, write the relation as a directed graph (digraph). Conversely given the digraph for a relation from A to B, write out the ordered pairs in the relation. 
+ Determine the properties held by a relation by investigating its digraph. 

### 8.4: Closures of Relations

+ Determine the reflexive closure of a relation on a set A. 
+ Determine the symmetric closure of a relation on a set A. 
+ Determine the transitive closure of a relation on a set A using a digraph or a matrix. 
+ Determine the transitive closure of a relation on a set A using Algorithm 1 and using Warshall's Algorithm. 

### 8.5: Equivalence Relations

+ Determine whether a relation on a set is an equivalence relation. 
+ Given an equivalence relation on a set and an element x in that set, determine the equivalence class of x. 
+ Given an equivalence relation on a set, determine a partition of the set using the equivalence relation. Conversely, given a partition of a set, use it to define an equivalence relation on that set. 

### 8.6: Partial Orderings

+ Determine whether a relation on a set is a partial ordering. 
+ Determine whether a given partially ordered set is a total ordering. 
+ Draw the Hasse diagram for a given poset. 
+ Find: the greatest and least elements of a poset; upper and lower bounds of a subset of a poset; the least upper bound and greatest lower bound of a subset of a poset. 
+ Determine whether a poset is a lattice. 
+ Perform a topological sort of a partially ordered set. 

## Chapter 9: Graphs

### 9.1: Graphs and Graph Models

+ Determine whether a given graph is a simple graph, a multigraph, or a pseudograph. (Similarly for directed graphs.) 
+ Use a graph to model a system of interconnected nodes. 

### 9.2: Graph Terminology and Special Kinds of Graphs

+ Calculate the degree of a vertex in a graph.
+ Explain the reasoning behind the Handshaking Theorem and how the Handshaking Theorem helps to establish the other results in this section. 
+ Draw examples of complete graphs, cycle graphs, wheel graphs, and n-cube graphs. 
+ Determine if a graph is bipartite. 

### 9.3: Representing Graphs and Graph Isomorphism

+ Represent a graph as an adjacency list; and conversely given an adjacency list, draw the graph. 
+ Represent a graph as an adjacency matrix; and conversely given an adjacency matrix, draw the graph.   
+ Represent a graph as an incidence matrix; and conversely given an incidence matrix, draw the graph. 
+ Determine whether two graphs are isomorphic. If they are isomorphic, state the function that implements the isomorphism. 
    
### 9.4: Connectivity

+ Find paths and circuits inside both directed and undirected graphs. 
+ Determine if an undirected graph is connected, and find the connected components of a disconnected graph. 
+ Determine if a directed graph is strongly connected or weakly connected. 
+ Determine the number of paths of length $r$ between two nodes in a graph by using the graph's adjacency matrix. 

### 9.5: Euler and Hamilton Paths

+ Determine whether a graph (directed or undirected) has an Euler path or an Euler circuit. If it has one, construct it using Algorithm 1. 
+ Determine whether a graph (directed or undirected) has an Hamilton path or an Hamilton circuit. 
+ Use Dirac's Theorem and Ore's Theorem to draw conclusions about the existence of Hamilton circuits. 

### 9.6: Shortest-Path Problems

+ Determine the length of a path in a weighted graph. 
+ Use Dijkstra's Algorithm to find the shortest path between two vertices in a weighted graph. 

### 9.7: Planar Graphs

+ Determine whether a graph is planar. If it is, then draw a planar embedding of the graph. 
+ Use Euler's Formula to draw conclusions about the nodes and edges of a planar graph. 

### 9.8: Graph Coloring

+ Determine the chromatic number of a graph. 
+ Apply graph coloring to problems in scheduling and other areas. 

## Chapter 10: Trees

### 10.1: Introduction to Trees

+ Determine whether a graph is a tree. 
+ Given a tree: 
    * Determine its root, if it has one
    * Given a node in the tree, determine its parent and all of its children, siblings, and descendants; and determine whether the node is a leaf or an internal vertex
    * Determine whether it is a full $m$-ary tree for some integer $m$
+ Given a binary tree and a node within the tree, find the left and right children of that node and the left and right subtrees at those children. 
+ Use trees to model various kinds of networks.
+ Use the formulas in the "Properties of Trees" subsection to draw conclusions about the edges and nodes in a tree. 

### 10.2: Applications of Trees

+ Construct a binary search tree for an ordered set of objects. 
+ Use Algorithm 1 to find and add items into a binary search tree. 
+ Use Huffman coding to encode a list of symbols with associated frequencies. 

### 10.3: Tree Traversal

+ Perform preorder, postorder, and inorder traversals of an ordered rooted tree. 
+ Represent a mathematical expression in infix, prefix, and postfix notation. 

### 10.4: Spanning Trees

+ Find a spanning tree within a graph using depth-first and breadth-first search. 

### 10.5: Minimum Spanning Trees

+ Find a minimum spanning tree in a connected weighted graph using Prim's algorithm. 
+ Find a minimum spanning tree in a connected weighted graph using Kruskal's algorithm.


## Other content 

### Technological competence 

+ Sage and SageMath Cloud setup: 
    * Set up an account on SageMath Cloud and create projects and folders within the account for different kinds of work. 
    * Create a Sage notebook in SMC. 
    * Install Sage locally on your own computer. 
    * Perform basic arithmetic calculations using Sage. 
    * [More sage stuff here; suggestions?]
+ Discussion board: 
    * Create an account on Piazza. 
    * Create a new post on Piazza. 
    * Reply to a post on Piazza. 
    * Tweak your email settings on Piazza to raise/lower the frequency of post digests. 
+ Python: 
    * Will have to work on this... basic stuff involving lists, dictionaries, loops, conditional statements and logic -- focusing on stuff used in Sage

### Earlier MTH 225 content

+ 3.8: Matrices 
    * Identify the i-th column, j-th row, and the (i,j)-entry of a matrix. 
    * Identify the size of a matrix. 
    * Calculate the sum of two matrices. 
    * Calculate the product of two matrices. 
    * Write out the $n \times n$ identity matrix. 
    * Given a matrix, write out its transpose. 
    * Determine whether a matrix is symmetric. 
    * Find the join, meet, and Boolean product of two zero-one matrices. 
    * Find the r-th Boolean power of a square zero-one matrix.