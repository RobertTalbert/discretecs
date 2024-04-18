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

### Common mistakes 

- **Answering "True" on 1(c):** That is, stating that $1/2$ is an integer. I'm not sure why this happened but please review [what an integer is](https://publish.obsidian.md/mth225/Computer+Arithmetic/Integers). 
- **Giving duplicate elements in 2(c):** For example saying that the set is $\lbrace 0, 1, 2, 0, 1, 2, 0, 1, 2, \dots \rbrace$. This is incorrect set notation because sets cannot contain duplicate elements. 

## C4 

1. $\lbrace 5 \rbrace$
2. $\lbrace 1,2,3,5,7\rbrace$
3. $\lbrace 0,10 \rbrace$
4. $\lbrace 3 \rbrace$
5. $\lbrace \emptyset, \lbrace 7 \rbrace \rbrace$
6. $12$

### Common mistakes

- **Giving the cardinality on part 5 when it was asking for the set:** If this were asking for the cardinality, there would have been vertical bars around the set: $|{\cal{P}}(D)|$. But there were no such symbols. 
- **Giving the set on part 6 when it was asking for the cardinality:** Those vertical bar symbols *were* around $A \times C$ though. 


## C5 

(The parts here were mistakenly labeled "3" and "4" on the Checkpoint form, instead of "1" and "2". They are renumbered below.)

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

### Common mistakes

All of the common mistakes were concentrated on part 2(b). 

- **Assuming that the words *start* with an "A"**: For example, saying the count is $7^3$ because it's a license plate problem with "A" in the first slot and a free choice of 7 letters for the remaining 3. It doesn't say that the *first* letter is "A", just that "A" has to be in the word somewhere. (You might think that, therefore, $4 \cdot 7^3$ should be correct because there are 4 choices for where to put an "A" in order to ensure that the word has at least one, and then free choice of 7 letters for the other 3 for each choice of that "A"s position. This is close, $4 \cdot 7^3 = 1372$. But it double-counts many words, for example if you stick "A" in the first letter and then choose B, C, and then A for the final letter, this is counted separately from if you put the "A" in the last position and chose A for the first letter, then B, then C -- but they spell out the same word.) 
- **Assuming repetitions aren't allowed:** For example, saying that the count is $6 \cdot 5 \cdot 4$ because if "A" has to be in the word, then there are three letters remaining and six choices for the first letter, five for the second, then 4 for the third/last. But that's not the case -- it says repetitions are allowed and so the number of choices wouldn't drop. (There are other issues as well with this approach.)
- **Treating it like a simple license plate problem:** For example, saying the count is $7^4$ because there are four letters in the word and 7 choices each. The problem with this, is that it doesn't account for the fact that "A" must be one, possibly more than one, of the letters. That number $7^4$ counts *all possible* words, including ones like `BCDE` with no "A"s in them. 
- **Using a binomial coefficient (and nothing else):** For example, saying the count is $\binom{7}{3}$, which is incorrect because this is the total number of all *three* letter words from the entire set, so the length of the word is incorrect and also it allows for words that don't have "A" in them. Also incorrect is $\binom{7}{4}$ because although this chooses four-letter words, it does not take ordering into account (it would treat `BCDE` as the same selection as `DCBE`) and also allows for words with no "A"s. 


---

