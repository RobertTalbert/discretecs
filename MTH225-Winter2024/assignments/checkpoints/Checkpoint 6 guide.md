# Checkpoint 6 Guide

## C1

Initial statement: "I will say hello if I see you later."

1. I will see you later
2. I will say hello
3. If I say hello, then I saw you later. 
4. If I don't say hello, then I didn't see you later. 
5. If I don't see you later, I won't say hello. 
6. I saw you later but I didn't say hello. 

### Common mistakes

These are the same common mistakes that have cropped up before; please see the guides for [Checkpoint 3](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%203%20guide.md) and [Checkpoint 2](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%202%20solutions.md) for details: 

- **Using an incorrect form for the negation**, and 
- **Not actually switching the hypothesis and conclusion in the converse** but just movintg them to different parts of the sentence. 

## C2 

>For every integer $n \geq 1$, $1 + 2+3+ \cdots + n = \dfrac{n(n+1)}{2}$.  

1. The predicate is " $1 + 2+3+ \cdots + n = \dfrac{n(n+1)}{2}$ ". 
2. The base case is $n = 1$
3. Suppose $n=1$. Then the left side of the predicate is the one-term "sum" consisting of just the number 1. The right side of the predicate is the fraction $\dfrac{1(1+1)}{2}$. This fraction equals $\frac{1 \cdot 2}{2}$ which equals $1$. The sides are equal so the base case holds. 
4. Assume that $1 + 2+3+ \cdots + k = \dfrac{k(k+1)}{2}$ for some positive integer $k$. 
5. Prove that $1 + 2+3+ \cdots + (k+1)= \dfrac{(k+1)(k+2)}{2}$. 

### Common mistakes

- **Not using the phrase "Assume that..." in the inductive hypothesis:** That is, writing that the inductive hypothesis only says " $1 + 2+3+ \cdots + k = \dfrac{k(k+1)}{2}$ for some positive integer $k$ ". It's very important to communicate that we are *assuming* that this is the case; in an actual proof, this would need to be made clear. *Omission of this phrase is being counted from now on as a "simple" error as long as the rest of the work is correct.*
- **In the inductive hypothesis and inductive step, having only $k$ and $k+1$ on the left sides:** For example, saying that we will assume that $k = \dfrac{k(k+1)}{2}$. It's supposed to be *the sum of 1 through $k$* , not just $k$ itself. As discussed in class this is just the predicate, identified in step 1, with $k$ instead of $n$. 


## C3

1. (a) False 

   (b) False

   (c) True

   (d) True

   (e) False 

2. (a) $\lbrace 5,6,7 \rbrace$

   (b) Two possibilities: Either INCORRECT SYNTAX because it's written predicate-first; or it's the set {True, False} when interpreting $n^2 < 100$ as a Boolean-valued function. 

   (c) $\lbrace 2,4,6,8,10 \rbrace$

### Common mistakes

- **Answering "True" for 1(a)**: The set $\lbrace 1,2,3 \rbrace$ is not an *element* of the set $\lbrace 0,1,2,3,4 \rbrace$, it is a *subset*. The elements of the set $\lbrace 0,1,2,3,4 \rbrace$ are the numbers 0, 1, 2, 3, and 4. 
- **Stating that 2(b) is the set $\lbrace 64, 81 \rbrace$ or $\lbrace 8, 9 \rbrace$:** Both are incorrect because of the reasons explained above. The second of these, $\lbrace 8, 9 \rbrace$, would be a correct roster notation for the set $\lbrace n \in \lbrace 8,9,10,11\rbrace : n^2 < 100  \rbrace$ -- that is, if the original set were written in correct set-builder notation. 
- **Stating that the set in 2(c) is incorrect syntax:** It's not. There are two forms of correct syntax: a function, followed by a set to map it over; and a set, followed by a predicate to filter it with. 2(c) is the second kind. 


## C4

1. $\emptyset$
2. $\lbrace 2,3,4,5 \rbrace$
3. $\lbrace 5 \rbrace$
4. $\lbrace 3,4,6,7,8 \rbrace$
5. $\lbrace 1,2,3,4,5,6,7,8,9,10 \rbrace$
6. $8$ 

### Common mistakes

- **Putting set braces around the empty set in item 1:** That is, giving the answer as $\lbrace \emptyset \rbrace$ instead of just $\emptyset$ which is the correct response. The sets $\lbrace \emptyset \rbrace$ and $\emptyset$ are not equal! One is empty and the other isn't. This is treated as a "simple" error in terms of the success criteria. 
- **Mixing up intersection and union:** For example stating that $A \cap C$ in item 1 is $\lbrace 2,3,4,6,7,8 \rbrace$. 
- **Giving the full power set in item 8 instead of its cardinality:** That's what the " $| \ |$ " bars mean -- cardinality. 

## C5

