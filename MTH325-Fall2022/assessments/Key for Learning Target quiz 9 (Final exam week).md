---
tags: mth225
---

# Key for Learning Target quiz 9 (Final exam week)

## CA.1 

1. 11001 and 19
2. 2538
3. 115
4. 11001001

## CA.2

## L.1

| Statement: | If it's raining, then I'm getting wet. | 
| ---- | ----- | 
| Hypothesis: | It's raining | 
| Conclusion: | I'm getting wet |
| Negation: | It's raining but I'm not getting wet. | 
| Converse: | If I'm getting wet, it's raining. | 
| Contrapositive: | If am not getting wet, then it's not raining. | 


## L.2

1.
| $P$ | $Q$ | $P \vee Q$ | $\neg (P \vee Q)$ | $\neg P$ | $\neg Q$ | $(\neg P) \wedge (\neg Q)$
   | --- | --- | :----------: | :---------------: | :----: | :--: | :--: | 
   |  T  |  T  | T | F | F | F | F | 
   |  T  |  F  | T  | F | F | T | F |
   |  F  |  T  | T | F |  T | F| F | 
   |  F  |  F  | F | T | T | T  | T | 


   
So the two statements **are** logically equivalent. 

2. 
| $P$ | $Q$ | $R$ | $P \rightarrow Q$ | $Q \rightarrow R$ | $(P \rightarrow Q) \wedge (Q \rightarrow R)$ | 
|:---:|:---:|:---:|:----------:|:---------------------:| :--: | 
|  T  |  T  |  T  |     T      |           T           | T
|  T  |  F  |  T  |     F     |           T           | F
|  F  |  T  |  T  |     T      |           T           | T
|  F  |  F  |  T  |     T      |           T           | T
|  T  |  T  |  F  |     T      |           F           | F
|  T  |  F  |  F  |     F      |           T           |F
|  F  |  T  |  F  |     T      |           F           |F
|  F  |  F  |  F  |     T      |           T           |T

## L.3

1. True, False, True, True
2. (a) False, for example $x = 1$
   (b) True, for example $x = 10$
   (c) True, adding 2 to an integer always just produces another integer 
3. Three possible correct answers (there are others): 
   - Some problems for this Learning Target have different answers.
   - Some problems for this Learning Target do not have the same answer. 
   - There exist at least two problems for this Learning Target that do not have the same answer. 

## SF.1

1. (a) $\{1, 2, 3\}$ 
   (b) $\{1, 8, 27, 64, 125, 216\}$
   
2. One possible correct answer is $\left\{\left(\frac{1}{2}\right)^n \, : \, n \in \mathbb{N}\right\}$. 


## SF.2

1. $\{d,e,f,g,x,y,z\}$
2. $\{e,g\}$
3. $\{x,y,z\}$
4. $\{a,c,d,f\}$
5. $\emptyset$
6. 12
 
## SF.3

1. This is a function. The domain is $\{1,2,\dots,10\}$, the codomain is $\mathbb{R}$, and the range is $\{1/3, 2/3, 1, 4/3, \dots, 10/3\}$. 
2. This is not a function, because $2$ maps to two different outputs. 
3. This is a function. The domain is the set of all possible 3-bit strings; the codomain is $\mathbb{N}$, and the range is $\{0,1,2,3\}$. 


## SF.4

1. This function is injective. But it is not surjective since the range is just $\{1,4,9,16,\dots, 100\}$. 
2. This function is surjective, but not injective because $g(1.5) = g(2)$. 
3. This function is not surjective because no string can map to anything greater than 3. It is also not injective because $h(010) = h(011)$. 

None of these are bijective. 

## SF.5

1. $2$
2. $-3$
3. $3$
4. $-5$ 
5. $3628800$
6. $1$
7. $14$
8. $11$
9. $43$


## C.1

1. Forming a 6-digit octal integer requires a sequence of 6 choices with 8 options each, so the number is $8^6 = 262144$. 
2. The number of 6-digit octal integers beginning with a 0 is $8^5$ since we lock in the left digit and have 5 choices with 8 options each for the rest. Similarly the number of 6-digit octal integers that end in a 0 is also $8^5$. The number of 6-digit octal integers that do *both*, is $8^4$ by the same reasoning. So the total number that either start or end with a 0 is $8^5 + 8^5 - 8^4 = 61440$. 
 
## C.2

1. This is the same as forming a 20-bit string with exactly 5 "1" bits, so the number is $\binom{20}{5} = 15504$. 
2. This is the same as the number of 3-element subsets of $\{1,2,\dots,12\}$: $\binom{12}{3} = 220$ 

## C.3

1. This is just the number of rearrangements of seven distinct items $7! = 5040$. 
2. There are seven ways to give friend 1 the first book, then 6 ways to give the next book to friend 2, then 5 ways to give the third book to friend 3: $P(7,3) = 7 \cdot 6 \cdot 5 = 210$.  

## C.4

1. This is a problem of distributing eight identical objects to three people. That's a stars-and-bars situation where the diagram would have eight stars and two bars, so the number is $\binom{10}{2} = 45$. 
2. We first give one book to each friend, so now there are five objects going to three people, so the number of distributions is $\binom{7}{2} = 21$.


## RI.1

1. $1, 3, 7, 13, 21, 31$
2. $3.0, 1.5, 0.75, 0.375, 0.1875, 0.09375$
3. $4, 9, 22, 53, 122, 269$
4. $2, 3, 8, 19, 46, 111$

## RI.2