[Remember it's now our policy](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 

| $p$ | $q$ | $r$ | $\neg p$ | $(\neg p) \vee r$ | $((\neg p) \vee r) \rightarrow q$ |
| --- | --- | --- | -------- | ----------------- | --------------------------------- |
| T   | T   | T   | F        | T                 | T                                 |
| T   | T   | F   | F        | F                 | T                                 |
| T   | F   | T   | F        | T                 | F                                 |
| T   | F   | F   | F        | F                 | T                                 |
| F   | T   | T   | T        | T                 | T                                 |
| F   | T   | F   | T        | T                 | T                                 |
| F   | F   | T   | T        | T                 | T                                 |
| F   | F   | F   | T        | T                 | F                                 |

| $p$ | $q$ | $p \wedge q$ | $\neg(p \wedge q)$ | $\neg p$ | $\neg q$ | $(\neg p) \wedge (\neg q)$ |
| --- | --- | ------------ | ------------------ | -------- | -------- | ------------------- |
| T   | T   | T            | F                  | F        | F        | F                   |
| T   | F   | F            | T                  | F        | T        | F                   |
| F   | T   | F            | T                  | T        | F        | F                   |
| F   | F   | F            | T                  | T        | T        | T                   |

The statements are not logically equivalent. 



## S4

1. (a) False

   (b) False

   (c) False (There are some integers with two digits)

   (d) True (for example, $x=8$, because $8^2$ ends in a 4)

2. All prime numbers are odd. (Or, "not even")
 
 
## S5

- $a_2 = 3a_1 + 4a_0 = 3(8) + 4(5) = 44$
- $a_3 = 3a_2 + 4a_1 = 3(44) + 4(8) = 164$
- $a_4 = 3a_3 + 4a_2 = 3(164) + 4(44) = 668$
- $a_5 = 3a_4 + 4a_3 = 3(668) + 4(164) = 2660$
- $a_6 = 3a_5 + 4a_4 = 3(2660) + 4(668) = 10652$
 

## S6

1. $R(1) = 5$, $R(2) = 10$, $R(3) = 17$. 
2. The two squares that stick off to the bottom-left and top-right are always present, so focus on how the recursion uses the "middle" part of each figure. In each step, the middle portion from the previous figure is included, and adds a new column to the figure and then a new row across the top. The height of the column in any step appears to be the step number plus 1, and the row across the top has width equal to the step number. So the recurrence relation should be $R(n) = R(n-1) + (n+1) + n$ which simplifies to $R(n) = R(n-1) + 2n + 1$. 

## S7

1. Not a function. 
2. Not a function. 
3. Function. Domain = $\lbrace t,h \rbrace$. Range and codomain = $\lbrace v,u \rbrace$. 
4. Function. Domain = $\lbrace 0,6 \rbrace$. Codomain = $\lbrace 2, 9 \rbrace$. Range = $\lbrace 9 \rbrace$. 
5. Function. Domain = $\lbrace f,w,u,a \rbrace$. Codomain and range = $\lbrace l,t,d,b \rbrace$.
6. Function. Domain = $\lbrace o,m,d,n,y \rbrace$. Codomain and range = $\lbrace o,p,d,l \rbrace$. 


## S8

1. Bijective. 
2. Injective but not surjective, because for example the number 500 can never be output since its binary representation (`111110100`) has more than 8 bits.
3. Not injective, since `00000000` and `1000000` both map to `00000000`. Also not surjective because no bitstring with a `1` in either the first or last position can be output (for example `11111111`).  

## S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 
| 1 | Geometric | $a(n) = 4 \cdot \left( \frac{1}{2} \right)^n$ | $a_0 = 4$ and $a_n = \frac{1}{2}a_{n-1}$ |
| 2 | Neither | n/a | n/a |  
| 3 | Arithmetic | $a(n) = 4 + 4n$ | $a_0 = 4$ and $a_n = a_{n-1} + 4$ | 
| 4 | Neither | n/a | n/a | 



## S10

The characteristic equation for the recurrence relation is
$$r^2 = 7r -12$$
Getting all the terms on the left gives $r^2 - 7r + 12 = 0$. This factors into $(r-4)(r-3) = 0$ on the left, so the characteristic roots are $r = 4$ and $r=3$. 

The framework for the solution using those roots is: 
$$a(n) = c_1 (4)^n + c_2 (3)^n$$

Plugging in $n=0$ gives the equation $4 = c_1 (4)^0 + c_2(3)^0$ which simplifies to $c_1 + c_2 = 4$. 

Plugging in $n=1$ gives the equation $7 = c_1 (4)^1 + c_2(3)^1$ which simplifies to $4c_1 + 3c_2 = 7$. 

Let's use the "elimination" method for solving the system of equations. We first multiply both sides of the first equation by $-3$ to get $-3c_1 - 3c_2 = -12$. Now add both sides to the corresponding sides of the second equation to get $c_1 = -5$. 

To find $c_2$, plug $c_1 = -5$ in to $c_1 + c_2 = 4$ to get $-5 + c_2 = 4$. Now solve for $c_2$ to get $c_2 = 9$. 

So the final solution is
$$a(n) = -5 (4)^n + 9 (3)^n$$
