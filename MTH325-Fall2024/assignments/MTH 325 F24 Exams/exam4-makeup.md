# MTH 325 -- Makeup for Exam 4

This is a makeup exam for those who missed Exam 4. All 14 skills are available. If you missed Exam 4 due to an excused absence (that is, a personal emergency or condition that was out of your control and made attendance impossible), and if you have contacted Prof. Talbert about it, you are allowed to attempt any of these problems. Otherwise, you may attempt **any two (2)** but no more than two (2). 

Do all of your work on separate pages in numerical order, and place your name on each page along with the text "Exam 4 makeup" and today's date (December 6, 2024). 

---

## Skill 1

> **(CORE)** I can outline a proof by mathematical induction.

Consider the following proposition, and suppose we want to prove it with mathematical induction: 

**For any integer $n \geq 1$, the number $n^3 + 2n$ is an integer multiple of $3$.** 

1.	State the value of $n$ that corresponds to the base case, then prove that the base case holds. 
2.	Clearly state the inductive hypothesis. Your answer should be phrased as a complete sentence. (No explanation is required here; simply state the inductive hypothesis.) 
3.	Clearly state what you would need to prove, after assuming the inductive hypothesis. Your answer should be phrased as a complete sentence. (You do not need to give a completed proof the statement; simply state what you would need to prove.) 

## Skill 2

> **(CORE)** I can outline a proof using direct, contrapositive, and indirect approaches. 

Consider the proposition: **If $2^n$ is a prime number, then $n$ is a prime number.** 

1. Clearly state what you would assume and what you would prove if you were to prove this statement with a *direct proof*. 
3. Clearly state what you would assume and what you would prove if you were to prove this statement with a *proof by contrapositive*. 
2. Clearly state all the assumptions you would make if you were to prove this statement with a *proof by contradiction*, also known as an *indirect proof*.  


## Skill 3

> **(CORE)** I can represent a graph in different ways, determine information (degree, degree sequence, paths of given length, etc.) about a graph using different representations, and give examples of graphs with specified properties. 

Suppose $G$ is a graph with this Python dictionary: `{0: [3, 6], 1: [2, 3, 6], 2: [1, 4, 5, 6, 7], 3: [0, 1, 6, 7], 4: [2, 7], 5: [2, 7], 6: [0, 1, 2, 3, 7], 7: [2, 3, 4, 5, 6]}`. 

1. Give the adjacency matrix for $G$. 
2. Give the edge list for $G$. 
3. State the degree of each vertex. 
4. Give an example of a cycle of of length 4 in $G$. If no such cycle exists, say so. 

## Skill 4

> I can determine whether a graph has an Euler path or Euler circuit, and whether a graph has a Hamiltonian path or circuit.

Consider the graph below: 

<img src="exam4makeup_s4.png" alt="alt text" style="zoom:67%;" />

**Note: this version of the problem contains new instructions. Read carefully.** 

1. Determine if this graph has an Euler trail, and explain how you know. If it does have an Euler trail, state it as a sequence of vertices. 
2. Determine if this graph has an Euler circuit, and explain how you know. If it does have an Euler circuit, state it as a sequence of vertices.
3. Determine if this graph has a Hamilton path, and explain how you know. If it does have a Hamilton path, state it as a sequence of vertices. 
4. Determine if this graph has a Hamilton cycle, and explain how you know. If it does have a Hamilton cycle, state it as a sequence of vertices.

## Skill 5

> I can use a greedy algorithm to find a vertex coloring for a graph, and I can determine a graph's chromatic number. 



<img src="exam4makeup_s4.png" alt="alt text" style="zoom:67%;" />

1. Implement the greedy coloring algorithm to find a valid vertex coloring for this graph. For the ordering of the vertices, use the degree of the vertices from high to low, and use increasing numerical order in the case of a tie. (For example, if 3 and 7 had the same degree, you would color 3 first.) Your work should consist of a list of vertices in the order in which they are considered; and the color assigned to each one, given **as a non-negative integer** (*not* as an actual color, like blue or red).
2. State the chromatic number of the graph, and explain your reasoning. 

## Skill 6

> I can determine whether two graphs are isomorphic; I can give an explicit isomorphism if they are, and an explanation if they are not.

Consider the two graphs below: 

<img src="exam4makeup_s6.jpg" alt="alt text" style="zoom:67%;" />


Determine if these graphs are isomorphic. If they are isomorphic, give an explicit function between the vertex sets and prove that the edges are preserved. If they are not isomorphic, give a specific isomorphism invariant property that one has but the other does not have. 


## Skill 7

> **(CORE)** I can determine whether a graph is a tree and state information about it. 

1. A graph $G$ has the following adjacency matrix: 

$$\begin{bmatrix}
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 & 0 & 1 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 1 \\
1 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
1 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & 1 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0
\end{bmatrix}$$


Which of the following statements is true? (a) $G$ **must** be a tree; (b) $G$ **might** be a tree but might not be one; or  (c) $G$ **cannot** be a tree? Clearly state your choice, then explain your reasoning. 

2. Consider the following tree with vertex $4$ designated as the root: 
<img src="exam4makeup_s7.png" style="zoom:50%;" />

(a) State the child or children of vertex $1$. 

(b) State the parent or parents of vertex $9$. 

(c) State the leaves of the tree. 

## Skill 8

> I can use Prim's Algorithm and Kruskal's Algorithm to construct a minimum spanning tree for a weighted graph.

<img src="exam4makeup_s8.png" alt="alt text" style="zoom:67%;" />

Using the weighted graph above: 

1. Using Prim's Algorithm and starting at vertex $0$, construct a minimum spanning tree for this graph. Your work should consist of a list of edges in the tree, given in the order in which they are added.
2. Repeat part 1 except using Kruskal's Algorithm. 

