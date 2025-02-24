# Solution guide for Learning Target Exam 2


## Learning Target 1

> (**CORE**) Given two integers $a$ and $b$, I can find the quotient and remainder when dividing $a$ by $b$, the greatest common divisor of $a$ and $b$ using the Euclidean Algorithm, and the value of `a % b`.

1. Use long division to find the quotient and remainder obtained when dividing $2893$ by $33$.

**Answer**: Quotient = 87, Remainder = 22. Note: Work is not shown on this one due to math formatting limitations. For questions about your work, please bring those to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 

2. Use the Euclidean Algorithm to find $\gcd(322, 16)$. 

**Solution**: 

$$\begin{eqnarray*}
322 &= 16(20) + 2 \\
16 &= 2(8) + 0
\end{eqnarray*}$$

Therefore $\gcd(322,16) = 2$ since $2$ is the last nonzero remainder. 

3. State the values of each of the following: 

- (a) $9876 \, \% \, 54$ 

- (b) $123098091235 \, \% \, 5$

- (c) $7890 \, \% \, 3$

**Answers**: $48$, $0$, $0$. (Note, no work needs to be shown here because it asks you to "state" the values.) 


## Learning Target 2

>I can convert a positive integer between bases 2, 8, 10, and 16; and I can represent a negative integer in binary using twos complement.

1. Convert the integer $3456$ from octal (base 8) to decimal (base 10). 

**Solution**: 
$$(3456)_{8} = 3 \times 8^3 + 4 \times 8^2 + 5 \times 8^1 + 6 \times 8^0 = 1838$$

2. Convert the integer `10110111` from binary (base 2) to decimal (base 10). 

$$(10110111)_2 = 1 \times 2^7 + 1 \times 2^5 + 1 \times 2^4 + 1 \times 2^2 + 1 \times 2^1 + 1 \times 2^0 = 128 + 32 + 16 + 4 + 2 + 1 = 183$$


3. Convert the integer 86457 from decimal (base 10) to hexadecimal (base 16). 

**Solution**: Using the base conversion algorithm: 

$$\begin{eqnarray*}
86457 &= 16(5403) + 9 \\
5403 &= 16(337) + 11 \\
337 &= 16(21) + 1 \\ 
21 &= 16(1) + 5 \\
1 &= 16(0) + 1 
\end{eqnarray*}$$

The algorithm stops since the quotient is zero and we read off the remainders in reverse order (changing to letters where appropriate): `151B9`. 

## Learning Target 3

> I can perform arithmetic operations on binary numbers. 

Note: Work is not shown below due to math formatting limitations. For questions about your work, please bring those to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 

1. Compute `110011 + 101011`.
2. Compute `110011 - 101011`. 
3. Compute `11001` $\times$ `101`. 
4. Compute `1000111` $\div$ `11`. 

**Answers:** `1011110`; `1000`; `1111101`; Quotient: `10111`, Remainder : `10`

### Notes

- A few submissions converted the binary to base 10, performed the basic arithmetic in base 10, then converted back to binary. This is not allowed; all work has to be done "natively" in base 2. 
- A few submissions of the division question gave the quotient but omitted the remainder. Both must be given. 


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: **If my final exam is on Monday, I will set my alarm.** 

1. State the hypothesis and conclusion of this implication. Make sure to state which is which. 
2. State the converse. 
3. State the contrapositive. 
4. State the negation. 

**Answers**: 

1. Hypothesis: My final exam is on Monday. Conclusion: I will set my alarm. 
2. If I set my alarm, then my final exam is on Monday. 
3. If I do not set my alarm, then my final exam is not on Monday. 
4. My final exam is on Monday, but I did not set my alarm. 

### Notes

**Many of the same common problems from Exam 1 are also common on Exam 2.  If you missed the same thing two exams in a row, you should get help immediately on this topic.**

