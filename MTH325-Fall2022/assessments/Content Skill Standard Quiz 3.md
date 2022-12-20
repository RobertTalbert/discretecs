---
tags: mth325-f22
---

# Content Skill Standard Quiz 3

:::info
This quiz contains *new versions* of  **Content Skill Standards P.1-P.3 and G.1-G.3** and *introduces* **Content Skill Standard G.4**. 

**Instructions**

* Work only the problems that you **need to work** and **feel ready to work**. 
* Do your work on separate pages with **each Content Skill Standard on its own separate page**. *Please do not put work for multiple Standards on the same page.* 
* Make sure to consult the [Specifications for Student Work in MTH 325](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document before starting on your work, so you're clear on what is expected and what constitutes a "successful" attempt. 
* Also, make sure to carefully read the **Success Criteria** below each problem to know exactly what is expected from that problem. 
* When you are done: **Scan** each Learning Target to a clear, legible, black-and-white PDF and **upload the PDF** to the designated folder on Blackboard. Please  *do not just take a picture with your camera* --- use a scanning app to create a PDF, and upload the PDF. You can also type up your work and save to a PDF if you want; or use a notes app on a tablet to handwrite your work and save that to a PDF. 
:::


## Content Skill Standard P.1 

:::warning
★ P.1: Given a statement to prove with mathematical induction, I can identify the predicate, state and prove the base case, state the inductive hypothesis, and outline the rest of the proof. 
:::

Consider the statement: 

>For all positive integers $n$, $2^n > n$. 

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

>Suppose $G$ and $H$ are graphs. If $G$ and $H$ are isomorphic, then $G$ and $H$ have the same number of edges. 


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

:::success
**Proposition:** For all positive integers $n$, $n^3 + n$ is even. 
**Proposed proof:** We prove this by contradiction. So suppose that $n^3 + n$ is odd. This is a contradiction because there is a counterexample, $n = 1$. In this case $1^3 + 1 = 2$ which is even. Since there is a counterexample to the negation, the original claim that $n^3 + n$ is even must be true. :black_medium_small_square: 

:::

**Success criteria:** The work clearly states which of the three categories the proposition and proof belong to. If there is a counterexample, it is specifically and clearly stated. If there is a fundamental flaw, it is specifically and clearly stated, and the nature of the flaw is clearly explained. If there are no fundamental flaws, this is clearly stated and a plausible suggestion for improvement is given. 

## Content Skill Standard G.1

:::warning
★ G.1: I can represent a graph in different ways and change representations from one to another.
:::

Consider the graph $G$ given below as a Python dictionary: 

```python=
{0: [1, 4], 1: [0, 2, 3, 4], 2: [1, 3, 4, 5], 
 3: [1, 2], 4: [0, 1, 2], 5: [2]}
```

Write $G$ as: 

1. An edge list 
3. An adjacency matrix

**Success criteria:** All representations are correct, with up to two errors (for example, forgetting one node, or getting one bit wrong in the matrix) allowed. 


## Content Skill Standard G.2

:::warning
★ G.2: I can determine information about a graph and its individual vertices and edges using different representations.
:::

Consider the graph given by the following adjacency matrix: 

|vertex|0|1|2|3|4|5|
|---|---|---|---|---|---|---|
|0|0\.0|1\.0|1\.0|0\.0|0\.0|1\.0|
|1|1\.0|0\.0|0\.0|0\.0|0\.0|1\.0|
|2|1\.0|0\.0|0\.0|0\.0|1\.0|1\.0|
|3|0\.0|0\.0|0\.0|0\.0|1\.0|0\.0|
|4|0\.0|0\.0|1\.0|1\.0|0\.0|0\.0|
|5|1\.0|1\.0|1\.0|0\.0|0\.0|0\.0|

   (a) State the degree sequence of the graph and briefly explain your reasoning **without using a visualization of the graph -- your explanation must only use the matrix**. 
   (b) Determine the number of edges in this graph and briefly explain your reasoning **without using a visualization of the graph -- your explanation must only use the matrix.**
   (c) Determine if it is possible to travel from node 1 to node 4 along a sequence of edges in this graph. If it is, give a sequence of edges that does so. If it is not, explain why. **Do not use a visualization of the graph  -- your explanation must only use the matrix.**


**Success criteria:** All answers are correct and explanations are complete, correct, and clear (and do not use visualizations of the graph). 

## Content Skill Standard G.3

:::warning
G.3: I can give examples of graphs having combinations of various properties or explain why no such example exists, and I can draw examples of special ("named") graphs.
:::

1. Draw (by hand) the following graphs. Be sure to draw neatly and label which one is which: 
    (a) $K_{3,3}$
    (b) $K_6$
    (c) $P_3$
    
2. For each item below, give an example of a graph (or pair of graphs, if appropriate) that has the stated combination of properties. If it is not possible to give an example, explain why. 
    (a) A graph with degree sequence 2, 2, 2, 2, 2
    (b) Two graphs $G$ and $H$ that have the same number of vertices and edges, but which are not isomorphic
    (c) A graph with one vertex of degree 5 but all other vertices are degree 2 or less
    
    
## :new: Content Skill Standard G.4

:::warning
G.4: I can determine whether two graphs are isomorphic; I can give an explicit isomorphism if they are, and an explanation if they are not. 
:::
    

1. Are the two graphs below isomorphic? If so, write the isomorphism $f$ as a table of inputs and outputs. If not, give a *specific* reason why not. 

![](https://i.imgur.com/gZPoQOq.png)
![](https://i.imgur.com/vpu6UIa.png)



2. Are the two graphs below isomorphic? If so, write the isomorphism $f$ as a table of inputs and outputs. If not, give a *specific* reason why not. 

![](https://i.imgur.com/JdfOA3f.png)
![](https://i.imgur.com/qrDGziZ.png)

Your explanations must use specific facts about graph isomorphisms. They cannot be general or vague, for example "You can (or can't) rearrange one graph to get the other". [You may use any of the isomorphism invariants found on this list](https://gist.github.com/RobertTalbert/2dadae14f8f42c3654a8a77ef5a038f1) if you like. 


**Success criteria:** All four graphs in the first part are drawn correctly. All items in part (2) are correctly identified as being either possible or not possible; for those that are possible, a correct example is given, and for those that are not, a correct and clear explanation is given that uses mathematical concepts from the course. 