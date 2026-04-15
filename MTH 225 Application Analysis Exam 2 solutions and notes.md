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

#### Notes

- A number of submissions used $n=6$ as the base case not $n=7$. 
- Both here and in option 2 some submissions are using imprecise language to refer to the inductive hypothesis, for example "We will assume that *it* is true for $n=k$" (without stating what the "it" is referring to) or "We will assume $P(k)$ is true" (without stating what $P(k)$ says). Always give the framework in precise terms using the actual language of the predicate. 
- A number of solutions just didn't do the analysis of the proof. 

### Option 2

The predicate here is 

$$P(n): 1 + 2 + \cdots + n = \frac{n(n+1)}{2}$$

**Verification of base case:** The base case is when $n=1$. We want to show $P(1)$ is true. In this case the left side of the equation in $P(n)$ is just the single number $1$ with no other terms. The right side is $\frac{1(2)}{2}$ and this equals $1$. Since the left and right sides equal each other, the base case is verified. 

**Inductive hypothesis:** Assume for some $k$ that $1 + 2 + \cdots + k = \frac{k(k+1)}{2}$. 

**Inductive step:** We need to prove that $1 + 2 + \cdots + (k+1) = \frac{(k+1)(k+2)}{2}$. 

**Outline of a proof:** Several approaches are possible. Here is a sample:

- We might start with the inductive hypothesis which we have assumed to be true: $1 + 2 + \cdots +k = \frac{k(k+1)}{2}$. 
- Then add $k+1$ to both sides to get $1 + 2 + \cdots +k + (k+1) = \frac{k(k+1)}{2} + k+1$. 
- Then do a bunch of algebra and hopefully get the two sides equal to each other. 

This is enough for a reasonable outline. [A full proof can be found in the vault](https://publish.obsidian.md/discretecs/Proof/Mathematical+induction). 

#### Notes

- See Option 1 notes for some common errors on both parts. 
- A number of solutions did not write a sum for the left side but only involved the last term, for example saying that we will assume $k = \frac{k(k+1)}{2}$. This is a fundamental misunderstanding of the predicate, which says that a **sum of** numbers equals a fraction, not that a **single** number does. 

## Part C (Functions and sets) 

### Option 1

(a) This function would be neither injective nor surjective. It would not be surjective because the only outputs possible are the ones that correspond to days of the year: 0 through 364. Anything larger than 365 would never be output. It would not be injective because in a space of 20000 people there must be at least one pair with the same birthday. 

(b) Assuming nobody has the same full name, this function would be both injective and surjective. 


### Option 2

First of all here is a partial table of outputs, which would be sufficient for reasoning in the main problem: 

|$x$| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 
|--|--|--|--|--|--|--|--|--|--|--|
|$f(x)$| 0 | 1 | -1 | 2 | -2 | 3 | -3 | 4 | -4 | 5 | 


(a) The function appears to be a bijection from $\mathbb{N}$ to $\mathbb{Z}$. There are no collisions and every integer appears to be represented in the outputs (or will be, eventually). 

(b) Because this function is a bijection from $\mathbb{N}$ to $\mathbb{Z}$, the cardinalities of the two sets are **the same** (equal). The bijection provides a one-to-one pairing of natural numbers to integers without any integer left "uncovered". 


## Part D

### Option 1

Selecting a password under this system involves the following sequence of three choices: 

- First, pick the positions where the two vowels will go. 
- Second, pick the actual vowels that go in those positions. 
- Third, pick the characters that go in the other six positions. 

We just need to count the number of outcomes of each choice. 

- The number of ways to position the two vowels among eight characters is $\binom{8}{2}$. This number equals $\binom{8}{2} = \frac{8!}{2! 6!} = \frac{8 \cdot 7}{2} = 28$. 
- The number of ways to pick the actual vowels is $5^2$ because there are two of these vowels and each one has $5$ options. 
- The remaining six characters can be chosen freely from the alphabet so there are $26^6$ ways to do that. 

Therefore the count is
$$\binom{8}{2} \cdot 5^2 \cdot 26^6 = 28 \cdot 25 \cdot 308915776 = 216241043200.$$


### Option 2

The creation of the delegation involves the following choices: 

- First pick the two faculty members. Note, it says two faculty members must be on the delegation but one of those has to be the department chair so you are really just picking 



> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA3MTI5NDY4M119
-->