1. $2 + 5 + 8 + 11 + 14 = 40$
2. $.02 + .002 + .0002 = .0222$
3. $\sum_{n=1}^{101}n$
4. $\sum_{n=0}^5 \left(4 \cdot (1.5)^n\right)$

Multiple correct answers are possible for 3 and 4. 

## RI.3

Assume all indices start at 0 unless is says otherwise. 

| Sequence | Type | Closed formula | Recursive formula | 
| :----: | :----: | :------------: | :---------------: | 
| $2, 6, 10, 14, 18, 22, \dots$ | Arithmetic, amount = 4 | $f(n) = 2 + 4n$ | $a_0 = 2$, $a_n = a_{n-1} + 4$ if $n>0$ | 
| $4, \, 6, \, 9, \, 13.5, \, 20.25, \, \dots$ | Geometric, ratio = $1.5$ | $f(n) = 4(1.5)^n$ | $a_0 = 4$, $a_n = 1.5a_{n-1}$ if $n > 0$ |
| $2, .2, .02, .002, .0002, .00002, \dots$ | Geometrric, ratio = $0.1$ | $f(n) = 2(0.1)^n$ | $a_0 = 2$, $a_n = 0.1a_{n-1}$ if $n > 0$ |
| $10, 21, 32, 43, 54, 65, \dots$ | Arithmetic, amount = $11$ | $f(n) = 10 + 11n$ | $a_0 = 10$, $a_n = 11 + a_{n-1}$ if $n > 0$ | 

## RI.4

The function $f(n) = 2^{n-1} + 2^{2n-1}$ is a solution to the recurrence relation $a_0 = 1$, $a_1 = 3$ and for $n > 1$, $a_n = 6a_{n-1} - 8a_{n-2}$. 

First note that $f(0) = 2^{-1} + 2^{-1} = \frac{1}{2} + \frac{1}{2} = 1$, and $f(1) = 2^0 + 2^1 = 1 + 2 = 3$, so the initial conditions are met. 

For $n > 1$, on the right side of the recurrence relation replace $a_{n-1}$ with $f(n-1)$ and $a_{n-2}$ with $f(n-2)$. These are, respectively, 

\begin{align*}
f(n-1) &= 2^{(n-1)-1} + 2^{2(n-1) - 1} = 2^{n-2} + 2^{2n-3} \\
f(n-2) &= 2^{(n-2)-1} + 2^{2(n-2) - 1} = 2^{n-3} + 2^{2n-5}
\end{align*}

Now when we replace we get: 
\begin{align*}
6a_{n-1} - 8a_{n-2} &= 6\left(2^{n-2} + 2^{2n-3}\right) - 8\left(2^{n-3} + 2^{2n-5}\right) \\
&= 3\cdot 2 \left(2^{n-2} + 2^{2n-3}\right) - 2^3 \left(2^{n-3} + 2^{2n-5}\right) \\
&= 3\left(2^{n-1} + 2^{2n-2}\right) - \left(2^{n} + 2^{2n-2}\right) \\
&= 3 \cdot 2^{n-1} + 3 \cdot 2^{2n-2} - 2^n - 2^{2n-2} \\ 
&= 3\cdot 2^{n-1} - 2\cdot 2^{n-1} - 2\cdot 2^{2n-2} \\ 
&= 2^{n-1} - 2^{2n-1}
\end{align*}
This equals $a_n$ if a similar replacement is made, so the function solves the recurrence relation. 

## RI.5

The characteristic equation for this recurrence relation is 
$$r^2 -7r + +10 = 0$$
The left side factors into $(r-5)(r-2)$. So the characteristic equation has two distinct roots: $r = 5$ and $r=2$. 

The solution framework is
$$f(n) = c_1(2)^n + c_2(5)^n$$
The initial conditions require $f(0)=2$ and $f(1) = 1$. Therefore we have 
$$2 = c_1(2)^0 + c_2(5)^0$$
which gives $c_1 + c_2 = 2$. Also, 
$$1 = c_1(2)^1 + c_2(5)^1$$
which gives the equation $1 = 2c_1 + 5c_2$. We now have to solve the system

\begin{align*}
c_1 + c_2 &= 2 \\
2c_1 + 5c_2 &= 1
\end{align*} 

Multiply both sides of the first equation by $-2$:
\begin{align*}
-2c_1 + -2c_2 &= -4 \\
2c_1 + 5c_2 &= 1
\end{align*} 
Add the sides of these together to get: 
$$3c_2 = -3$$
Therefore $c_2 = -1$, and since $c_1 + c_2= 2$ this means $c_1 = 3$. 


Therefore the solution is 
$$f(n) = 3\cdot (2)^n -(5)^n$$. 

## RI.6

* **Base case**: We want to show directly that $1^3 + 2(1)$ is a multiple of 3. Since $1^3 + 2(1) =3$, the base case holds. 

* **Induction hypothesis:** Assume that for some positive integer $k$, $k^3 + 2k$ is a multiple of 3. 

* **Proof step:** We now want to show that 
$(k+1)^3 + 2(k+1)$ is a multiple of 3. A step that we might take from here is to expand out all the parenthesized expressions here and simplify, and look for $k^3 + 2k$ (the expression from the induction hypothesis) in the results. 

:::info
In fact, if we do this step, we get 
$$3 + 5 k + 3 k^2 + k^3$$
which equals 
$$(k^3 + 2k) + (3 + 3k + 3k^2)$$
From here we can argue that the first group is a multiple of 3 by the induction hypothesis, and the second group is a multiple of 3 because each term is a multiple of 3. Therefore the entire thing must be a multiple of 3. 
:::