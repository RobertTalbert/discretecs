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

(a) Find all values in $0 \leq x \leq 9$ that satisfy $4x \equiv 8 \pmod{10}$. 


| $x$ | $4x$ | $4x \pmod{10}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $4$  | $4$  | 
| $2$ | $8$  | $8$ $\star$ | 
| $3$ | $12$  | $2$  | 
| $4$ | $16$  | $6$  | 
| $5$ | $20$  | $0$  | 
| $6$ | $24$  | $4$   | 
| $7$ | $28$  | $8$ $\star$  | 
| $8$ | $32$  | $2$  | 
| $9$ | $36$  | $6$  | 

The solutions are $x = 2$ and $x = 7$. 

(b) Repeat for $3x \equiv 8 \pmod{10}$. 

| $x$ | $3x$ | $3x \pmod{10}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $3$  | $3$  | 
| $2$ | $6$  | $6$  | 
| $3$ | $9$  | $9$  | 
| $4$ | $12$  | $2$  | 
| $5$ | $15$  | $5$  | 
| $6$ | $18$  | $8$ $\star$  | 
| $7$ | $21$  | $1$   | 
| $8$ | $24$  | $4$  | 
| $9$ | $27$  | $7$  | 

This time there's only one solution, $x = 6$. 

### Option 2

(a) Find a modular inverse for $5$ modulo $11$. 



| $x$ | $5x$ | $5x \pmod{11}$ | 
| --- | --- | ---- | 
| $0$ | $0$  | $0$  | 
| $1$ | $5$  | $5$  | 
| $2$ | $10$  | $10$  | 
| $3$ | $15$  | $4$  | 
| $4$ | $20$  | $9$  | 
| $5$ | $25$  | $3$  | 
| $6$ | $30$  | $8$  | 
| $7$ | $35$  | $2$  | 
| $8$ | $40$  | $7$  | 
| $9$ | $45$  | $1$  $\star$  | 
| $10$ | $50$  | $6$  | 

The modular inverse of $5$ mod $11$ is $9$. 

(b) To solve $5x \equiv 7 \pmod{11}$, multiply both sides by $9$ and reduce: 

$$\begin{eqnarray*}
9 \cdot 5x &\equiv 9 \cdot 7 \pmod{11} \\
(9 \cdot 5)x &\equiv 63 \pmod{11} \\
x &\equiv 8 \pmod{11}
\end{eqnarray*}$$

So the solution is $x=8$. 

---

## Part C

### Option 1

Translated into symbols, the statement is: 

$$\neg \left( (p \wedge q) \vee (r \wedge q) \right)$$

Applying DeMorgan's Law to the entire statement gives: 

$$\neg (p \wedge q) \wedge \neg (r \wedge q)$$

Now apply DeMorgan's Law twice: 

$$(\neg p \vee \neg q) \wedge (\neg r \vee \neg q)$$

Now "factor out" a $\neg q$ using the Distributive Law: 

$$\neg q \vee (\neg p \wedge \neg r)$$

Translated back into words, the connection is allowed if the user is authenticated, or if both the IP is unblocked and the port is unrestricted. 

### Option 2

The two statements in symbolic form are: $(p \vee q) \rightarrow r$ and $(\neg p \wedge \neg q) \vee r$. A truth table for both statements is below, with all the necessary intermediate columns: 

| p | q | r | ¬p | ¬q | p ∨ q | **(p ∨ q) → r** | ¬p ∧ ¬q | **(¬p ∧ ¬q) ∨ r** |
|---|---|---|----|----|-------|-------------|---------|---------------|
| T | T | T | F  | F  |   T   |      T      |    F    |       T       |
| T | T | F | F  | F  |   T   |      F      |    F    |       F       |
| T | F | T | F  | T  |   T   |      T      |    F    |       T       |
| T | F | F | F  | T  |   T   |      F      |    F    |       F       |
| F | T | T | T  | F  |   T   |      T      |    F    |       T       |
| F | T | F | T  | F  |   T   |      F      |    F    |       F       |
| F | F | T | T  | T  |   F   |      T      |    T    |       T       |
| F | F | F | T  | T  |   F   |      T      |    T    |       T       |

As we can see from the seventh and ninth columns, the two statements have all the same logical values and are therefore logically equivalent. 

### Grading notes for Part C

- A number of submissions for option 2 did not show all the intermediate columns for the truth table. This was an explicit instruction and anytime you make a truth table, you must show all intermediate columns. 
- Other submissions for option 2 had the correct truth table with all the intermediate columns, but did not answer the main question of the problem, which is whether the two statements are logically equivalent. Remember to read all the directions carefully and make sure you're giving the information that you're being asked for. 

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

