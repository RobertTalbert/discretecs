# MTH 325 Learning Target Exam 3 -- Solutions and Notes 

## Learning Target 5

1. Technically no because there are not exactly two vertices of odd degree. However if you said there was an Euler circuit and this is an example of a special kind of trail, I allowed it. 
2. Yes, it has an Euler circuit: A, B, C, D, E, C, A. (Note our theorem from class would agree since the degree of each vertex is even.)
3. Yes, it has a Hamilton path: A, B, C, D, E. 
4. No, it does not have a Hamilton cycle. If the cycle started at A or B, it would have to cross C once to visit D and E but then again to complete the cycle. Similar reasoning holds for starting at C, D or E. 

### Notes

- Several submissions were mixing up what Euler and Hamilton mean. Euler has to do with edges, Hamilton has to do with nodes. 

---

## Learning Target 8

---

## Learning Target 9

1. Here are the algorithm steps using the table we used in class: 

| Node | Neighbors | Neighbors' colors | NODE COLOR | 
| :--: | :--------: | :--------------: | :--------: | 
| A | C | n/a | 1 | 
| B | E, D | n/a | 1 | 
| C | A, D, E, F | 1 | 2 | 
| D | C, B, E | 1, 2 | 3 | 
| E | B, C, D, F | 1, 2, 3 | 4 | 
| F | C, E | 2, 4 | 1 | 

2. No, the true chromatic number is 3. Here is a proper 3-coloring given as a dictionary: 

```python
{A: 1, B: 2, C: 2, D: 1, E: 3, F: 1}
```

And we know there is no coloring with fewer than 3 colors because of the 3-cycle B, E, D, B. 

### Notes

- A number of submissions did not run the algorithm using the correct node ordering (alphabetical). A key point from class discussion is that the ordering of the nodes at the beginning of the algorithm is critically important because the greedy algorithm is highly sensitive to initial conditions. So it's essential to obey the instructions given to the algorithm in terms of the ordering. 


---

## Learning Target 10 

1. $d^-(1) = 1$ and $d^+(1) = 2$. 
2. `{0: [ ] , 1: [2,4], 2:[3], 3:[ ], 4: [0], 5:[1]}`
3. Below: 

$$\begin{pmatrix}
0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 \\
1 & 0 & 0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & 0 \\
\end{pmatrix}$$


### Notes

- A lot of submissions confused $d^-(1)$ (the in-degree) and $d^+(1)$ (the out-degree). Having the right values but attached to the wrong notation was considered a "simple" error. 
- A lot of submissions did not use correct Python dictionary syntax as directed. **Dictionaries in Python are enclosed in curly braces `{ }`, key-value pairs are separated by commas, and the values are lists enclosed in square brackets `[]`.** Some syntax errors were minor, for example forgetting the ending curly brace or using curly braces instead of square braces. Others were inventing entirely new notations for dictionaries. Minor errors were considered "simple" errors while major deviations from correct syntax were not. 

## Learning Target 11 

*Note: There may be multiple specific concrete examples of property failures that are possible for each part. Here we just list a sample.* 

1. Reflexive and symmetric. But not transitive because $(A,B)$ and $(B,C)$ are in the relation but not $(A,C)$. 
2. Reflexive and transitive. But not symmetric because $(A,B)$ is in the relation but not $(B,A)$. 
3. Not reflexive because $(A,A)$ is not in the relation. Also not symmetric because $(A,B)$ is in the relation but not $(B,A)$. Also not transitive because $(A,B)$ and $(B,C)$ are in the relation, but $(A,C)$ is not. 

### Notes 

- I tweaked the standard on this one to match the present form of this question: You are allowed one incorrect response, or a correct statement that a property fails but the example doesn't work, on this one (out of nine) before being downgraded to Proficient. 
- Which is good because a lot of submissions said $R_3$ was transitive when it is not -- the edge $(C,A)$ is in the relation but the one you need is $(A,C)$. 

---

## Learning Target 12

1. 
| **k** | **i** | **j** | **W[i,j]** | **W[i,k]** | **W[k,j]** | **Result** |
| ----- | ----- | ----- | ---------- | ---------- | ---------- | ---------- |
| 0     | 0     | 0     | 0          | 0          | 0          | 0          |
| 0     | 0     | 1     | 0          | 0          | 0          | 0          |
| 0     | 0     | 2     | 0          | 0          | 0          | 0          |
| 0     | 0     | 3     | 1          | 0          | 1          | 1          |
| 0     | 1     | 0     | 0          | 0          | 0          | 0          |
| 0     | 1     | 1     | 0          | 0          | 0          | 0          |

2. There are several sets of values that work including: 

- $i = 0, j = 0, k = 3$
- $i = 3, j = 3, k = 0$
- $i = 3, j = 3, k = 2$
- $i=2, j=2, k = 3$ 
- $i = 2, j = 1, k = 3$ 

In each of these, the bit in the matrix flips from `0` to `1` because although there is no existing edge from $i$ to $j$, there is an edge from $i$ to $k$ and then from $k$ to $j$. This search for a pivot is what makes Warshall's Algorithm work. 