---
tags: mth325-f22
---

# Content Skill Standard Quiz 4

:::info
This quiz contains *new versions* of  **Content Skill Standards P.1-P.3 and G.1-G.4** and *introduces* **Content Skill Standards G.5 and G.6**. 

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

>For all positive integers $n$, a set with $n$ elements has $2^n$ subsets. 

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

>Suppose $G$ and $H$ are graphs. If $G$ and $H$ are isomorphic and $G$ is connected, then $H$ is connected. 


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
**Proposition:** For all integers $n \geq 4$, $n! > 2^n$. 
**Proposed proof:** Suppose that $k! > 2^k$ for some integer $k \geq 4$. We want to show that $(k+1)! > 2^{k+1}$. 

The left side of the inequality to prove, $(k+1)!$, can be rewritten as $(k+1) \cdot k!$. Using the inductive hypothesis above, we therefore conclude that 
$$(k+1)! = (k+1) \cdot k! > (k+1) \cdot 2^k$$
And since $k \geq 4$, it follows that $k+1 \geq 5$ and therefore $k+1 > 2$. This produces the chain of inequalities: 
$$(k+1)! > (k+1) \cdot 2^k > 2 \cdot 2^k = 2^{k+1}$$
Hence $(k+1)! > 2^{k+1}$, which is what we wanted to show.:black_medium_small_square: 

:::

**Success criteria:** The work clearly states which of the three categories the proposition and proof belong to. If there is a counterexample, it is specifically and clearly stated. If there is a fundamental flaw, it is specifically and clearly stated, and the nature of the flaw is clearly explained. If there are no fundamental flaws, this is clearly stated and a plausible suggestion for improvement is given. 

## Content Skill Standard G.1

:::warning
★ G.1: I can represent a graph in different ways and change representations from one to another.
:::

Consider the graph $G$ given below as an adjacency matrix: 

|vertex |0|1|2|3|4|5|
|---|---|---|---|---|---|---|
|0|0\.0|0\.0|0\.0|1\.0|1\.0|0\.0|
|1|0\.0|0\.0|1\.0|0\.0|1\.0|1\.0|
|2|0\.0|1\.0|0\.0|1\.0|1\.0|0\.0|
|3|1\.0|0\.0|1\.0|0\.0|0\.0|0\.0|
|4|1\.0|1\.0|1\.0|0\.0|0\.0|1\.0|
|5|0\.0|1\.0|0\.0|0\.0|1\.0|0\.0|

Write $G$ as: 

1. An Python dictionary 
3. An edge list 

**Success criteria:** All representations are correct, with up to two errors (for example, forgetting one node, or getting one bit wrong in the matrix) allowed. 


## Content Skill Standard G.2

:::warning
★ G.2: I can determine information about a graph and its individual vertices and edges using different representations.
:::

Consider the graph given by the following dictionary: 
```python=!
{0: [2, 3, 5, 7],
 1: [2, 3, 4, 6],
 2: [0, 1, 5, 6],
 3: [0, 1, 5, 7],
 4: [1],
 5: [0, 2, 3, 7],
 6: [1, 2, 7],
 7: [0, 3, 5, 6]}
```

   (a) State the degree sequence of the graph and briefly explain your reasoning **without using a visualization of the graph -- your explanation must only use the dictionary**. 
   (b) Determine the number of edges in this graph and briefly explain your reasoning **without using a visualization of the graph -- your explanation must only use the dictionary.**
   (c) Determine if it is possible to travel from node 1 to node 5 along a sequence of edges in this graph. If it is, give a sequence of edges that does so. If it is not, explain why. **Do not use a visualization of the graph  -- your explanation must only use the dictionary.**


**Success criteria:** All answers are correct and explanations are complete, correct, and clear (and do not use visualizations of the graph). 

## Content Skill Standard G.3

:::warning
G.3: I can give examples of graphs having combinations of various properties or explain why no such example exists, and I can draw examples of special ("named") graphs.
:::