- Many submissions stated the negation incorrectly, as some form of conditional statement such as *If my exam is not on Monday, then I will set my alarm*. **The negation of a conditional statement is NOT another conditional statement.** The negation of $P \rightarrow Q$ is $P \wedge (\neg Q)$ --- there should be no "if" or "then". 
- Many submissions stated the converse as *I will set my alarm if my final exam is on Monday*. But **this is the same sentence as the original, using the same hypothesis and the same conclusion, only written in a different order.** Remember, the physical ordering of the words is irrelevant -- the only thing that matters is which statement is the hypothesis and which is the conclusion. 
- Several submissions omitted both of the words "if" and "then" from the converse and contrapositive and used a comma, for example: *I set my alarm, my final exam is on Monday.* **Without at least one of "if" or "then", the statement is incorrect because there is no way to tell what the new hypothesis or new conclusion is.** Since there is no clear indication of cause and effect, this is not a conditional statement. In fact it is not even a grammatically correct sentence. That comma could be interpreted as "and", or "because", or "therefore"... it could mean many different things. 
- Some submissions included the word "if" in the hypothesis ("If my final exam is on Monday"). We have discussed in class that this is incorrect and explained why. 



## Learning Target 5

>I can write the truth table for a statement containing two or three variables.

Write the truth tables for the following statements. Remember to include *all* intermediate columns. 

1. $\neg(P \wedge Q)$

| $P$ | $Q$ | $P \wedge Q$ | $\neg(P \wedge Q)$ |
| --- | --- | ------------ | ------------------ |
| T   | T   | T            | F                  |
| T   | F   | F            | T                  |
| F   | T   | F            | T                  |
| F   | F   | F            | T                  |

2. $P \rightarrow (Q \vee (\neg P))$

| $P$ | $Q$ | $\neg P$ | $Q \vee (\neg P)$ | $P \rightarrow (Q \vee (\neg P))$ |
| --- | --- | -------- | ----------------- | --------------------------------- |
| T   | T   | F        | T                 | T                                 |
| T   | F   | F        | F                 | F                                 |
| F   | T   | T        | T                 | T                                 |
| F   | F   | T        | T                 | T                                 |

3. $P \wedge (Q \vee R)$ 

| $P$ | $Q$ | $R$ | $Q \vee R$ | $P \wedge (Q \vee R)$ |
| --- | --- | --- | ---------- | --------------------- |
| T   | T   | T   | T          | T                     |
| T   | F   | T   | T          | T                     |
| F   | T   | T   | T          | F                     |
| F   | F   | T   | T          | F                     |
| T   | T   | F   | T          | T                     |
| T   | F   | F   | F          | F                     |
| F   | T   | F   | T          | F                     |
| F   | F   | F   | F          | F                     |

### Notes

- Some submissions for the first truth table put `T` in the row where both $P$ and $Q$ are false. This is not how "and" works. 
- A few submissions had the wrong number of rows: 8 rows for the second part and 4 rows for the third part. 


## Learning Target 6

>Given a predicate, I can state the free variable(s); determine whether quantified forms are true or false; and state its negation.

1. For each quantified predicate below, state whether it is True or whether it is False. The domain of each predicate is the set $\mathbb{N} = \{0,1,2,3,\dots\}$.
    - (a) $\forall x (x \geq 0)$ **Answer:** True. 
    - (b) $\exists x (x^2 < 4)$ **Answer:** True. 
2. Below are some predicates that have quantifiers. For each, state which variables are free. If there are no free variables, say so. 
    - (a) $\forall x \exists z P(x,y,z)$ **Answer:** $y$
    - (b) $\exists x \exists y P(x,y)$ **Answer:** None
3. State the negation of the statement: *Some planets in our solar system have rings.* Phrase the result in plain English and do not just put the word "Not" or "It is not the case that" in front of the original statement. 

