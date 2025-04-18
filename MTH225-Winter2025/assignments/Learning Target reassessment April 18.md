# Learning Target reassessment April 18 solutions guide 

[Click here for the form](https://drive.google.com/open?id=1S4DimqkSU82SiqXEHzHWpQkzu47v6qh9&usp=drive_fs) with the questions on it. 

## Learning Target 7

1. Here's a truth table showing the propositions P → Q, Q → R, and P → R:

| P | Q | R | P → Q | Q → R | P → R |
|---|---|---|-------|-------|-------|
| T | T | T | T     | T     | T     |
| T | T | F | T     | F     | F     |
| T | F | T | F     | T     | T     |
| T | F | F | F     | T     | F     |
| F | T | T | T     | T     | T     |
| F | T | F | T     | F     | T     |
| F | F | T | T     | T     | T     |
| F | F | F | T     | T     | T     |

The premises are simultaneously true in rows 1, 5, 7, and 8 and in those rows, the conclusion is also true. Therefore this is a valid argument. 

2. Here are the truth tables for ¬(P → Q) and P → (¬Q): 

| P | Q | P → Q | ¬(P → Q) | ¬Q | P → (¬Q) |
|---|---|-------|----------|-----|----------|
| T | T | T     | F        | F   | F        |
| T | F | F     | T        | T   | T        |
| F | T | T     | F        | F   | T        |
| F | F | T     | F        | T   | T        |

The two expressions have different outcomes in rows 3 and 4, so they are not logically equivalent. 

## Learning Target 10 

1.
    - (a) Incorrect syntax (since it has a predicate first)
    - (b) Correct syntax, and equal to $\lbrace -10, -9, -8 \rbrace$.
    - (c) Correct syntax, and equal to $\lbrace 0, 2, 4, 6, 8, 10 \rbrace$. 
2. .
   - (a) False ($\emptyset$ is a set and is not one of the numbers 0, 1, or 2)
   - (b) False (the first set contains 0 as an element but the second one doesn't)
   - (c) True 
   - (d) False (the first set contains *all* natural numbers, the second one does not)
   - (e) False (none of the elements in the first set are in the second, because the second set has no elements)

## Learning Target 12

1. Not a function (because $f$ maps to two outputs)
2. Surjective, but not injective (because $p$ and $c$ both map to 2)
3. Injective, but not surjective (because nothing maps to 5)
4. Neither injective nor surjective (not injective because three point map to $w$; not surjective because nothing maps to $e$)
5. Not a function (because $v$ doesn't have an output)
6. Injective but not surjective (because nothing maps to $s$)

## Learning Target 13 

1. There are 19 items with two possible outcomes per item, so the total is $2^{19} = 524288$. 
2. The total is the number of math majors, plus the number of computer science majors, minus the number of double-majors because we double counted those: $14 + 11 - 5 = 20$. 
3. A two-letter string cannot start with A and also start with B, so we can count the two cases separately and then add them (Additive Principle). There are 26 possible strings that start with A (because the second character is a free choice) and similarly 26 possible strings that start with B, so the total is $26 + 26 = 52$. 


## Learning Target 14

1. To make the pizza we are selecting 4 (different) toppings from the 16 available, and the order doesn't matter because it's the same choice of toppings regardless. So the total is $\binom{16}{4} = \frac{16!}{4! 12!} = \frac{16 \times 15 \times 14 \times 13}{6 \times 5 \times 4 \times 3 \times 2 \times 1} = 1820$. 
2. Out of the 20 positions we are choosing 2 to remain blank. Since this is selecting 2 from 20 and the order of selection doesn't matter,the total is $\binom{20}{2} = \frac{20!}{2! 18!} = \frac{20 \times 19}{2} = 190$. 
3. We are arranging 8 different items, so the number is $8! = 40320$. 

## Learning Target 15

1. Neither
2. Geometric with a common ratio of 3.
    - Closed formula: $a(n) = 2 \times 3^n$ 
    - Recurrence relation: $a(0) = 2$ and $a_n = 3a_{n-1}$ when $n > 0$. 
3. Arithmetic with a common step of 1. 
   - Closed formula: $a(n) = 11 + n$ 
   - Recurrence relation: $a(0) = 11$ and $a_n = a_{n-1} + 1$ for $n > 0$
4. Geometric with a common ratio of $0.5$ or $\frac{1}{2}$. 
   - Closed formula: $a(n) = 100 \times (0.5)^n$ 
   - Recurrence relation: $a(0) = 100$ and $a_n = 0.5a_{n-1}$ for $n > 0$.  