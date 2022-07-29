# Lesson Level Objectives for MTH 325

## Review

- Given a set, or two sets: 
  - Determine if an object is an element 
  - Determine if one is a subset of the other
  - Find the intersection, union, difference, and cartesian product 
- Determine if two integers are congruent mod $m$
- Given a conditional statement: 
  - State the hypothesis and conclusion
  - State the converse, contrapositive, and negation
  - State the conditions under which it's true
- Given a function between two sets: 
  - State the domain, codomain, and range
  - Determine whether it's injective, surjective, or bijective 
- Given a statement to be proven using mathematical induction (weak): 
  - State and prove the base case
  - State the inductive hypothesis
  - State what needs to be proven in the proof step, and provide useful thoughts on how to do it  
- 

## Proof

- Given a statement to be proven using mathematical induction (of any flavor): 
  - State and prove the base case
  - State the inductive hypothesis
  - State what needs to be proven in the proof step, and provide useful thoughts on how to do it 
- Explain the differences between weak, strong, and structural induction and when each method of proof is appropriate. 
- Given a conditional statement to prove, determine whether direct, indirect, or contrapositive is the best approach
- Given a statement to be proven using direct proof: 
  - Identify the assumptions and the goal 
  - Write the first and last lines of the proof
  - Perform "forward" and "backward" steps
  - Write a well-written completed proof 
- Given a statement to be proven using contradiction: 
  - State the assumptions 
  - Outline a proof that arrives at a contradiction and identity the contradiction
  - Write a well-written completed proof
- Given a written proof: 
  - Identify the form of proof being used
  - Analyze its structure
  - Perform a "critical analysis" (determine whether the proposition itself is true or false; determine if the proof is correct and find critical errors; if the proof is correct and free of critical errors, give suggestions for stylistic improvement)


## Graphs 

*This is long! May need to break into 2 modules* 

- State the definition of a graph
- Represent a graph in different ways 
  - As a pair (V,E) of vertices and edges 
  - As an adjacency list 
  - As a picture
  - As a matrix (two ways: adjacency and incidence)
  - As a table
  - ==As a Python dictionary==
- Visualize a graph using `networkX` 
- Determine whether or not two graphs are isomorphic; if they are, state an explicit isomorphism between them 
- Determine the degree of a vertex 
- Draw the complete graph on $n$ vertices, $K_n$ 
- State and prove the Handshake Lemma 
- Find the degree sequence of a graph and determine if a given sequence can be the degree sequence of a graph
- State/prove Proposition 4.18 (number of vertices of odd degree must be even)
- Determine if a graph is bipartite; if so, write the parts 
- Draw $K_{m,n}$
- Identify and draw all the "famous" graphs: $K_n$, $K_{m,n}$, $C_n$, $P_n$ 
- Determine whether two vertices are adjacent; state all the vertices adjacent to a given vertex
- Determine whether a graph is connected; find all the connected components of a graph
- State the definition of a tree; determine if a graph is a tree
- State/prove Proposotion 4.2.1 (tree iff a unique path between any two distinct vertices)
- State/prove Proposition 4.2.3 (tree with at least two vertices has at least two vertices of degree 1)
- State/prove Proposition 4.2.4 (e = v - 1 in a tree)
- Find all parents, children, and siblings of a vertex in a rooted tree
- Find a spanning tree for a connected graph
- Find the total weight of a path in a weighted graph
- Use Dijkstras algorithm to find the shortest path between two vertices in a weighted graph
- Find a minimal spanning tree in a weighted graph (Prim/Kruskal)
- Give a proper vertex coloring for a graph
- Determine the chromatic number of a graph
- State the Four Color Theorem 
- Apply graph coloring to scheduling problems
- Identify cliques in a graph and the clique number of a graph
- State/prove Theorem 4.4.4
- State/prove Brooks' Theorem 
- Find the chromatic index of a graph
- State/prove Vizing's Theorem
- Identify whether a path on a graph is a circuit, Euler path, Euler circuit; Hamilton path, Hamilton cycle 
- Determine whether a graph has an Euler path or Euler circuit (similarly Hamilton path/cycle)
- identify matchings and partial matchings in graphs. 
- Apply Hall’s Marriage theorem to determine whether a bipartite graph has a matching.


## Digraphs and Relations

**This needs additional ideas from alternate sources** 

- Represent a digraph/relation in different ways
  - As a picture
  - As a matrix
  - ==As a Python dictionary== 
  - As a table
- Determine the in-degree and out-degree of a vertex in a digraph
- Determine whether a digraph is weakly/strongly connected
- Find the n-th order composition of a relation with itself 
- Determine whether a relation is reflextive, symmetric, antisymmetric, transitive
- Determine whether a relation is an equivalence relation; if it is, give the equivalence classes (or the class of one vertex); determine whether two elements belong to the same equivalence class 
- Create examples of relations with specific combinations of reflexivity, symmetry, antisymmetry, and transitivity
- Sketch the transitive closure of a digraph
- Determine when a set with relation is a poset
- Draw the Hasse diagram for a poset 
- Identify maximal/minimal elements or greatest/least elements

## Trees

**This needs additional ideas from alternate sources** 

- Construct the binary search tree for a total ordering
- List the vertices of a tree in order, using preorder, postorder, and inorder traversals 