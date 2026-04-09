# MTH 325 Learning Target Exam 3 -- Solutions and Notes 

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