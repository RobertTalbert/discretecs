# Mini Exam on Core Skills -- MTH 325 F24

Before starting, make sure you know which Skills you need to attempt. **Turning in work on any  Skill on which you have already attained a rating of Master, then 5 engagement credits per problem will be deducted from your total.**

## Skill 1

> **(CORE)** I can outline a proof by mathematical induction.

Consider the following proposition, and suppose we want to prove it with mathematical induction: 

**For every integer $n \geq 1$, a set with $n$ elements has $2^n$ subsets.** 

1.	State the value of n that corresponds to the base case, then prove that the base case holds. 
2.	Clearly state the inductive hypothesis. Your answer should be phrased as a complete sentence. (No explanation is required here; simply state the inductive hypothesis.) 
3.	Clearly state what you would need to prove, after assuming the inductive hypothesis. Your answer should be phrased as a complete sentence. (You do not need to give a completed proof the statement; simply state what you would need to prove.) 

## Skill 2

> **(CORE)** I can outline a proof using direct, contrapositive, and indirect approaches.

Consider the following proposition: **For all real numbers $x$, if $x \geq 10$ then $x^2 \geq 25$.** 

1. Clearly state what you would assume and what you would prove if you were to prove this statement with a *direct proof*. 
2. Clearly state all the assumptions you would make if you were to prove this statement with a *proof by contradiction*. 
3. Clearly state what you would assume and what you would prove if you were to prove this statement with a *proof by contrapositive.*

## Skill 3

> **(CORE)** I can represent a graph in different ways, determine information (degree, degree sequence, paths of given length, etc.) about a graph using different representations, and give examples of graphs with specified properties.

Here is the Python dictionary for a graph: 

```python
{0: [1, 2, 3], 1: [0, 3, 4, 7], 2: [0, 5], 3: [0, 1, 4, 5, 6], 4: [1, 3, 6], 5: [2, 3], 6: [3, 4, 7], 7: [1, 6]}
```

1. Write the adjacency matrix for this graph. Assume the rows and columns are indexed $0, 1, 2, \dots, 7$ in that order. 
2. Draw a picture of this graph. 
3. State the degree of each vertex. 
4. Find the number of edges in the graph. Show your work and explain your reasoning. 

## Skill 7

> **(CORE)** I can determine whether a graph is a tree and state information about it.

1. A graph $G$ has degree sequence 3, 2, 2, 2, 1. Which of the following statements is true? (a) $G$ **must** be a tree; (b) $G$ **might** be a tree but might not be one; or  (c) $G$ **cannot** be a tree? Clearly state your choice, then explain your reasoning. 

2. Consider the following rooted tree with vertex 1 designated as the root: 

   ```mermaid
   graph TD
       1[1]
       2[2]
       3[3]
       4[4]
       5[5]
       6[6]
       7[7]
       8[8]
       9[9]
       10[10]
       11[11]
       12[12]
       
       1 --- 2
       1 --- 3
       1 --- 4
       2 --- 5
       2 --- 6
       3 --- 7
       4 --- 8
       5 --- 10
       6 --- 11
       7 --- 12
       8 --- 9
   ```

   (a) State the children of vertex 2. 

   (b) State the height of the tree. 

   (c) State the parent(s) of vertex 8. 

   (d) State all the leaves of the tree. 

## Skill 11

> **(CORE)** I can represent a directed graph in different ways, and determine information about a graph using different representations.

Consider the following directed graph $G$ given as an adjacency matrix: 
$$
\begin{bmatrix}
0 & 0 & 1 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\
1 & 0 & 0 & 0 & 0 & 0 & 0 & 0
\end{bmatrix}
$$
Assume the vertices are $0, 1, 2, \dots, 7$ and the rows and columns are indexed accordingly. 

1. Write the Python dictionary for $G$. Be sure to use correct Python dictionary syntax (for example `{a: [b,c], b:[c,d]}`).
2. Without drawing the graph, find the number of edges in $G$ and explain your reasoning. 
3. Draw a picture of the graph. 
4. State the in- and out-degrees of each vertex. 