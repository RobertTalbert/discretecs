# MTH 325: Fundamental properties of trees


## Part 1: Tree or no? (4 minutes)

For each graph below, determine if it is a tree. If not, explain why.

**Graph A:**
```
    1 — 2
    |   |
    3 — 4
```

**Graph B:**
```
    1 — 2 — 3
        |
        4 — 5
```

**Graph C:**
```
    1 — 2 — 3
    |       |
    4 — 5 — 6
```

**Graph D:**
```
    1   2
    |   |
    3   4
```

**Graph E:**
```
    1
   /|\
  2 3 4
    |
    5
```

**Question 1.1:** Which of the above graphs are trees?

**Question 1.2:** For the non-trees, what would you need to change (add or remove edges) to make them trees?

---

## Part 2: Counting Vertices and Edges (6-7 minutes)

**Question 2.1:** Based on the data collected in the spreadsheet from Class Prep, what pattern do you notice between the number of vertices and the number of edges?

**Question 2.2:** Make a conjecture: For a tree with $n$ vertices, how many edges does it have?

**Question 2.3:** Test this conjecture out by drawing some trees with specific numbers of vertices, then count the edges. 

| Number of Vertices (n) | Draw a Tree | Number of Edges (m) |
| ---------------------- | ----------- | ------------------- |
| 1                      |             |                     |
| 2                      |             |                     |
| 3                      |             |                     |
| 4                      |             |                     |
| 5                      |             |                     |
| 6                      |             |                     |
| 10                     |             |                     |


**Question 2.4:** Prove that your conjecture is true, using one of our proof techniques from class. (Which one "feels" the best?)

---

## Part 3: Paths in Trees (5-6 minutes)

Consider this tree T:

```
        A
       / \
      B   C
     /|   |\
    D E   F G
```

**Question 3.1:** How many different paths are there from vertex A to vertex D?

**Question 3.2:** How many different paths are there from vertex B to vertex G?

**Question 3.3:** Pick any two vertices in the tree above. How many paths exist between them?

**Question 3.4:** Make a conjecture: In ANY tree, how many paths exist between any two vertices?

**Question 3.5:** Suppose a connected graph G has the property that there is exactly one path between every pair of vertices. Must G be a tree? Why or why not?

---

## Part 4: Leaves and Internal Vertices (5-6 minutes)

**Definition:** A **leaf** (or pendant vertex) in a tree is a vertex of degree 1. An **internal vertex** is a vertex of degree ≥ 2.

**Question 4.1:** In the tree from Part 3, identify all the leaves and all the internal vertices.

**Question 4.2:** Draw several different trees with exactly 8 vertices. For each tree you draw, count the number of leaves.

| Your Tree | Number of Leaves |
|-----------|------------------|
| Tree 1    |                  |
| Tree 2    |                  |
| Tree 3    |                  |

**Question 4.3:** What is the minimum number of leaves a tree with 8 vertices can have?

**Question 4.4:** What is the maximum number of leaves a tree with 8 vertices can have?

**Question 4.5:** Make a conjecture: What is the minimum number of leaves that ANY tree must have? (Consider trees with different numbers of vertices)

---

## Part 5: Alternative Characterizations (3-4 minutes)

We defined a tree as "a connected graph with no cycles." However, there are other equivalent ways to define a tree.

**Question 5.1:** Based on your work in Part 3, complete this statement:

"A tree is a graph in which there is exactly _____________ between every pair of vertices."

**Question 5.2:** Based on your work in Part 2, complete this statement:

"A tree with $n$ vertices is a connected graph with exactly _____________ edges."

**Question 5.3:** Consider these two statements:
- Statement X: "G is a connected graph with $n$ vertices and $n-1$ edges"
- Statement Y: "G is a tree"

Do you think X implies Y? That is, if a graph satisfies Statement X, must it be a tree?

**Question 5.4:** What about the reverse direction? If G is a tree (Statement Y), must it satisfy Statement X?

---

## Part 6: Challenge Problems (If Time Permits)

**Challenge 1:** Prove that every tree with at least 2 vertices has at least 2 leaves.

*Hint: Think about starting at any vertex and following a path as far as you can go without repeating vertices.*

**Challenge 2:** Suppose you have a tree T with 15 vertices. You know that 3 vertices have degree 3, and 2 vertices have degree 4. How many leaves does this tree have?

*Hint: Use the handshaking lemma and the relationship between vertices and edges in trees.*

**Challenge 3:** True or False: If you remove any edge from a tree, the resulting graph is disconnected.

**Challenge 4:** True or False: If you add any edge to a tree (connecting two existing vertices), the resulting graph contains a cycle.