1. Draw (by hand) the following graphs. Be sure to draw neatly and label which one is which: 
    (a) $K_{2,3}$
    (b) $K_4$
    (c) $C_4$
    
2. For each item below, give an example of a graph (or pair of graphs, if appropriate) that has the stated combination of properties. If it is not possible to give an example, explain why. 
    (a) A graph with exactly one vertex of degree 1
    (b) A graph with exactly one vertex of odd degree
    (c) A graph with five vertices that does not have a cycle of length 5
    
**Success criteria:** All graphs in part 1 are correctly drawn. All parts of part 2 are correct with specific, correct examples given, or in the case of an impossible situation a correct and clear explanation is given. 
    
## Content Skill Standard G.4

:::warning
G.4: I can determine whether two graphs are isomorphic; I can give an explicit isomorphism if they are, and an explanation if they are not. 
:::
    

1. Are the two graphs below isomorphic? If so, write the isomorphism $f$ as a table of inputs and outputs. If not, give a *specific* reason why not. 

![](https://i.imgur.com/LQpx96f.png)
![](https://i.imgur.com/1JCfcHR.png)



2. Are the two graphs below isomorphic? If so, write the isomorphism $f$ as a table of inputs and outputs. If not, give a *specific* reason why not. 

![](https://i.imgur.com/BYz2NJ1.png)
![](https://i.imgur.com/0sVXcIq.png)

Your explanations must use specific facts about graph isomorphisms. They cannot be general or vague, for example "You can (or can't) rearrange one graph to get the other". [You may use any of the isomorphism invariants found on this list](https://gist.github.com/RobertTalbert/2dadae14f8f42c3654a8a77ef5a038f1) if you like. 


**Success criteria:** If a pair of graphs is isomorphic, a correct isomorphism is given as a table of inputs and outputs. If a pair of graphs is *not* isomorphic, a correct reason is given (which can be pulled from [the list of isomorphism invariants](https://gist.github.com/RobertTalbert/2dadae14f8f42c3654a8a77ef5a038f1)). 

## :new: Content Skill Standard G.5

:::warning
G.5:  I can give a valid vertex coloring for a graph and determine a graph's chromatic number.
::: 

Consider the following graph: 

![](https://i.imgur.com/ugvAJRR.png)

1. Give a valid coloring for the vertices that uses exactly four colors. If this is not possible, explain why. 

2. Determine the chromatic number of the graph. Explain your reasoning by (a) stating the coloring and (b) explaining in one sentence why a smaller coloring is impossible. 

**Success criteria:** In part 1, a proper coloring is explicitly stated that uses the stated amount of colors. In part 2, the chromatic number is correct; a proper coloring with the right number of colors is given; and there is an explanation for why a smaller coloring is impossible. 

## :new: Content Skill Standard G.6

:::warning
G.6: I can determine whether a graph has an Euler path or Euler circuit, and whether a graph has a Hamiltonian path or cycle.
:::

1. Consider this graph, given as a dictionary: 
```python=!
{0: [2, 3, 5, 7],
 1: [2, 3, 4, 6],
 2: [0, 1, 5, 6],
 3: [0, 1, 5, 7],
 4: [1],
 5: [0, 2, 3, 7],
 6: [1, 2, 7],
 7: [0, 3, 5, 6]}
```
Determine whether this graph has an Euler path; if it does, state that path as a sequence of nodes, and if not, clearly explain why not. Then, repeat this task for Euler cycles. 

2. Consider this graph: 

![](https://i.imgur.com/chFKkzV.png)

Determine whether this graph has a Hamilton path (not necessarily a cycle). If it does, state that path as a sequence of nodes. If not, explain why not. 

**Success criteria:** If a graph has a structure (Euler path, Euler cycle, Hamilton path --- whatever is requested in the problem) then a correct example is stated as a node sequence. If not, a correct and *specific* explanation is given. 