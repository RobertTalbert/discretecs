---
tags: mth325-f22
---

# Content Skill Standard Quiz 8

:::info
This quiz contains *new versions* of  **Content Skill Standards P.1-P.3, G.1-G.8, and DR.1-DR.6** and *introduces* **Content Skill Standard T.1**. 

**Instructions**

* Work only the problems that you **need to work** and **feel ready to work**. 
* Do your work on separate pages with **each Content Skill Standard on its own separate page**. *Please do not put work for multiple Standards on the same page.* 
* Make sure to consult the [Specifications for Student Work in MTH 325](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document before starting on your work, so you're clear on what is expected and what constitutes a "successful" attempt. 
* Also, make sure to carefully read the **Success Criteria** below each problem to know exactly what is expected from that problem. 
* When you are done: **Scan** each Learning Target to a clear, legible, black-and-white PDF and **upload the PDF** to the designated folder on Blackboard. Please  *do not just take a picture with your camera* --- use a scanning app to create a PDF, and upload the PDF. You can also type up your work and save to a PDF if you want; or use a notes app on a tablet to handwrite your work and save that to a PDF. 

**Authorized resources you may use:**

- [Your textbook](https://discrete.openmathbooks.org/dmoi3.html)
- Previous Content Skill Standard quiz work including feedback on your work 
- Any video or reading used in a Daily Prep 
- A calculator or computer if used for basic calculations 

**The use of Python and networkX is not allowed.** 

If you have another resource you'd like to use that it not shown above, please ask before using it. 
:::


## Content Skill Standard P.1 

:::warning
★ P.1: Given a statement to prove with mathematical induction, I can identify the predicate, state and prove the base case, state the inductive hypothesis, and outline the rest of the proof. 
:::

Consider the statement: 

>For all integers $n \geq 4$, $2^n < n!$. (Here, $n!$ is "$n$ factorial".)

1. State the predicate involved in this statement. 
2. State and prove the base case for a proof by induction of this statement. 
3. State the inductive hypothesis for a proof by induction of this statement. 
4. Outline the remainder of a proof by induction for this statement by clearly stating what you would prove, and giving at least one plausible idea for proving it. 

**Success criteria:** The predicate must be clearly stated; the base case must be correctly stated and proven; and the inductive hypothesis must be correctly stated in the context of the problem. The outline for the remainder of the proof must clearly state what you are going to prove, and the "plausible idea" must be some specific step you might take that makes sense in the context of the problem. 



## Content Skill Standard P.2

:::warning
★ P.2: Given a conditional statement, I can state the assumptions and conclusions for a direct proof, proof by contrapositive, and proof by contradiction. 
:::

Consider the statement: 

>If $T$ is a tree having $v$ vertices and $e$ edges, then $e = v - 1$.  


1. Clearly state what you would assume and what you would prove, if proving this statement with a *direct proof*. 
2. Clearly state what you would assume and what you would prove, if proving this statement with a *proof by contrapositive*.
3. Clearly state *all* the assumptions you would make, if proving this statement *by contradiction*. 

**Success criteria:** All parts of each of the three items here are correctly and clearly stated. 

## Content Skill Standard P.3

:::warning
P.3: I can conduct a critical analysis of a proposed proof of a logical proposition.
:::

Below is a proposition and a proposed proof. Read both carefully and then categorize them in one of the following ways: 

- *The proposition is false.* If this is the case, give a specific counterexample that shows the proposition is false. 
- *The proposition is true but the proof has a fundamental flaw.* If this is the case, find at least one of those fundamental flaws and explain why it makes the proof incorrect. 
- *The proposition is true and there are no fundamental flaws in the proof.* If this is the case, say so, and then give one possible suggestion for improving the clarity or correctness of the proof. 

Be sure to state which of the three categories to which you believe the proposition and proposed proof belong. 

**Note:** This proof uses the terms *rational* and  *irrational numbers*. A *rational number* is a number that can be writtem as a fraction of two integers in lowest form; for example, $3/5$ is rational; so is $0.12$ (because this is equal to $3/25$); and so is $0.111.\dots$ (because this is equal to $1/9$). But for example $\sqrt{2}$ and $\pi$ are irrational because they cannot be written as fractions of integers. 


:::success
**Proposition:** For every real number $x$, if $x$ is irrational and $m$ is an integer, $mx$ is irrational. 

**Proposed proof:** Assume that $x$ is a real number and is irrational. This means that for all integers $a$ and $b$ (with $b \neq 0$), $x \neq \dfrac{a}{b}$. Therefore $mx \neq \dfrac{ma}{b}$ and therefore $mx$ is irrational. :black_medium_small_square: 
:::

**Success criteria:** The work clearly states which of the three categories the proposition and proof belong to. If there is a counterexample, it is specifically and clearly stated. If there is a fundamental flaw, it is specifically and clearly stated, and the nature of the flaw is clearly explained. If there are no fundamental flaws, this is clearly stated and a plausible suggestion for improvement is given. 

## Content Skill Standard G.1

:::warning
★ G.1: I can represent a graph in different ways and change representations from one to another.
:::

Consider the graph $G$, given as a dictionary: 

```python=
{0: [2, 6],
 1: [4, 5, 7],
 2: [0, 6],
 3: [4, 5, 6, 7],
 4: [1, 3],
 5: [1, 3, 7],
 6: [0, 2, 3, 7],
 7: [1, 3, 5, 6]}
```

Write $G$ as: 

1. An acjacency matrix 
3. An edge list 

**Success criteria:** All representations are correct, with up to two errors (for example, forgetting one node, or getting one bit wrong in the matrix) allowed. 


## Content Skill Standard G.2

:::warning
★ G.2: I can determine information about a graph and its individual vertices and edges using different representations.
:::

Consider the graph $G$, given as the dictionary: 

```python=
{0: [1, 6],
 1: [0],
 2: [3, 4, 6],
 3: [2, 4, 5, 6],
 4: [2, 3],
 5: [3, 7],
 6: [0, 2, 3],
 7: [5]}
```

   (a) State the degree sequence of the graph and briefly explain your reasoning **without using a visualization of the graph -- your explanation must only use the edge list**. 
   
   (b) Determine if the graph is bipartite. Explain your reasoning **without using a visualization of the graph -- your explanation must only use the edge list.**


**Success criteria:** All answers are correct and explanations are complete, correct, and clear (and do not use visualizations of the graph). 

## Content Skill Standard G.3

:::warning
G.3: I can give examples of graphs having combinations of various properties or explain why no such example exists, and I can draw examples of special ("named") graphs.
:::

For each situation below, either give an example or explain clearly why no such example exists. 

1. A graph that is not a tree
2. A graph without cycles that is not a tree 
3. A graph with degree sequence 2, 2, 1, 1 
4. A graph with a cycle of length 4 but no cycle of length 3


    
**Success criteria:**  All parts are correct with specific, correct examples given, or in the case of an impossible situation a correct and clear explanation is given. 
    
## Content Skill Standard G.4

:::warning
G.4: I can determine whether two graphs are isomorphic; I can give an explicit isomorphism if they are, and an explanation if they are not. 
:::
    
**Give an example, if possible, of two graphs that have the same number of edges and the same degree sequence but which are *not* isomorphic.**

If an example is possible, draw the two graphs and explain in specific, concrete terms why they are not isomorphic. If an example is not possible, give a clear, correct, and convincing explanation why. 




Remember we have [a list of isomorphism invariant properties](https://gist.github.com/RobertTalbert/2dadae14f8f42c3654a8a77ef5a038f1) that you can use if necessary. 


**Success criteria:** The response to the example (that it is possible, or not possible to construct an example) is correct; and the explanation is correct, clear, and convincing. 
 

## Content Skill Standard G.5

:::warning
G.5:  I can give a valid vertex coloring for a graph and determine a graph's chromatic number.
::: 

Consider the following graph: 

![](https://i.imgur.com/U0wr869.png)


Determine the chromatic number of this graph by doing the following: 

1. Give a proper vertex coloring (either by labeling the vertices, or by actually coloring them) that uses a number of colors equal to the chromatic number; and 
2. Explain why the chromatic number is *exactly* this quantity and not greater or lesser. 

**Success criteria:** In part 1, a proper coloring is explicitly stated that uses the stated amount of colors. In part 2, the chromatic number is correct; a proper coloring with the right number of colors is given; and there is an explanation for why a smaller coloring is impossible. 

## Content Skill Standard G.6

:::warning
G.6: I can determine whether a graph has an Euler path or Euler circuit, and whether a graph has a Hamiltonian path or cycle.
:::


Consider the graph $G$: 

![](https://i.imgur.com/7JO9Eaw.png)



1. Determine if $G$ has an Euler path; if it does, state that path as a sequence of nodes, and if not, clearly explain why not. Then, repeat this task for Euler cycles. *Do these without referring to visual representations of the graph.* 

2. Determine if $G$  has a Hamilton path (not necessarily a cycle). If it does, state that path as a sequence of nodes. If not, explain why not. *Do these without referring to visual representations of the graph.* 

**Success criteria:** If a graph has a structure (Euler path, Euler cycle, Hamilton path --- whatever is requested in the problem) then a correct example is stated as a node sequence. If not, a correct and *specific* explanation is given. Also, the explanations do not refer to or depend on a visual representation of the graph.  

## Content Skill Standard G.7

:::warning
G.7: I can use Prim's Algorithm and Kruskal's Algorithm to construct a minimum spanning tree for a weighted graph.
:::

Consider the weighted graph: 

![](https://i.imgur.com/9QouvzC.png)




1. Using **Prim's Algorithm starting at node B**, construct a minimum spanning tree for this graph. Your answer here should be a list of edges in the MST, given in the order in which they are added to the tree by Prim's Algorithm. 

2. Using **Kruskal's Algorithm**, construct a minimum spanning tree for this graph. Your answer here should be a list of edges in the MST, given in the order in which they are added to the tree by Kruskal's Algorithm. 

**Success criteria:** In each part, the minimum spanning tree is given as a correct list of edges, in the correct order of addition into the tree. 

## Content Skill Standard G.8

:::warning
G.8: I can use Dijkstra's Algorithm to find a minimum-weight path between two vertices in a connected weighted graph.
:::

Consider the weighted graph: 
![](https://i.imgur.com/YklNdXc.png)



**Starting at node B**, use Dijkstra's Algorithm to create the table of shortest-distance information given by the algorithm. Remember the heading for this table looks like this: 

| Vertex | Distance from B| Previous vertex | 
| ----- | ----- | ----- | 

**Success criteria:** No more than one error is present in the table. (Errors that "cascade" from a single error count as multiple errors.)


## Content Skill Standard DR.1

:::warning
★ DR.1: I can determine information about a directed graph and its individual vertices and edges using different representations.
:::

Consider the directed graph given by this edge list: 
```python=
[(0, 3),
 (0, 4),
 (1, 1),
 (2, 7),
 (4, 6),
 (4, 4),
 (5, 1),
 (5, 2),
 (6, 0),
 (7, 0),
 (7, 6)]
```

1. Give the in-degree and out-degree of each vertex. 
2. Write the adjacency matrix for the graph. 

**Success criteria:** The degrees in part 1 are all correct with *no errors*. The adjacency matrix is correct with *up to one error*. 

## Content Skill Standard DR.2

:::warning
DR.2: I can give examples of relations on a set that have combinations of the properties of reflexivity, symmetry, antisymmetry, and transitivity.
:::

For each item below, draw a directed graph for a relation on the set $\{0,1,2,3\}$ that has the indicated combination of properties. If no such example is possible, explain why. (You do not need to provide explanations for examples that are possible.)

1. Symmetric and antisymmetric
2. Transitive but not reflexive  
3. Reflexive, symmetric, and transitive  

**Success criteria:** All examples have the correct combination of properties. Explanations in the event that an example is impossible clearly express why the example is impossible. 


## Content Skill Standard DR.3

:::warning
DR.3: I can determine if a relation is an equivalence relation; I can determine the equivalence class of an element under an equivalence relation and determine whether two elements belong to the same equivalence class. 
:::

1. Consider the relation on the set $\mathbb{Z}$ of all integers given by saying $a \sim b$ if $a - b \leq 10$. Is this an equivalence relation? If so, give a complete and clear explanation of why. If not, give a *specific* example that explains why not. 
2. Consider the relation on the set of all words in the English language, by saying that the word $w_1$ is related to the word $w_2$ if $w_1$ starts and ends with the same letters that $w_2$ starts and ends with. For example the word "actual" would be related to the words "artificial" and "ail", but not to the words "artist" or the word "bridal". It can be shown (but don't do it here) that this is an equivalence relation. State five different elements of $[\text{discrete}]$. 

**Success criteria:** The explanation in the first item is clear, correct, and specific. The elements listed in the second part are all correct. 

##  Content Skill Standard DR.4

:::warning
DR.4: I can find the $n$th order composition of a relation with itself. 
:::

Consider the relation $r$ on the set $\{0,1,2,3,4,5\}$ given below as an edge list: 

```python=
[(0, 1), (0, 3), (1, 4), (2, 5), (4, 1), 
 (4, 2), (4, 5), (5, 1), (5, 2)]
```
1. State the complete edge list for the relation $r^2$. 
2. State three edges that belong to $r^3$. (If there are fewer than three, state them all.)

**Success criteria:** The edge list in the first part is correct except for one mistake or omission allowed. The three edges in the second part are all correct members of $r^3$. 

## Content Skill Standard DR.5

:::warning
DR.5: I can sketch the transitive closure of a relation as a directed graph. 
:::

Consider the relation $r$ on the set $\{0,1,2,3,4,5\}$ given below as directed graph:

![](https://i.imgur.com/eoCgWEJ.png)



State the transitive closure of $r$, as an *edge list*. (You can draw the directed graph if you like, but your answer must include a correct edge list.) 

**Success criteria:** The edge list is correct with up to two mistakes or omissions allowed. 

## Content Skill Standard DR.6

:::warning
DR.6: I can determine when a set with a relation is a partially ordered set; I can draw the Hasse diagram of a poset and identify maximal/minimal elements and/or greatest/least elements, if they exist.
:::

Let $U = \{1,2,3,4\}$ and suppose $S$ is the set whose elements are all the subsets of $U$ with $1$, $2$, or $3$ elements. For example $\{1,2\} \in S$ and $\{2,3,4\} \in S$, but $\emptyset \not \in S$ and $\{1,2,3,4\} \not \in S$. So, $S$ is part of, but not equal to the power set of $S$.

For any two sets $A, B \in S$ say that $A \sim B$ if $A \subseteq B$. This relation makes $S$ a partially ordered set.  

1. Draw the Hasse diagram for this poset. 
2. State the maximal and minimal elements, if they exist. If either of these does not exist, say so. 
3. State the greatest and least elements, if they exist. If either of these does not exist, say so. 

**Success criteria:** The Hasse diagram is correct with no errors or omissions. The maximal, minimal, greatest, and least elements are all correct with no omissions or errors; if any of these does not exist, that fact is clearly stated. 


## :new: Content Skill Standard T.1

:::warning
T.1: I can determine whether a description of a graph (list of vertex and edge sets, degree sequence, a drawing, or list of properties) represents a tree.
:::

Each part below states a specific condition on a graph $G$. For each case, determine if the graph *must* be a tree, *might or might not* be a tree, or *cannot* be a tree. 

In each case, if the graph *must* be a tree or *cannot* be a tree, give a specific, clear, and correct explanation of why (that does not merely state the definition of a tree). If the graph *might or might not* be a tree, give a concrete, specific example of a graph that is a tree that satisfies the conditions given and a concrete, specific example of a graph that is not a tree that satisfies the conditions. 

1. $G$ is a graph with 10 vertices and 7 edges
2. $G$ is a graph with degree sequence 4, 1, 1, 1, 1
3. $G$ is a graph with degree sequence 2, 2, 2, 1, 1

:::info
Solutions: 

1. This graph **cannot** be a tree because all trees satisfy the property that $e = v-1$ where $e$ and $v$ are the numbers of edges and vertices, respectively, and this graph doesn't do that. 
2. This graph **must** be a tree because the only possible graph that can be drawn with this degree sequence is the one with edges $(0,1), (0,2), (0,3), (0,4)$ and that's a tree. 
3. This graph **might or might not** be a tree. One possible graph that has this degree sequence is the one that's $K_3$ and $K_2$ taken side by side, and this isn't a tree because it's not connected and it has a cycle. On the other hand, $P_4$ (a path with four edges) is a tree that has this degree sequence. (Other examples of trees and non-trees are possible here!)
:::


**Success criteria:** Each part has a correct basic answer (must be a tree, cannot be a tree, might or might not be a tree). If the basic answer is "must be" or "cannot be", the explanation is clear, correct, and convincing. If the answer is "might or might not be" then two correct examples are given -- one where the condition is satisfied and the graph is a tree, and another where the condition is satisfied and the graph is not a tree. 