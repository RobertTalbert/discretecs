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
- **Stating that 2(b) is the set $\lbrace 64, 81 \rbrace$ or $\lbrace 8, 9 \rbrace$:** Both are incorrect because of the reasons explained above. The second of these, $\lbrace 8, 9 \rbrace$, would be a correct roster notation for the set $n \in \{8,9,10,11\} : \lbrace n^2 < 100  \rbrace$ -- that is, if the original set were written in correct set-builder notation. 


## C4

1. $\emptyset$
2. $\lbrace 2,3,4,5 \rbrace$
3. $\lbrace 5 \rbrace$
4. $\lbrace 3,4,6,7,8 \rbrace$
5. $\lbrace 1,2,3,4,5,6,7,8,9,10 \rbrace$
6. $8$ 

## C5

1. Since the choice of blouse and the choice of skirt are independent of each other, the Multiplicative Principle applies, and the count is $4 \cdot 3 = 12$. 
2. The Principle of Inclusion and Exclusion says that the count is the number of sneakers, plus the number of white shoes, minus the number of white sneakers: $3 + 5 - 1 = 7$. 

## C6

1. (a) $7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5040$

   (b) $\displaystyle{\binom{99}{97} = \frac{99!}{97! \cdot 2!} = \frac{99 \cdot 98}{2} = 4851}$


2. By definition the count of these is $\displaystyle{\binom{10}{4} = 210}$. 

--- 

*Supplemental Skills coming later*