# Checkpoint 9 guide 

## C1

*"The program will terminate if the input is zero."*

1. The input is zero
2. The program will terminate
3. If the program terminates, then the input is zero 
4. If the program does not terminate, then the input is not zero 
5. If the ihput is not zero, the program will not terminate
6. The input is zero but the program did not terminate
 

## C2

Let $x$ be a positive real number. Then for any $n \in \mathbb{N}$, we have $(1+x)^n \leq 1 + nx$.

1. The predicate is $P(n): (1+x)^n \leq 1 + nx$.
2. The base case is at $n = 0$. 
3. If $n = 0$, then the left side of the inequality is $(1+x)^0$ which equals $1$, and the right side is $1 + (0)(x)$ which also equals $1$. Since the left side is indeed less than or equal to the right side, the base case holds. 
4. Assume that for some $k \geq 1$, that $(1+x)^k \leq 1 + kx$. 
5. Now prove that $(1+x)^{k+1} \leq 1 + (k+1)x$. 


## C3

Explanations are provided for study/review purposes; they aren't necessary in your submissions.

1. (a) False (because nothing is an element of the empty set)

   (b) False (because not every element of the set on the left is an element of the set on the right)

   (c) True ($\mathbb{Z}$ is the set of *all* integers, including the negative ones)

   (d) False (because not every integer is in the natural numbers, for example $-5$)

   (e) True (the empty set is a subset of every set; discussed in class)

2. (a) $\lbrace   5,7,9  \rbrace$ or This is mapping the " $n+1$ " function over the set. 

   (b) $\lbrace  8, 10 \rbrace$. This is taking the set $\lbrace  8,9,10,11 \rbrace$ and filtering it using the predicate. 

   (c) Incorrect syntax because $a^2$ is not a predicate, it's a function to map over the domain set and so it's supposed to come first. 

## C4 

1. $\lbrace  5 \rbrace$
2. $\lbrace  1,2,3,5,7 \rbrace$
3. $\lbrace  0, 10 \rbrace$
4. $\lbrace  3,5 \rbrace$ 
5. $\lbrace  0,3,5,10 \rbrace$
6. $\lbrace (1,7), (3,7), (5,7), (7,7) \rbrace$ 


## C5 

1. It's literally a license plate problem. There are 10 choices for the four places that digits go, and 26 choices for the three letters. So the full count is $10^4 \cdot 26^3 = 175760000$. 
2. Use the Principle of Inclusion and Exclusion: 
   - The number of plates that start with an odd number on the left is $5 \cdot 10^3 \cdot 26^3 = 87880000$ (or, reason that it's exactly half of the license plates you counted in part 1)
   - The number of plates that end in an even number is the same, $87880000$ and for the same reasons.
   - The plates that **both** start with an odd number **and** end in an even number have been counted twice. There are $5^2 \cdot 10^2 \cdot 26^3= 43940000$ of those. (You can also reason that it's exactly half the plates that begin with an odd number; or one-quarter of all the plates you counted in the first part).
   - Therefore the full count is the first number plus the second, minus the third to correct for the overcount: $87880000 + 87880000 - 43940000 = 131820000$. 

## C6

1. (a) $5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120$. 

   (b) $\displaystyle{\binom{700}{698} = \frac{700!}{698! \cdot 2!} = \frac{700 \cdot 699}{2} = 244650}$. 

2. This is a dots-and-dividers problem where there are 20 "dots" and 4 "dividers" (five people, so four changes between the people). The diagrams for this distribution would correspond to a binary string of length 24 and weight 4. Therefore the count is $\displaystyle{\binom{24}{4} = \frac{24!}{4! \cdot 20!} = \frac{24 \cdot 23 \cdot 22 \cdot 21}{4 \cdot 3 \cdot 2 \cdot 1} = 10626}$. 

---

[Remember from the last Checkpoint guide](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 

## S4

## S5


## S6


## S7


## S8
