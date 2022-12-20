---
tags: mth225
---

# Key for Learning Target quiz 5, 2021-10-29

## CA.1, CA.2, and SF.5

You can check these using calculators: 

- [Base conversion calculator](https://www.rapidtables.com/convert/number/base-converter.html) 
- [Binary arithmetic calculator](https://www.calculator.net/binary-calculator.html) 
- [Wolfram|Alpha](https://wolframalpha.com) for the rest

## L.1

| Statement: | $A \rightarrow B$ | If I wait until 9pm on Sunday to start on a Weekly Challenge, then I will be stressed out. | 
| --- | --- | --- | 
| Hypothesis | $A$ | I wait until 9pm on Sunday to start on a Weekly Challenge | 
| Conclusion | $B$ | I will be stressed out | 
| Negation   | $A \wedge (\neg B)$ | I waited until 9pm on Sunday to start a Weekly Challenge but am not stressed out  | 
| Converse   | $B \rightarrow A$  | If I am stressed out, then I waited until 9pm on a Sunday to start a Weekly Challenge. | 
| Contrapositive | $(\neg B) \rightarrow (\neg A)$ | If I am not stressed out, then I did not wait until 9pm on Sunday to start a Weekly Challenge.  | 

Note, "but" and "and" in the negation are interchangeable. 

## L.2

1.
| $P$ | $Q$ | $P \rightarrow Q$ | $(\neg P)$ | $(\neg P) \vee Q$ |
   | --- | --- | ---------- | -----------------| ---- |
   |  T  |  T  | T | F | T |
   |  T  |  F  | F | F | F | 
   |  F  |  T  | T | T | T |
   |  F  |  F  | T | T | T |
   


   
So the two statements are logically equivalent. 

2. 
| $P$ | $Q$ | $R$ | $Q \wedge R$ | $P \vee (Q \wedge R)$ |
|:---:|:---:|:---:|:----------:|:---------------------:|
|  T  |  T  |  T  |     T      |           T           |
|  T  |  F  |  T  |     F      |           T           |
|  F  |  T  |  T  |     T      |           T           |
|  F  |  F  |  T  |     F      |           F           |
|  T  |  T  |  F  |     F      |           T           |
|  T  |  F  |  F  |     F      |           T           |
|  F  |  T  |  F  |     F      |           F           |
|  F  |  F  |  F  |     F      |           F           |


## L.3

1. True, False, False, False 
2. (a) False because not all integers are multiples of 5, for example $n = 3$
   (b) True, for example $P(10)$ is true
   (c) True, because for example $Q(2)$ is true. (In fact this is the one and only value of $x$ in the positive integers that makes this predicate true.)
3. All smartphones cost $1000 or less. ("less than $1000" is also OK) 

## SF.1

1. (a) $\{5, 6, 7, 8, 9, 10,  \dots\}$
   (b) $\emptyset$ because the only number that makes $x+5 = 0$ is $x = -5$ and that's not a natural number. 
   (c) $\{2,4,6,8,10\}$
   
2. Two possible correct answers: 
   - $\{10^{x+1} \, : \, x \in \mathbb{N}\}$ 
   - $\{x \in \mathbb{N} : x \ \text{is a power of 10} \}$
There are lots of others. 

3. (a) True
   (b) True (the empty set is a subset of every set)
   (c) False (for example $1.1 \in \mathbb{R}$ but $1.1 \not \in \mathbb{N}$) 
   (d) True 
   (e) False 
   (f) False ($1$ is in the first set but not in the second) 

## SF.2

1. $\{5,9\}$
2. $\{1,2,3,4,5,7,8,9\}$
3. $\{1,3,7\}$
4. $\{0,3,5,6,7,9,10\}$
5. $\{2,3,4,5,7,8,9\}$
6. $10$ 
7. $\{3,5,7,9\}$
8. $\{\emptyset, \{5\}, \{9\}, \{5,9\}\}$


## SF.3

1. This is a not a function because $2$ maps to two things. 
2. This is a function with domain $\{1,2,3,4\}$, codomain = $\{x,y,z,t\}$, and range $\{x\}$. 
3. This is a function domain $\{1,2,3,4\}$, codomain = $\{x,y,z,t\}$, and range $\{t,x,z\}$.


## SF.4

1. This function is bijective. 
2. This function is injective, but not surjective because even numbers are never output. Therefore not bijective.   
3. This function is bijective. 

## C.1 

1. This is a problem about selecting one thing from a bunch of disjoint bins. So the Additive Principle states that the number of choices is the sum of the bin sizes: $5 + 2 + 4 = 11$. 
2. With the final three bits decided, the first five bits have a free choice with two options each so the number of bit strings is $2^5 = 32$. 

## C.2 

$\binom{12}{3} = \frac{12!}{3! \cdot 8!} = 220$
$\binom{70}{69} = 70$ either through the formula, or realizing this is the number of 69-element subsets of a 70-element set. Choosing 69 elements means you're leaving out exactly 1, and there's 70 ways to omit one element. 
$\binom{70}{70} = 1$ because there is only one 70-element subset of $\{1, 2, \dots, 70\}$ namely the set itself. Or use the formula. 

The number of ways to select $6$ songs from a list of 22 and not care about the order is $\binom{22}{6} = 74613$. 


## C.3

1. The number of ways to choose an *ordered* list of 6 songs from a list of 22 is $P(22,6) = \frac{22!}{16!} = 22 \times 21 \times 20 \times 19 \times 18 \times 17  = 53721360$. 
2. The number of ways to give out first and second place to a group of 50 people is $P(50,2) = \frac{50!}{48!} = 50 \times 49 = 2450$. 


## C.4 

1. Such a distribution would be represented by a stars-and-bars diagram with 50 stars (the candy bars) and 9 bars (the number of switches between the kids). That's 59 objects total, with 9 of them bars. That corresponds to a bit string with 59 bits having weight 9. The number of those is $\binom{59}{9} = 12565671261$.  
2. This is the same problem, but to ensure each kid gets a candy bar, start off by giving one to each kid. You now have 40 candy bars to give out however you want. This is a stars-and-bars problems with 40 stars and 9 bars, so the number of distributions is $\binom{49}{9} = 2054455634$. 

Upon further reflection I could have chosen the "stars" to be something other than candy **bars**. :joy: 