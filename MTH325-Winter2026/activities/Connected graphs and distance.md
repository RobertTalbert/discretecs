# MTH 325 -- Connected graphs and distance 

## Learning Objectives
By the end of this activity, you will be able to:
- Determine if a graph is connected
- Calculate the distance between any two nodes in a connected graph
- Identify the diameter and radius of a graph
- Work with multiple graph representations

---

## Part 1: Warm-Up Review (5 minutes)

Consider the following graph G represented as a Python dictionary:

```python
G = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F'],
    'D': ['B'],
    'E': ['B', 'F'],
    'F': ['C', 'E']
}
```

- Draw this graph on paper on a whiteboard. 
- For each of the following, determine if it exists in graph G. If yes, give an example:
  - a) A walk of length 4 from A to F
  - b) A path from A to D
  - c) A cycle containing node E
  - d) A trail from C to D that is not a path

Bonus question: How would you do the previous tasks if you didn't have a visualization of the graph but just the dictionary? 

---

## Part 2: Connectivity (5 minutes)

A graph is **connected** if there exists a path between every pair of vertices.

- Is graph G (from Part 1) connected? Justify your answer.

- Consider this new graph H:

```python
H = {
    'A': ['B', 'C'],
    'B': ['A'],
    'C': ['A'],
    'D': ['E', 'F'],
    'E': ['D'],
    'F': ['D']
}
```

Is graph H connected? If not, how many connected components does it have? List the vertices in each component. Try to determine these *without* drawing the graph. 

---

## Part 3: Distance Between Nodes (8-10 minutes)

The **distance** between two vertices u and v, denoted d(u,v), is the length of the shortest path between them. If no path exists, we say d(u,v) = ∞.

Using graph G from Part 1:

- Complete the distance table below by finding the distance between each pair of vertices:

|   | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| A | 0 |   |   |   |   |   |
| B |   | 0 |   |   |   |   |
| C |   |   | 0 |   |   |   |
| D |   |   |   | 0 |   |   |
| E |   |   |   |   | 0 |   |
| F |   |   |   |   |   | 0 |

- For the pair of vertices with the largest distance, write out a shortest path connecting them.

- Are there multiple shortest paths between any pair of vertices? If so, give an example.

---

## Part 4: Diameter and Radius (5-7 minutes)

**Definitions:**
- The **eccentricity** of a vertex v, denoted ecc(v), is the maximum distance from v to any other vertex in the graph.
- The **diameter** of a graph is the maximum eccentricity among all vertices: diam(G) = max{ecc(v) : v ∈ V}
- The **radius** of a graph is the minimum eccentricity among all vertices: rad(G) = min{ecc(v) : v ∈ V}
- A vertex with eccentricity equal to the radius is called a **center** of the graph.

- Using your distance table from Part 3, calculate the eccentricity of each vertex:
  - ecc(A) = 
  - ecc(B) = 
  - ecc(C) = 
  - ecc(D) = 
  - ecc(E) = 
  - ecc(F) = 

- What is the diameter of graph G?

- What is the radius of graph G?

- Which vertex (or vertices) is a center of graph G?

---

## Part 5: Challenge Problem (If Time Permits)

Consider the following adjacency matrix for a graph K:

```
    A  B  C  D  E
A [ 0  1  0  0  1 ]
B [ 1  0  1  1  0 ]
C [ 0  1  0  1  0 ]
D [ 0  1  1  0  1 ]
E [ 1  0  0  1  0 ]
```

- Is this graph connected?
- Without creating a full distance table, determine:
  - The distance d(A, C)
  - The diameter of K
  - At least one center of K

- How is the diameter related to the "compactness" of a network? Why might this be important in computer networks?
