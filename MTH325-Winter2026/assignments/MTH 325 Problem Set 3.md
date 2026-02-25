# Problem Set 3

## Instructions

Recall the rules for problem sets:

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 

---


## Problem 1: Hypercube graph

The *hypercube graph* $Q_n$ is the graph formed as follows: 

* The vertices of $Q_n$ are the integers $0,1,2,\dots, 2^n - 1$ written in binary form as an $n$-bit string. 
* Two vertices of $Q_n$ are connected by an edge if their binary strings differ in exactly one place. 

For example, the hypercube graph $Q_3$ has eight vertices: `000`, `001`, `010`, `011`, `100`, `101`, `110`, and `111` (the numbers 0 through 7, in binary as 3-bit strings). The vertices `000` and `001` are connected by an edge, as are `000` and `010`; but `001` and `010` are not connected by an edge. (There are more edges than just these.) 

If you want to visualize $Q_3$, you can do so in networkX: 

```python=
import networkx as nx
G = nx.hypercube_graph(3)
nx.draw(G, with_labels = True, node_color = "lime")
```

Find a formula that gives you the number of edges in $Q_n$ for any positive integer $n$, as a function of $n$, and prove that your formula is correct. (Remember, examples do not prove correctness; you should play with examples, and will need to do so to come up with a formula. But examples should not appear in your writeup.)


## Problem 2: More than one MST? 

We saw in class that an unweighted graph can have a lot of different spanning trees. We said that a *weighted* graph could potentially have more than one *minimum* spanning tree but the example we did with Prim's and Kruskal's algorithm only produced a single MST. So here's a pair of problems about whether a weighted graph can have more than one MST or whether the MST must be unique. 

1. Suppose you have a weighted graph in which two edges have the same weight. Give a small example (4–5 vertices) of such a graph where either Prim's algorithm or Kruskal's algorithm leads to two different MSTs of equal total weight. Verify that both are valid MSTs and show your steps. 
2. Suppose all edge weights in a graph are *different*. Prove (or give a careful argument) that the MST is unique in this case. (Hint: Assume two different MSTs exist and consider the lowest-weight edge that appears in one but not the other.)

## Problem 3: Rooted trees

A **rooted tree** is a tree in which one vertex has been designated as the root. This gives the tree a natural hierarchical structure: parent-child relationships, levels, ancestors, and descendants. [The vault has this article which gives some terminology pertaining to nodes in a rooted tree](https://publish.obsidian.md/discretecs/Trees/Rooted+tree).  

1. Consider the following rooted tree $T$ with root $r = A$, defined by its parent relationships:

| Vertex | Parent |
|--------|--------|
| $A$    | (root) |
| $B$    | $A$    |
| $C$    | $A$    |
| $D$    | $B$    |
| $E$    | $B$    |
| $F$    | $C$    |
| $G$    | $D$    |
| $H$    | $D$    |
| $I$    | $F$    |

Draw the tree $T$ with $A$ at the top. Then answer the following, justifying each answer with a brief explanation:

- What is the **height** of $T$?
- Which vertices are **leaves**?
- What is the **depth** of vertex $F$?
- List all **ancestors** of vertex $H$.


2. A rooted tree is called **complete $m$-ary** if every internal node (non-leaf) has exactly $m$ children. Is $T$ above a complete binary tree (complete 2-ary)? If not, identify specifically which internal nodes violate the condition, and describe the *smallest* modification — adding or removing vertices while keeping $A$ as root — that would make it complete binary.
   
3. There is a well-known formula relating the number of internal vertices $i$ and leaves $\ell$ in a full $m$-ary tree (where every internal vertex has *exactly* $m$ children):

$$\ell = (m-1)i + 1$$

Verify this formula for the case $m = 2$ by constructing *two different* full binary trees with exactly 4 internal vertices. Confirm that both have the number of leaves predicted by the formula, and explain in one or two sentences why the formula holds intuitively — without just citing a proof.

4. A software company stores its file system as a rooted tree where the root is the top-level directory, internal nodes are subdirectories, and leaves are individual files. Suppose a directory tree has height 4 and is a complete 3-ary tree (every subdirectory contains exactly 3 items).

- How many **files** (leaves) does the system contain?
- How many **total nodes** (files + directories) are in the tree?
- If the company wants to add a new level to the bottom of the tree, maintaining the complete 3-ary structure, how many **new files** would be added?

Show your work using the relevant formulas for complete $m$-ary trees.