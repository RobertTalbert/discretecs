# MTH 225 Application/Analysis Exam 1 REATTEMPT 1 -- Solution Guide and Notes 

## Part A

1. B
2. C
3. B
4. C
5. A
6. D
7. C
8. D
9. B
10. C

## Part B

### Option 1
<!-- 
To solve $3x \equiv 6 \pmod{12}$ just run through all the integers $0$ to $12$ and check. (Note, *all* integers must be checked, or at least there has to be an explanation about repeated values. Simply finding three values that work, is not enough -- a complete solution must also rule out the values that don't work.)

| $x$ | $3x$ | $3x \pmod{12}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $3$  | $3$  | 
| $2$ | $6$  | $6$  | 
| $3$ | $9$  | $9$  | 
| $4$ | $12$  | $0$  | 
| $5$ | $15$  | $3$  | 
| $6$ | $18$  | $6$  | 
| $7$ | $21$  | $9$  | 
| $8$ | $24$  | $0$  | 
| $9$ | $27$  | $3$  | 
| $10$ | $30$  | $6$  | 
| $11$ | $33$  | $9$  | 
| $12$ | $36$  | $0$  | 

From the table we can see that the solutions are $x = 2, 6, 10$ and those are the only ones. 

Now repeating this for $5x \equiv 6 \pmod{12}$: 

| $x$ | $5x$ | $5x \pmod{12}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $5$  | $5$  | 
| $2$ | $10$  | $10$  | 
| $3$ | $15$  | $3$  | 
| $4$ | $20$  | $8$  | 
| $5$ | $25$  | $1$  | 
| $6$ | $30$  | $6$  | 
| $7$ | $35$  | $11$  | 
| $8$ | $40$  | $4$  | 
| $9$ | $45$  | $9$  | 
| $10$ | $50$  | $2$  | 
| $11$ | $55$  | $7$  | 
| $12$ | $60$  | $0$  | 

Here we see there is only one solution, $x = 6$.  -->



### Option 2

<!-- Here, we make a table of outputs for $3x \pmod{7}$ for $x = 0$ through $x = 6$ and search for a value of $x$ that produces $1$. (We only need to search this range of $x$ values because they will just repeat once we go greater than $6$.) 

| $x$ | $3x$ | $3x \pmod{7}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $3$  | $3$  | 
| $2$ | $6$  | $6$  | 
| $3$ | $9$  | $2$  | 
| $4$ | $12$  | $5$  | 
| $5$ | $15$  | $1$  | 
| $6$ | $18$  | $4$  | 

We can see that $x=5$ is what want. In other words $3^{-1} = 5$. 

To use this fact to solve $3x \equiv 5 \pmod{7}$, multiply both sides of this equivalence by $5$: 

$$\begin{eqnarray*}
3x &\equiv 5 \pmod{7} \\
5 \cdot 3x &\equiv 5 \cdot 5 \pmod{7} \\
(5 \cdot 3)x &\equiv 25 \pmod{7} \\
1x &\equiv 4 \pmod{7}
\end{eqnarray*}$$

The last line is true because $5 \cdot 3 \equiv 1 \pmod{7}$ as shown in the table, and because $25 \pmod{7} = 4$ by definition. Therefore $x = 4$.  -->

### Grading notes for Part B



---

## Part C

### Option 1

<!-- Translated into symbols, the messy statement is: 

$$\neg(((\neg p) \wedge q) \vee ((\neg p) \wedge (\neg r)))$$ 

Using the Distributive Law to "factor out" a $\neg p$ gives us: 

$$\neg ( (\neg p) \wedge (q \vee (\neg r)))$$

Now use DeMorgan's Law to distribute the $\neg$ across the two statements that are joined by $\wedge$: 

$$\neg(\neg p) \vee \neg(q \vee (\neg r))$$ 

The Double Negation law applied to the first term gives: 

$$p \vee \neg(q \vee (\neg r))$$ 

Then another application of DeMorgan's Law to the second term gives: 

$$p \vee ((\neg q) \wedge \neg(\neg r))$$ 

And finally, the Double Negation law applied to the final term gives: 

$$p \vee ((\neg q) \wedge r)$$ 

No more meaningful simplification can be done at this point. -->

### Option 2

<!-- Results will vary based on the equivalence chosen. Here is a sample solution using the first equivalence in Table 7, $p \rightarrow q \equiv \neg p \vee q$: 

| $p$ | $q$ | $p \rightarrow q$ | $\neg p$ | $\neg p \vee q$ | 
| -- | -- | -- | -- | -- | 
| T | T | T | F | T | 
| T | F | F | F | F | 
| F | T | T | T | T | 
| F | F | T | T | T | 

Since the columns for $p \rightarrow q$ and $\neg p \vee q$ have the same outcomes in all rows, they are logically equivalent statements.  -->

### Grading notes for Part C



---

## Part D 

### Option 1

<!-- 1. $\forall s \exists p R(s,p)$ 
2. $\exists p \forall s R(s,p)$ 
3. $\forall s (\exists p (H(p) \wedge R(s,p)) \rightarrow O(s))$. This one would translate literally into the following English: Looking at all servers, if there is a process such that the process is high priority and is running on the server, then the server is overloaded. 
4. **We can conclude that every server in the data center is overloaded**, if we assume that the statement in part (c) is true. That's because the final logical statement here is the hypothesis of the conditional statement that is in part (c). Nothing in the problem actually tells us that that statement in part c is true, however, But it's okay here to assume that that's the case.  -->

### Option 2

<!-- It is possible for both of these statements to be simultaneously true.  The first statement, when translated into English, would say: **for every server, if the server is overloaded, then it is running at least one high-priority process**. The second statement says that **there exists a server which only runs low priority processes**. (Literally: For every process, if the server is running that process, then it is not high priority.) A condition under which both of these statements would be true is **if one of the servers only ran low priority processes and was never overloaded**. If it only runs low priority processes, then it makes the second statement true. If it is never overloaded, then it makes the first statement true because the hypothesis of the conditional statement is false.  -->

### Grading notes for Part D

