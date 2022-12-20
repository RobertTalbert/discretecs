---
tags: mth225
---

# Key for Learning Target quiz 4, 2021-10-22

## CA.1, CA.2, and SF.5

You can check these using calculators: 

- [Base conversion calculator](https://www.rapidtables.com/convert/number/base-converter.html) 
- [Binary arithmetic calculator](https://www.calculator.net/binary-calculator.html) 
- [Wolfram|Alpha](https://wolframalpha.com) for the rest

## L.1

| Statement: | $A \rightarrow B$ | If a student is enrolled in MTH 203, the student passed MTH 201. | 
| --- | --- | --- | 
| Hypothesis | $A$ | A student is enrolled in MTH 203 | 
| Conclusion | $B$ | The student passed MTH 201 | 
| Negation   | $A \wedge (\neg B)$ | A student is enrolled in MTH 203 but did not pass MTH 201.  | 
| Converse   | $B \rightarrow A$  | If a student passed MTH 201, the student is enrolled in MTH 203. | 
| Contrapositive | $(\neg B) \rightarrow (\neg A)$ | If a student did not pass MTH 201, the student is not enrolled in MTH 203.  | 

Note, "but" and "and" in the negation are interchangeable. 

## L.2

1.
| $P$ | $Q$ | $P \rightarrow Q$ | $\neg (P \rightarrow Q)$ |
   | --- | --- | ---------- | ----------------- |
   |  T  |  T  | T | F | 
   |  T  |  F  | F | T |
   |  F  |  T  | T | F | 
   |  F  |  F  | T | F |
   


| $P$ | $Q$ | $\neg Q$ | $P \wedge (\neg Q)$ | 
| -------- | -------- | -------- | ------- | 
| T     | T     | F     | F |
| T     | F     | T     | T |
| F     | T     | F     | F |
| F     | F     | T     | F |

   
So the two statements are logically equivalent. Very useful for Learning Target L.1 by the way. 

2. 
| $P$ | $Q$ | $R$ | $Q \vee R$ | $P \wedge (Q \vee R)$ |
|:---:|:---:|:---:|:----------:|:---------------------:|
|  T  |  T  |  T  |     T      |           T           |
|  T  |  F  |  T  |     T      |           T           |
|  F  |  T  |  T  |     T      |           F           |
|  F  |  F  |  T  |     T      |           F           |
|  T  |  T  |  F  |     T      |           T           |
|  T  |  F  |  F  |     F      |           F           |
|  F  |  T  |  F  |     T      |           F           |
|  F  |  F  |  F  |     T      |           F           |


## L.3

1. True, False, False, False 
2. (a) False because not all integers are even, for example $n = 3$
   (b) True, for example $P(2)$ is true
   (c) True, because for example $Q(8)$ is true since $8/2$ is an integer. 
3. There is a numbered street in Allendale that has a number not divisible by 4. (Other formulations are possible. And, it's an open question whether the original statement is true! Drive around town and check it out.) 

## SF.1

1. (a) $\{0, 5, 10, 15, 20,  \dots\}$
   (b) $\{0,1,2,3,4\}$  (Must be a finite set with no repetitions!)
   (c) $\{1\}$
   
2. Two possible correct answers: 
   - $\{2x+1 \, : \, x \in \mathbb{N}\}$ 
   - $\{x \in \mathbb{N} : x \ \text{is odd} \}$
There are lots of others. 

3. (a) True ([remember this?](https://campuswire.com/c/GB1A69E25/feed/76))
   (b) True
   (c) True 
   (d) False
   (e) True
   (f) True 

## SF.2

1. $\{1\}$
2. $\{1,3,5,7,9\}$
3. $\{5\}$
4. $\{0,3,5,6,7,9,10\}$
5. $\{2,3,4,5,6,7,8,9\}$
6. $\{3,5,7,9\}$
7. $16$


## SF.3

1. This is a function with domain = $\{1,2,3,4\}$, codomain = $\{x,y,z,t\}$, and range $\{x,y,z,t\}$.
2. This is a function with domain = $\{1,2,3,4\}$, codomain = $\{x,y,z,t\}$, and range $\{x,z,t\}$. 
3. This is not a function because 4 does not map to anything. 


## SF.4

1. This function is bijective. 
2. This function is not injective because 1 and 2 both map to $z$. It is also not surjective because nothing maps to $t$. Therefore it's also not bijective.  
3. This function is injective, but it isn't surjective because no negative integers are ever output. (Also there are a lot of positive integers that aren't output, like 3). Therefore it's not bijective. 

## C.1 

1. A three-digit base-8 integer has three digits, so there's three choices for the digit, with 8 options ($0-7$) for each digit. Therefore the number of 3-digit integers possible is $8 \times 8 \times 8 = 512$. 
2. There are $2^4 = 16$ 4-bit strings possible. Of those, $2^3$ start with a 1, because the starting digit is locked in and there are three remaining choices with 2 options each. The same reasoning says there are $2^3$ that end in a 1. And, there are $2^2$ that *both* start *and* end in a 1, since locking in the starting and ending digits allows free choice of the middle two bits. Therefore by the Principle of Inclusion/Exclusion, the total number that either start or end in a 1 is $2^3 + 2^3 - 2^2 = 12$. 


## C.2 

:::info
Note on C.2--C.4: As mentioned in class, on the "word problem" parts of these, you don't have to actually compute the numerical values of the answer, just set it up using the binomial coefficient or permutation and leave it. I've computed everything below just so you can see the results.
:::

$\binom{10}{6} = \frac{10!}{4! \cdot 6!} = 210$
$\binom{30}{29} = \frac{30!}{1! \cdot 29!} = 30$
$\binom{100}{0} = 1$ because there is only one zero-element subset of $\{1, 2, \dots, 100\}$. 

The number of ways to select $5$ books from a shelf of $20$ identical books is $\binom{20}{5} = \frac{20!}{5! \cdot 15!} = 15504$. 


## C.3

$P(22,8) = \frac{22!}{14!} = 22 \cdot 21 \cdots 16 \cdot 15 = 12893126400$

The number of ways to give away the five shirts is $P(24,5)$. If you start with the blue shirt there are 24 ways to give that one away, then 23 ways to give away the red one, then 22 ways to give away the green one, then 21 ways to give away the yellow one, then 20 ways to give away the purple one. So that's $P(24,5) = \frac{24!}{19!} = 24 \cdot 23 \cdot 22 \cdot 21 \cdot 20 = 5100480$. 

## C.4 

1. Such a distribution would be represented by a stars-and-bars diagram with 5 stars (the shirts) and 23 bars (the number of switches between the students). That's 28 objects total, with 23 of them bars. That corresponds to a bit string with 28 bits having weight 23. The number of those is $\binom{28}{23} = \frac{28!}{5! \cdot 23!} = 98280.$ 
2. This is the same problem as distributing 10 objects to three bins. A stars-and-bars diagram would have 10 stars and 2 bars, so the total number of natural number solutions is $\binom{12}{2} = \frac{12!}{2! \cdot 10!} = 66$. 