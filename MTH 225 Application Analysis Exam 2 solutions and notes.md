# MTH 225 Application Analysis Exam 2 solutions and notes 

## Part A -- Multiple Choice

1. B
2. A
3. B
4. A
5. B
6. A
7. A
8. C
9. A
10. C 

## Part B -- Mathematical Induction

**Reminder:** The *framework* for an induction proof consists of three things: 
1. A verification of the base case 
2. A statement of the inductive hypothesis
3. A statement of the inductive step

It also helps to have a clear statement of the predicate involved. 

### Option 1

The predicate here is

$$P(n):  3^n < n!$$

**Verification of base case:** The base case is when $n = 7$. We want to show $P(7)$ is true -- in other words we want to verify that $3^7 < 7!$. We can do this by computing the left and right sides directly: $3^7 = 2187$ and $7! = 5050$. We can see that $2187 < 5040$ so the base case is verified. 

**Inductive hypothesis:** Assume that for some $k$, $3^k < k!$. 

**Inductive step:** Prove that $3^{k+1} < (k+1)!$ 

**Analysis of the proposed proof:** The overall logic of this proof is to claim that each factor of $n!$ is greater, individually, than its corresponding factor in $3^n$, and therefore when multiplying these all together we will get a bigger number for $n!$. This approach would work, except for a logic flaw: It claims that the first three factors of $n!$ multiply to $6$ which is indeed greater than $3$, but this fact is irrelevant because 


The proposed proof has a flaw in its logic that makes it incorrect: When looking at the first three factors of $n!$, we do indeed have $1 \cdot 2 \cdot 3$ but those multiply to $6$. The proposed proof correctly points out that this is greater than $3$, but this fact is irrelevant. The logic of the 


, whereas the first three factors of $3^n$ multiply to  $3 \cdot 3 \cdot 3 = 27$. The proof correctly states that the 

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNjgxMTk0MTZdfQ==
-->