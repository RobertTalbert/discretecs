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

**Analysis of the proposed proof:** The overall logic of this proof is to claim that each factor of $n!$ is greater, individually, than its corresponding factor in $3^n$, and therefore when multiplying these all together we will get a bigger number for $n!$. This approach would work, except for a logic flaw: It claims that the first three factors of $n!$ multiply to $6$ which is indeed greater than $3$, but this fact is irrelevant because it is no longer comparing one factor of $n!$ with a single factor of $3^n$. Instead it is grouping several factors of $n!$ together and saying their product is greater than a single factor of $3^n$. Because we are no longer at that point comparing factors individually, the logic of the argument breaks down. 

### Notes

- A number of submissions used $n=6$ as the base case not $n=7$. 
- Both here and in option 2 some submissions are using imprecise language to refer to the inductive hypothesis, for example "We will assume that *it* is true for $n=k$" (without stating what the "it" is referring to) or "We will assume $P(k)$ is true" (without stating what $P(k)$ says). Always give the framework in pr

## Option 2

The pre




> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA5NDg0OTI2NV19
-->