# Exam 4 makeup -- selected answers

## Skill 1

> **(CORE)** I can outline a proof by mathematical induction.

Consider the following proposition, and suppose we want to prove it with mathematical induction: 

**For any integer $n \geq 1$, the number $n^3 + 2n$ is an integer multiple of $3$.** 

1.	State the value of $n$ that corresponds to the base case, then prove that the base case holds. 
2.	Clearly state the inductive hypothesis. Your answer should be phrased as a complete sentence. (No explanation is required here; simply state the inductive hypothesis.) 
3.	Clearly state what you would need to prove, after assuming the inductive hypothesis. Your answer should be phrased as a complete sentence. (You do not need to give a completed proof the statement; simply state what you would need to prove.) 


**Answers:**

1. The base case is $n=1$. In this case, we have the number $1^3 + 2(1)$. This equals 3, which is an integer multiple of 3 (namely, $1 \times 3$) so the base case holds. 
2. Assume that for some $k \geq 1$, $k^3 + 2k$ is an integer multiple of 3. 
3. Prove that $(k+1)^3 + 2(k+1)$ is an integer multiple of 3. 


---

## Skill 2

> **(CORE)** I can outline a proof using direct, contrapositive, and indirect approaches. 

Consider the proposition: **If $2^n$ is a prime number, then $n$ is a prime number.** 

1. Clearly state what you would assume and what you would prove if you were to prove this statement with a *direct proof*. 
3. Clearly state what you would assume and what you would prove if you were to prove this statement with a *proof by contrapositive*. 
2. Clearly state all the assumptions you would make if you were to prove this statement with a *proof by contradiction*, also known as an *indirect proof*.  

**Answers:**

1. Assume that $2^n$ is prime. Prove that $n$ is prime. 
2. Assume that $n$ is not prime. Prove that $2^n$ is not prime. 
3. Assume that $2^n$ is prime and also assume that $n$ is not prime. 

---

## Skill 12

> I can use the Floyd-Warshall algorithm to construct the transitive closure of a directed graph. 

Consider the adjacency matrix below: 

$$\left(
\begin{array}{cccc}
 0 & 1 & 1 \\
 1 & 1 & 0  \\
 1 & 0 & 0  \\
\end{array}
\right)$$

Assume that the vertices are 0, 1, 2 and that the rows and columns correspond to those vertices in this order. 

1. Complete the table below for the first six steps of Warshall’s algorithm. The first two rows have the values for the counters in the loops filled in for you. The other values of the loop counters must be done in the correct order given by the pseudocode for Warshall’s algorithm given in class. 
2. 

| $k$ | $i$ | $j$ | $W[i,j]$ | $W[i,k]$ | $W[k,j]$ | Result |
| --- | --- | --- | -------- | -------- | -------- | ------ |
| 0   | 0   | 0   | 0        | 0        | 0        | 0      |
| 0   | 0   | 1   | 1        | 0        | 1        | 1      |
| 0   | 0   | 2   | 1        | 0        | 1        | 1      |
| 0   | 1   | 0   | 1        | 1        | 0        | 1      |
| 0   | 1   | 1   | 1        | 1        | 1        | 1      |
| 0   | 1   | 2   | 0        | 1        | 1        | 1      |


2. Complete the step in Warshall’s algorithm correspoinding to k = 1, i = 1, and j = 2. 

| $k$  | $i$  | $j$  | $W[i,j]$ | $W[i,k]$ | $W[k,j]$ | Result |
| ---- | ---- | ---- | -------- | -------- | -------- | ------ |
| 1    | 1    | 2    |     0     |    1      |     0     |  0      |