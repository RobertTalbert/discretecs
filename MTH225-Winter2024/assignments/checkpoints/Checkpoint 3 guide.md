# Checkpoint 3 guide 

## C1

1. The screen breaks
2. I will get a new phone
3. If I get a new phone, the screen broke. (*or similar*)
4. If don't get a new phone, the screen wasn't broken. 
5. If the screen doesn't break, I won't get a new phone. 
6. The screen broke but I didn't get a new phone. 

### Common mistakes

-  **Getting the negation wrong:** The negation of the statement $P \rightarrow Q$ is $P \wedge (\neg Q)$. We have discussed this in videos and class meetings, and seen it from looking at truth tables, so this is now a well-established concept. If you correctly identify the hypothesis and conclusion in steps 1 and 2, then just use the formula to get the correct negation (shown above). A number of students mis-wrote the negation as $(\neg P) \wedge Q$ to get "My screen isn't broken but I got a new phone". Other incorrect formulations were present. **Practice: Memorize the formula for the negation -- then ask ChatGPT for practice exercises.** 
- **Not actually swapping the hypothesis and conclusion in the converse but just writing them in different locations:** For example, *"If the screen breaks, then I will get a new phone."* This moves the statement about the screen breaking from the second half of the sentence to the first half; but it does not change the fact that it's still the hypothesis. This is the same proposition, from a logical standpoint, as the original. The converse of $P \rightarrow Q$ is $Q \rightarrow P$ and this has to involve reversing the "cause" and the "effect", not just rearranging where phrases happen. **Practice: Memorize the formula for the converse -- then ask ChatGPT for practice exercises.**

## C2

1. The predicate is the statement, $1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$. 
2. $n = 1$
3. If $n=1$, the left side is just the number 1 (a one-term "sum"). The right side is $\frac{1(2)}{2}$ which equals $1$. The left and right sides are equal so the base case holds.
4. Assume that for some positive integer $k$, $1 + 2 + 3 + \cdots + k = \frac{k(k+1)}{2}$.
5. Prove that $1 + 2 + 3 + \cdots + (k+1) = \frac{(k+1)(k+2)}{2}$

## C3

1.(a) True

   (b) True 

   (c) True 

   (d) True 

   (e) False 

2. (a) Incorrect syntax 

   (b) $\lbrace 2,4,8\rbrace$ 

   (c) $\lbrace 1,3,5,7,9 \rbrace$ 

## C4

1. $\lbrace 2 \rbrace$ 
2. $\lbrace 2,3,4,5,6 \rbrace$ 
3. $\lbrace 4,5 \rbrace$ 
4. $\lbrace 2,3,4,6 \rbrace$
5. $9$ 
6. $\lbrace \emptyset, \lbrace 2 \rbrace, \lbrace 4 \rbrace, \lbrace 6 \rbrace, \lbrace 2,4 \rbrace, \lbrace 4,6 \rbrace,\lbrace 2,6 \rbrace, \lbrace 2,4,6 \rbrace \rbrace$

## C5

1. $2^{19}$ because the test consists of 19 items, each of which has two possible choices. 
2. According to the Principle of Inclusion and Exclusion, the number of students who major in either math or CS, is equal to the number of students majoring in math plus the number of students majoring in CS minus the number of students majoring in both subjects. It is the final item that we want; so let's find the other three quantities in this statement. The number of students majoring in math is 14; the number majoring in CS is also 14. The number of students majoring in one or both of those subjects, is the complement of those who are not majoring in either one -- so that's $24 - 5 = 19$. Therefore the number of students majoring in both is $14 + 14 - 19 = 9$. 

## C6

1. (a) $6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720$ 

   (b) $\displaystyle{\binom{20}{18} = \frac{20!}{18! \cdot 2!} = \frac{20 \cdot 19}{2} = 190}$ 

2. We are selecting 4 items (toppings) from a list of 16. The order of the selection is irrelevant since we end up with the same pizza no matter what order we choose the toppings in. So the count is given by the binomial coefficient, $\displaystyle{\binom{16}{4} = 1820}$. 

---

## S1

1. $(500)_{10}$ 
2. $(E1)_{16}$
3. $111000$
4. `1101 1100`

## S2

1. `01010010`
2. `100000`
3. `010101011`
4. `011100` Remainder : `1`

## S3

1.
| $p$ | $q$ | $r$ | $q \vee r$ | $p \wedge (q \vee r)$ |
| ---- | ---- | ---- | ---- | ---- |
| T | T | T | T | T |
| T | T | F | T | T |
| T | F | T | T | T |
| T | F | F | F | F |
| F | T | T | T | F |
| F | T | F | T | F |
| F | F | T | T | F |
| F | F | F | F | F |

2. (Putting both statements into a combo truth table)

| $p$ | $q$ | $p \rightarrow q$ | $\neg(p \rightarrow q)$ | $\neg p$ | $\neg q$ | $(\neg p) \rightarrow (\neg q)$ |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| T | T | T | F | F | F | T |
| T | F | F | T | F | T | T |
| F | T | T | F | T | F | F |
| F | F | T | F | T | T | T |

So, **no** the two statements are not logically equivalent. 


## S4

1. (a) True

   (b) True 

   (c) False

   (d) False 

2. There are at least two problems on this quiz that don't have the same answer. (*Other right answers are possible*)

### Common mistakes

- **Using a universal statement as the negation in part 2:** This would read something like *"Every problem on this quiz has a different answer"*. This is not the negation of the original because it's possible for this statement and the original to both be false -- imagine a quiz where the first two answers were the same but the rest of the answers are different. The negation of a universal statement is an existential statement -- a statement that a [counterexample](https://publish.obsidian.md/mth225/Logic/Counterexample) exists. 
- **Giving "TRUE" as the answer to 1(d)**: The statement in 1(d), in English, is saying that there exists an integer, $x$, for which $x+2$ is *not* an integer. But this is a false statement because adding 2 to an integer always creates another integer (not a fraction, etc.). 