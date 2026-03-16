# MTH 325 Learning Target Exam 2 Solution Guide 

## Learning Target 1

1. The base case is when $n = 1$. In that case, we get $8^1 - 3^1$ which equals $5$ and this is clearly divisible by $5$. 
2. Assume that $8^k - 3^k$ is divisible by $5$ for some $k$. 
3. Prove that $8^{k+1} - 3^{k+1}$ is divisible by $5$.

### Notes

- Remember that the quantifier in part two must be correct. It must say "for some" and not "for all". If the quantifier wrong, this is considered a minor error, and you get up to two of those before you are downgraded on this item. 
- The word "Assume" must also appear at the beginning of the inductive hypothesis in part two. Otherwise, the reader of your proof will not know what you intend to do with the statement that follows. In other words, you cannot just write,  "$8^k - 3^k$ is divisible by $5$ for some $k$." You must clearly indicate that you are assuming that this is correct. Failing to do so is considered a minor error, and you get up to two of those before you're downgraded on this item. 
- Similarly, the word "Prove" must show at the beginning of the inductive step in part three. Failing to do so is considered a minor error, etc., etc. 


## Learning Target 2

First of all pardon the bad English in the proposition statement. ("$b$ is odd integers")

1. Assume that $a$ is even and $b$ is odd. Then prove that $a+b$ is odd. 
2. Assume that $a+b$ is even. Then prove that *either* $a$ is odd *or* $b$ is even. 
3. Assume the following: $a$ is even, $b$ is odd, and that $a+b$ is even. 

### Notes

- Remember that a proof by contradiction starts by assuming the negation of the proposition you are proving. And the negation of "if P then Q" is "P and not Q".  So in a contradiction proof, there is never a statement of exactly what you're going to prove. There's only a statement of all the assumptions that are being made. Notice that is how part 3 is phrased on the exam form. In this case, because the hypothesis has two statements in it, you're actually assuming three things: Both parts of the hypothesis and the negation of the conclusion. 
- Because of [De Morgan's Laws](https://publish.obsidian.md/discretecs/Logic/DeMorgan's+Laws) from logic, the negation of the hypothesis of this statement that appears in part 2 is an "or" statement: Either $a$ is not even *or* $b$ is nod odd. If you put "and" instead of "or", I counted that as a simple error and you get up to two of those before you're downgraded. 
- A number of submissions in part 2 said to prove that either $a$ is *even* or $b$ is *odd*. Everything else was correct. Technically, this is not wrong because the proposition is stating that an even integer plus an odd integer is odd, regardless of how we label them. However, because the proposition itself labels $a$ as the even one to start with and $b$ the odd one, having these mislabeled in the contrapositive is a logic error. 


## Learning Target 3

1. 1
2. 3, 3, 2, 2, 1, 1
3. 4
4. Several right answers possible, for example: 1, 0, 1. 
5. Several right answers possible, for example: 1, 0, 3, 5, 0, 1. 
6. [Go to the vault](https://publish.obsidian.md/discretecs/Graphs/Complete+graph) for a picture of $K_6$. The graph $C_5$ is just a pentagon. 
   
### Notes 

- Several submissions on parts four and five gave examples of walks or closed walks that did have the properties stated rather than those that did not. For example, giving a walk that was claimed not to be a trail, but it actually was a trail. A trail is a walk with no repeated edges. So to find a walk that isn't a trail, you just have to repeat an edge. Similarly, a closed walk that fails to be a circuit would be any closed walk that repeats an edge. 

## Learning Target 4

1. Adjacency matrix: 

$$\begin{bmatrix}
0 & 0 & 1 & 1 & 0 & 0 \\
0 & 0 & 1 & 1 & 1 & 0 \\
1 & 1 & 0 & 1 & 1 & 0 \\
1 & 1 & 1 & 0 & 0 & 1 \\
0 & 1 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 \\
\end{bmatrix}$$

2. Dictionary: 
```python
{0: [2,3], 1: [2, 3, 4], 2: [0, 1,3, 4], 3: [0,1,2,5], 4: [1,2], 5:[3]}
```

## Learning Target 7

1. DFS: 

| Stack | Visited | 
| ---- | ---- | 
| [0] | [ ] | 
| [7, 5, 2, 1] | [0] | 
| [7,5,2] | [0, 1] | 
| [7,5,6,3] | [0, 1, 2] | 
| [7,5,6,4] | [0, 1, 2, 3] | 
| [7,5,6] | [0,1,2,3,4] |
| [7,5] |  [0,1,2,3,4,6] | 
| [7] |  [0,1,2,3,4, 6, 5] | 
| [] |  [0,1,2,3,4, 6, 5, 7] | 


2. BFS: 

| Queue | Visited | 
| ---- | ---- | 
| [0] | [ ] | 
| [1,2,5,7] | [0] | 
| [2,5,7] | [0,1] | 
| [5,7,3,6] | [0,1,2] | 
| [7,3,6] | [0,1,2,5] | 
| [3,6] | [0,1,2,5,7] | 
| [6,4] | [0,1,2,5,7,3] | 
| [4] | [0,1,2,5,7,3,6] | 
| [] | [0, 1, 2, 5, 7, 3, 6, 4] | 


### Notes

- Most people's BFS looked fine but in DFS, the nodes were added in the reverse order that they should have been in step 1 --- it was [1,2,5,7] instead of [7,5,2,1]. 
- A number of submissions on the depth first search part did not add all of the neighbors of node 0 after step one. Only node 1 was added. 
- I think a lot of the confusion on this item stemmed from a not-very-good explanation on my part in class and in the vault. So you can expect some additional class coverage on this coming soon.  

## Learning Target 8

1. (Prim's Algorithm) AC, CG, GJ, JI, CE, EB, AD, DH, HF. 
2. (Kruskal's Algorithm) GJ, FB, CG, AC, FH, IJ, CE, AD, DH. 

### Notes 

- A weirdly large number of submissions used edge AB instead of CE in both algorithms. 
- Remember always to reality check your work. You can do that here in a couple of ways. First, you would need to check to make sure that the resulting minimum spanning tree has nine edges because this is a tree that connects ten nodes. Second, you can take a calculator and find the total weight of each tree, and if they are not the same, then one of those two trees is wrong. 