## Skill 9

>  I can use Dijkstra's Algorithm to find a minimum distance spanning tree for a weighted graph. 

<img src="exam4makeup_s9.png" alt="alt text"  />


In the weighted graph above, implement Dijkstra’s Algorithm to find the shortest paths from vertex A to all other vertices in the graph. Your work should consist of two things: A list of visited vertices given in the order that they are visited in the algorithm, and a table showing the distances from A to the other vertices with the updates to distances specified in Dijkstra’s Algorithm. 

## Skill 10

> I can execute a breadth-first and depth-first search in a graph.



<img src="exam4makeup_s10.png" alt="Image description" width="400">

Using the graph above: 

1. Execute a depth-first search starting with node $0$. Your final submission should consist of two things: a list of visited vertices in the order in which they are visited, and a history of the stack or queue used to implement the search. Use numerical ordering (low to high) to add vertices into the stack or queue.
2. Repeat the first question but use a breadth-first search. 


## Skill 11

> **(CORE)** I can represent a directed graph in different ways, and determine information about a graph using different representations. 

Let $G$ be a directed graph with this dictionary representation: `{0: [1, 4], 1: [2, 4], 2: [0, 1, 3, 4, 5], 3: [1, 4], 4: [0], 5: [2, 3, 4]}`.


1. State the edge list for $G$. 
2. State the adjacency matrix for $G$. 
3. State the in-degree and out-degree of each vertex. 
4. Draw a picture of the directed graph. 


## Skill 12

> I can use the Floyd-Warshall algorithm to construct the transitive closure of a directed graph. 

Consider the adjacency matrix below: 

$$\left(
\begin{array}{cccc}
 0 & 1 & 1 \\
 1 & 1 & 0  \\
 1 & 0 & 0  \\
\end{array}
\right)$$

Assume that the vertices are 0, 1, 2 and that the rows and columns correspond to those vertices in this order. 

1. Complete the table below for the first six steps of Warshall’s algorithm. The first two rows have the values for the counters in the loops filled in for you. The other values of the loop counters must be done in the correct order given by the pseudocode for Warshall’s algorithm given in class. **Copy the table to your work and complete it there, not on this page!** 

| $k$  | $i$  | $j$  | $W[i,j]$ | $W[i,k]$ | $W[k,j]$ | Result |
| ---- | ---- | ---- | -------- | -------- | -------- | ------ |
| 0    | 0    | 0    |          |          |          |        |
| 0    | 0    | 1    |          |          |          |        |
|      |      |      |          |          |          |        |
|      |      |      |          |          |          |        |
|      |      |      |          |          |          |        |
|      |      |      |          |          |          |        |
|      |      |      |          |          |          |        |

2. Complete the step in Warshall’s algorithm correspoinding to k = 1, i = 1, and j = 2. 

| $k$  | $i$  | $j$  | $W[i,j]$ | $W[i,k]$ | $W[k,j]$ | Result |
| ---- | ---- | ---- | -------- | -------- | -------- | ------ |
| 1    | 1    | 2    |          |          |          |        |

## Skill 13

> I can determine whether a relation is reflexive, symmetric, antisymmetric, and/or transitive, and whether it is an equivalence relation; and if so, I can determine the equivalence class of a point. 

1. Let $S = \lbrace 1, 2, 3, \dots, 10 \rbrace$. Here are two relations on $S$: 
    - Relation 1: $a \sim b$ if $a >  b$  
    - Relation 2: $a \sim b$ if $b-a$ is an integer multiple of 3 

For each relation state whether or not the relation has these properties: reflexive, symmetric, antisymmetric, or transitive. Then state whether or not the relation is an equivalence relation. **This means you will be giving five yes/no responses for each relation, and each yes/no response is labelled with the property you are referring to.** Omitting a yes/no response will not be interpreted as a "yes", it will be interpreted as an incomplete answer. 


2. Let $S = \{ (a,b) \, : \, a,b \, \text{are positive integers} \}$ be the set of all pairs (or tuples) of positive integers. Examples of elements of this set include $(2,3)$ and $(100,200)$, but not $(0,1)$ (because $0$ is not positive) or $(1.1, 2.4)$ (because the entries aren't integers). Define a relation on $S$ by $(a,b) \sim (c,d)$ if $ad = bc$. This is an equivalence relation; state at least three elements of $[(1,2)]$. 

## Skill 14

> I can determine whether a relation is a partial ordering; if so, I can draw its Hasse diagram and identify maximal/minimal elements and/or greatest/least elements, if they exist.

1. Let $S = \{ (a,b) \, : \, a,b \, \text{are positive integers} \}$ be the set of all pairs (or tuples) of positive integers. Examples of elements of this set include $(2,3)$ and $(100,200)$, but not $(0,1)$ (because $0$ is not positive) or $(1.1, 2.4)$ (because the entries aren't integers). For each, state whether the relation is a partial ordering. If a relation *is* a partial order, you do not need to explain why; just state that it is a partial ordering. But, if a relation is *not* a partial ordering, state at least one property of partial orderings that is not satisfied. 
   
   (a) $(a,b) \sim (c,d)$ if $a \leq c$ 

   (b) $(a,b) \sim (c,d)$ if $a < c$

   (c) $(a,b) \sim (c,d)$ if either $a \leq b$ or $c \leq d$

2. Let $S = \{100, 50, 20, 4, 10, 25, 1, 5, 2\}$. Let $\sim$ be the relation on $S$ defined by $a \sim b$ if $b$ is an integer multiple of $a$. (For example, $35$ is an integer multiple of $7$, but $200$ is not.)  This is a partial ordering; draw its Hasse diagram. 