1. Since the choice of blouse and the choice of skirt are independent of each other, the Multiplicative Principle applies, and the count is $4 \cdot 3 = 12$. 
2. The Principle of Inclusion and Exclusion says that the count is the number of sneakers, plus the number of white shoes, minus the number of white sneakers: $3 + 5 - 1 = 7$. 

### Common mistakes

- **Not providing work that explains the answers:** This skill is one of the few where explanations and/or intermediate work, not just an answer, is required for a successful attempt. (See the success criteria for this skill.) So either giving an answer, right or otherwise, without supporting work; or giving work that doesn't clearly follow from the problem statement, will result in an unsuccessful attempt. 

## C6

1. (a) $7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5040$

   (b) $\displaystyle{\binom{99}{97} = \frac{99!}{97! \cdot 2!} = \frac{99 \cdot 98}{2} = 4851}$


2. [By definition](https://publish.obsidian.md/mth225/Combinatorics/Binomial+coefficient), the count of these is $\displaystyle{\binom{10}{4} = 210}$. 

--- 

## Supplemental skills

## S1

1. $370$
2. $(338)_{16}$
3. $(10100010)_2$
4. `1100 1001`

## S2

1. `01011100` 
2. `01110`
3. `010011111`
4. `011010`, Remainder : 1

## S3

| $p$ | $q$ | $r$ | $\neg r$ | $q \vee (\neg r)$ | $p \rightarrow (q \vee (\neg r))$ |
| --- | --- | --- | -------- | ----------------- | --------------------------------- |
| T   | T   | T   | F        | T                 | T                                 |
| T   | T   | F   | T        | T                 | T                                 |
| T   | F   | T   | F        | F                 | F                                 |
| T   | F   | F   | T        | R                 | T                                 |
| F   | T   | T   | F        | T                 | T                                 |
| F   | T   | F   | T        | T                 | T                                 |
| F   | F   | T   | F        | F                 | T                                 |
| F   | F   | F   | T        | T                 | T                                 |


| $p$ | $q$ | $p \rightarrow q$ | $\neg(p \rightarrow q)$ | $\neg p$ | $(\neg p) \vee q$ |
| --- | --- | ----------------- | ----------------------- | -------- | ----------------- |
| T   | T   | T                 | F                       | F        | T                 |
| T   | F   | F                 | T                       | F        | F                 |
| F   | T   | T                 | F                       | T        | T                 |
| F   | F   | T                 | F                       | T        | T                 |

The two propositions **are not** logically equivalent. 

## S4

1. (a) False (because $12^2 = 144$ which is bigger than 100)

   (b) True (because $9^2 = 81$ which is odd)

   (c) False (because $12$ is a counterexample)

   (d) True (because $2$ is an example -- $2^2 = 4$ which is not odd)

2. There are at least two questions on this quiz that do not have the same answer. (*Other correct responses, differently phrased but equivalent to this one, are possible*)

## S5

Given: $a_0 = 1$, $a_1 = 2$, and $a_n = 2a_{n-1} - 3a_{n-2}$ for $n \geq 2$. 

- $a_2 = 2a_1 - 3a_0 = 2(2) - 3(1) = 1$
- $a_3 = 2a_2 - 3a_1 = 2(1) - 3(2) = -4$
- $a_4 = 2a_3 - 3a_2 = 2(-4) - 3(1) = -11$
- $a_5 = 2a_4 - 3a_3 = 2(-11) - 3(-4) = -22 + 12 = -10$
- $a_6 = 2a_5 - 3a_4 = 2(-10) - 3(-11) = -20 + 33 = 13$

## S6

1. $R(1) = 2, R(2) = 6, R(3) = 12$. 
2. In the visual pattern, first note that in step $n$ the figure is a grid of blocks with $n$ rows and $n+1$ columns. Each step takes the figure in the previous step and adds the following to it: 
   - A new top row of blocks, having $n$ blocks in it 
   - A new right column, having $n-1$ blocks in it
   - One additional block in the top right corner. 
To count the number of blocks in step $n$, $R(n-1)$ gives the number of blocks from the previous step. Then add $n$, $n-1$, and $1$ to make the new figure. The resulting recurrence relation is $R(n) = R(n-1) + n + n-1 + 1$ or $R(n) = R(n-1) + 2n$. 

## S7

Note: Explanations are not necessary for this problem, but some explanations are provided in italics to help you understand the correct answers. 

1. Not a function (*because 3 has no output*) 
2. Not a function (*because 4 has no output*)
3. **Function**. Domain = $\lbrace 1,9,7,3,6 \rbrace$. Codomain = $\lbrace 4,7,3,8 \rbrace$. Range = $\lbrace 4,7,3,8 \rbrace$. 
4. Not a function (*because 8 is mapped to two outputs*)
5. Not a function (*because 5 is mapped to two outputs*)
6. **Function.** Domain = $\lbrace 2,1,0 \rbrace$. Codomain = $\lbrace 3,8,9,4 \rbrace$. Range = $\lbrace 8,9,4 \rbrace$. 