# Checkpoint 11 guide 

## C1

1. The temperature is 375
2. The oven is ready
3. If the oven is ready, then the temperature is 375
4. If the oven is not ready, then the temperature is not 375
5. If the the temperature is not 375, then the oven is not ready
6. The temperature is 375 but the oven is not ready

## C2

1. The predicate $P(n)$ is "$3^n - 1$ is even"
2. $n=1$
3. If $n=1$, then $3^1 - 1 = 3 - 1 = 2$ and that's even (no explanation needed here as this is common knowledge), so the base case holds. 
4. Assume that $3^k-1$ is even for some $k \geq 1$. 
5. Prove that $3^{k+1} - 1$ is even. 

## C3

1. (a) False (nothing is an element of the empty set)

   (b) False ($6$ is in the first set but not in the second one)

   (c) False ($1/2$ is not an integer)

   (d) False (for example $-1 \in \mathbb{Z}$ but $-1 \not \in \mathbb{N}$)

   (e) True (the empty set is a subset of every set) 

2. (a) $\lbrace 1, 4, 7, 10, 13, \dots \rbrace$

   (b) Incorrect syntax ($2^n$ is not a predicate, and if it's a function to map then the function has to come first)

   (c) $\lbrace 0, 1, 2 \rbrace$ (Mapping the "x mod 3" function to each element of that set)

## C4 

1. $\lbrace 5 \rbrace$
2. $\lbrace 1,2,3,5,7\rbrace$
3. $\lbrace 0,10 \rbrace$
4. $\lbrace 3 \rbrace$
5. $\lbrace \emptyset, \lbrace 7 \rbrace \rbrace$
6. $12$

## C5 

(The parts here were mistakenly labeled "3" and "4", instead of "1" and "2". They are renumbered below.)

1. This is a license plate problem with eight slots to fill and two choices per slot, so the count is $2^8 = 256$. 
2. Use the Principle of Inclusion and Exclusion. The number of 10-"bit" ternary strings that start with a 2 is $3^9 = 19683$ (fix a "2" in the leftmost slot and then choose freely from 0, 1, or 2 for the other 9). This is also the number of ternary strings that end in a 2 for the same reason. But this counts the ternary strings that *both* start *and* end in a 2 twice, so that number has to be subtracted out of the total. This number is $3^8 = 6561$. Therefore the complete count is $19683 + 19683 - 6561 = 32805$. 



## C6

1. (a) $7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5040$

   (b) $\displaystyle{\binom{500}{497} = \frac{500!}{497! \cdot 3!} = \frac{500 \cdot 499 \cdot 498}{3 \cdot 2 \cdot 1} = 20708500}$. 

2. (a) If we require "A" to be in the subset, then we are choosing a 3-element subset from the remaining six letters. The number of 3-element subsets of a 6-element set is by definition $\binom{6}{3} = 20$. 

   (b) We can find this number by taking the number of all possible 4-letter words made from these letters, and subtracting off the number that have no "A"s at all in them. What's left over must be the number of four-letter words with at least one "A". 
   
   The number of words that can possibly be formed from these seven letters is $7^4 = 2401$. (It's a license plate problem where there are four slots to fill and seven choices each.) The number of words that *don't* contain the letter "A", is $6^4 = 1296$ (license plate problem with four slots to fill and six choices each). The number of words that have at least one "A" in them, is the total number of words minus the number that don't have any "A"s: $2401 - 1296 = 1105$. 

   *Alternate solution:* The four letter word we are forming must have at least one "A" in it. This means it can have 1 "A", 2 "A"s, 3 "A"s, or 4 "A"s. Count each of these four cases separately. If there is only 1 "A" then there are $\binom{4}{1} = 4$ places where it can go, and we can choose freely among 6 remaining letters for the other 3 positions; so there are $6^3 \cdot 4 = 864$ words that have just one "A". If there are 2 "A"s, then there are $\binom{4}{2} = 6$ ways to insert those into the word, and $6^2 = 36$ choices for the remaining slots giving a total of $6 \cdot 36 = 216$ words with 2 "A"s. If there are 3 "A"s, then there are $\binom{4}{1} = 4$ places to put the one letter that is *not* an "A", and 6 choices of letter, giving a total of $24$ words. And there is only one word that has four "A"s. So the grand total of words with at least one "A" is $864 + 216 + 24 + 1 = 1105$. 


**Note**: If you interpreted the problem in 2(b) as saying "exactly one A", as the examples show, then this will be counted as a "simple" error and you'll get credit for this as long as the solution is correct and consistent with that interpretation. Here is what this would look like. If there is to be exactly one "A", then there are four positions where it could go in a four-letter word. For the other three positions, treat it as a license plate problem with three slots and six possible ways to fill each. This would give $6^3 = 216$ words; since there are four positions where the "A" could go, the total count is $4 \cdot 6^3 = 864$. 

---

[Remember it's now our policy](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 

## S4

 
## S5



## S6


## S7



## S8


## S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 



## S10

<!-- The characteristic equation for the recurrence relation is
$$r^2 = 3r + 4$$
Getting all the terms on the left gives $r^2 - 3r - 4 = 0$. This factors into $(r-4)(r+1) = 0$ on the left, so the characteristic roots are $r = 4$ and $r=-1$. 

The framework for the solution using those roots is: 
$$a(n) = c_1 (4)^n + c_2 (-1)^n$$

Plugging in $n=0$ gives the equation $5 = c_1 (4)^0 + c_2(-1)^0$ which simplifies to $c_1 + c_2 = 5$. 

Plugging in $n=1$ gives the equation $8 = c_1 (4)^1 + c_2(-1)^1$ which simplifies to $4c_1 - c_2 = 8$. 

Using the "elimination" method for solving the system of equations, we add the left and right sides of the first equation to the left and right sides of the second. The $c_2$ term cancels, leaving us with $5c_1 = 13$. Therefore $c_1 = 13/5$. 

To find $c_2$, plug $c_1 = 13/5$ in to $c_1 + c_2 = 5$ to get $13/5 + c_2 = 5$. Now solve for $c_2$ to get $c_2 = 5 - 13/5 = 12/5$. 

So the final solution is
$$a(n) = \frac{13}{5} (4)^n + \frac{12}{5} (-1)^n$$

(Note: Using decimals, $13/5 = 2.6$ and $12/5 = 2.4$. These are OK to use here.) -->