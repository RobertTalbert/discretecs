---
tags: mth325-f22
---

# Content Skill Standard Quiz 2

:::info
This quiz contains *new versions* of  **Content Skill Standards P.1 and P.2** and *introduces* **Content Skill Standards P.3, G.1, G.2, and G.3**. 

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

>For all positive integers $n$, $1 + 2 + 4 + 8 + \cdots + 2^n = 2^{n+1} - 1$. 

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

>Let $f$ be any function. If $f$ is differentiable, then $f$ is continuous. 

Note that you do not have to know what the words mean in order to work this problem. (It's a theorem from calculus.) 

1. Clearly state what you would assume and what you would prove, if proving this statement with a *direct proof*. 
2. Clearly state what you would assume and what you would prove, if proving this statement with a *proof by contrapositive*.
3. Clearly state *all* the assumptions you would make, if proving this statement *by contradiction*. 

**Success criteria:** All parts of each of the three items here are correctly and clearly stated. 

## :new: Content Skill Standard P.3

:::warning
P.3: I can conduct a critical analysis of a proposed proof of a logical proposition.
:::

Below is a proposition and a proposed proof. Read both carefully and then categorize them in one of the following ways: 

- *The proposition is false.* If this is the case, give a specific counterexample that shows the proposition is false. 
- *The proposition is true but the proof has a fundamental flaw.* If this is the case, find at least one of those fundamental flaws and explain why it makes the proof incorrect. 
- *The proposition is true and there are no fundamental flaws in the proof.* If this is the case, say so, and then give one possible suggestion for improving the clarity or correctness of the proof. 

Be sure to state which of the three categories to which you believe the proposition and proposed proof belong. 

:::success
**Proposition:** For all real numbers $x$ and $y$, $\sqrt{x^2 + y^2} > 2xy$. 
**Proposed proof:** We use proof by contradiction. So suppose $\sqrt{x^2 + y^2} \leq 2xy$. Squaring gives $x^2 + y^2 < 2xy$. Subtracting $2xy$ from both sides gives $x^2 - 2xy - y^2 \leq 0$. Factoring the left side of this gives $(x-y)^2 \leq 0$. But this is a contradiction because $(x-y)^2$ is a perfect square and therefore cannot be negative. So it must be the case that $\sqrt{x^2 + y^2} > 2xy$. :black_medium_small_square: 

:::

**Success criteria:** The work clearly states which of the three categories the proposition and proof belong to. If there is a counterexample, it is specifically and clearly stated. If there is a fundamental flaw, it is specifically and clearly stated, and the nature of the flaw is clearly explained. If there are no fundamental flaws, this is clearly stated and a plausible suggestion for improvement is given. 

## :new: Content Skill Standard G.1

:::warning
★ G.1: I can represent a graph in different ways and change representations from one to another.
:::

Consider the graph $G$, shown below as a visual: 
![](https://i.imgur.com/M75EpPe.png)


Write $G$ as: 

1. An edge list 
2. A Python dictionary
3. An adjacency matrix

**Success criteria:** All representations are correct, with up to two errors (for example, forgetting one node, or getting one bit wrong in the matrix) allowed. 


## :new: Content Skill Standard G.2

:::warning
★ G.2: I can determine information about a graph and its individual vertices and edges using different representations.
:::

1. Consider the graph given by the Python dictionary:
```python=
{0: [3, 4], 1: [2, 5, 7], 2: [1, 3, 5, 6, 7], 3: [0, 2, 4, 5, 6, 7], 
 4: [0, 3, 5, 6], 5: [1, 2, 3, 4, 7], 6: [2, 3, 4], 7: [1, 2, 3, 5]}
```
State (a) the degree sequence and (b) the number of edges in this graph, and give a complete and correct explanation of how you got your answers. (Do not just use Python to generate the graph; use math concepts from the class.)

2. Consider the graph given by the edge list: 
```python=
[(0, 2), (0, 3), (0, 4), (1, 2), (1, 3), (1, 5), (1, 6), 
 (2, 4), (2, 5), (2, 6), (2, 7), (3, 6), (4, 5), (4, 6)]
```
State the degree of node 5 and explain how you got the answer. 


**Success criteria:** All answers are correct and explanations are complete, correct, and clear (and do not just use Python to generate a visual of the graph). 

## :new: Content Skill Standard G.3

:::warning
G.3: I can give examples of graphs having combinations of various properties or explain why no such example exists, and I can draw examples of special ("named") graphs.
:::

1. Draw (by hand) the following graphs. Be sure to draw neatly and label which one is which: 
    (a) $K_4$
    (b) $K_{2,4}$ 
    (c) $C_4$ 
    (d) $P_4$ 
    
2. For each item below, give an example of a graph that has the stated combination of properties. If it is not possible to give an example, explain why. 
    (a) A graph with degree sequence 2, 2, 1, 1
    (b) A graph with degree sequence 2, 2, 2, 2, 2, 2, 2, 1
    (c) A graph with 7 vertices and 3 edges
    (d) A graph with 3 vertices and 7 edges
    
    
**Success criteria:** All four graphs in the first part are drawn correctly. All items in part (2) are correctly identified as being either possible or not possible; for those that are possible, a correct example is given, and for those that are not, a correct and clear explanation is given that uses mathematical concepts from the course. 