**Answer:** No planet in the solar system has rings. (Or: For every planet in the solar system, that planet does not have rings. Or: All planets in the solar system don't have rings. Or: There are no planets in the solar system that have rings. Other phrasings are also possible.)

### Notes

Here are some responses to the negation (third part), **none of which are correct**: 

- "Some planets in our solar system do not have rings"
- "All planets in our solar system have rings" 
- "Most planets in our solar system do not have rings"
- "Some planets outside our solar system have rings" 

These are all incorrect negations for the same reason: **Both they and the original statement are true at the same time.** For example it is true that some planets in our solar system have rings, and it is also true that most of them do not. **The fact that these statements are all true at the same time means that they are not negations of each other**. A statement and its negation must have exactly the opposite truth value in every situation. 


## Learning Target 7

>I can determine whether a sequence of statements is a valid rule of deduction and determine if two statements are logically equivalent. 

1. Determine whether these two statements are logically equivalent: $P \rightarrow Q$, and $(\neg P) \vee Q$. Show your work (which should involve a truth table) and clearly state whether the statements are logically equivalent or not. 

| $P$ | $Q$ | $\neg P$ | $P \rightarrow Q$ | $(\neg P) \vee Q$ |
| --- | --- | -------- | ----------------- | ----------------- |
| T   | T   | F        | T                 | T                 |
| T   | F   | F        | F                 | F                 |
| F   | T   | T        | T                 | T                 |
| F   | F   | T        | T                 | T                 |

The two statements **are logically equivalent**. 

2. Determine whether the following logical argument is valid or invalid: Premises are $p \rightarrow q$ and $\neg p$; conclusion is $\neg q$.   Show your work (which should involve a truth table) and clearly state whether the statements are logically equivalent or not. 

In the truth table below, the premises are marked with a checkmark and the conclusion is marked with a star: 

| $p$ | $q$ | $p \rightarrow q$ ✓ | $\neg p$ ✓ | $\neg q$ ☆ |              |
| --- | --- | ------------------- | ---------- | ---------- | ------------ |
| T   | T   | T                   | F          | F          |              |
| T   | F   | F                   | F          | T          |              |
| F   | T   | T                   | T          | F          | $\Leftarrow$ |
| F   | F   | T                   | T          | T          |              |

In the third row, the premises are true but the conclusion is not. Therefore **the argument is invalid**. 


## Learning Target 8

>Given a recurrence relation for a sequence or other structure, I can find several instances of the sequence or structure.

1. For each of the recurrence relations below, find the values of $a(1)$ through $a(5)$. Show all your work. 
    - (a) $a(1) = 3$, and if $n > 1$ then $a(n) = 2a(n-1) + 4$. 
    - (b) $a(1) = 5, a(2) = 6$, and if $n > 2$ then $a(n) = a(n-1) + a(n-2)$. 

2. Consider the following set of strings defined recursively: The string `A` is in the set. And for any string in the set, the string formed by appending `B` on to the left side of the string is also in the set. State six elements of this set. 

## Learning Target 9

>(**CORE**) Given a statement to prove by mathematical induction, I can set up the framework for its proof.

Consider this statement which we might want to prove using mathematical induction: For all positive integers $n$, the number $11^n - 6$ is a multiple of $5$. 

1. State the predicate involved in this proposition. 
2. State the value of the variable that corresponds to the base case. 
3. Prove that the base case holds. 
4. State the inductive hypothesis. 
5. State the inductive step (what you would need to prove to complete the argument). Note, you do not need to provide a completed proof here. 


**Answers:**

1. The predicate is $P(n):$ The number $11^n - 6$ is a multiple of $5$. 
2. $n = 1$ (because 1 is the smallest positive integer) 
3. When $n=1$ we have $11^1 - 6$ which is $11-6$ which equals $5$. This is a multiple of $5$. So the base case holds. 
4. Assume that for some positive integer $k$, $11^k - 6$ is a multiple of $5$. 
5. Prove that $11^{k+1} - 6$ is a multiple of $5$. 

### Notes

- Some submissions said the predicate involved was, "For all positive integers $n$, the number $11^n - 6$ is a multiple of $5$." That is, they included the quantifier "for all positive integers $n$". As we discussed in class this is incorrect because including the quantifier turns the predicate into a proposition -- it is no longer a predicate. 
- Some submissions stated the base case was when $n = 0$. That's incorrect because the proposition says all **positive** integers, and $0$ is not positive. 
- Some submissions did not include the words "Assume that..." in the inductive hypothesis. This is an error, somewhat minor but easy to avoid. The inductive hypothesis is not just "$11^k - 6$ is a multiple of $5$" -- it is the statement to the reader that we are going to assume that this statement is true. Be sure to tell the reader you are *assuming* something. 
- Some submissions used the wrong quantifier on the induction hypothesis, saying "Assume that $11^k - 6$ is a multiple of $5$ **for every** positive integer $k$." This is incorrect because if we assume this, we are assuming that the entire proposition we are trying to prove. That's wrong; we are only assuming that the predicate is true in one step, not all of them. 

**Special note:** I am making a change to the grading rubric for this item to categorize all of the above as "minor" errors and on this problem moving forward you are allowed *no more than one* of these errors. [Click here and scroll down to Learning Target 9](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md#standards-for-learning-targets). 
