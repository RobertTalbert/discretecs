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


### Common mistakes

- **Answering "4" for part 6:** The question does not ask for the cardinality of the set, it asks for the set itself. Had it asked for cardinality it would have said $|A \times D|$. 
- **Wrong data type in part 6:** The elements of the [cartesian product](https://publish.obsidian.md/mth225/Sets+and+Functions/Cartesian+product) $A \times D$ are *tuples*, not two-element sets. Therefore $(3,7)$ is a valid element but not $\lbrace 3, 7 \rbrace$. Another valid element that needs to appear here is the tuple $(7,7)$ which is not the same as the set $\lbrace 7 \rbrace$. In the past, getting the wrong data type on a cartesian product was a "simple" error but this time it's not simple because it ends up excluding one of the elements. 

## C5 

1. It's literally a license plate problem. There are 10 choices for the four places that digits go, and 26 choices for the three letters. So the full count is $10^4 \cdot 26^3 = 175760000$. 
2. Use the Principle of Inclusion and Exclusion: 
   - The number of plates that start with an odd number on the left is $5 \cdot 10^3 \cdot 26^3 = 87880000$ (or, reason that it's exactly half of the license plates you counted in part 1)
   - The number of plates that end in an even number is the same, $87880000$ and for the same reasons.
   - The plates that **both** start with an odd number **and** end in an even number have been counted twice. There are $5^2 \cdot 10^2 \cdot 26^3= 43940000$ of those. (You can also reason that it's exactly half the plates that begin with an odd number; or one-quarter of all the plates you counted in the first part).
   - Therefore the full count is the first number plus the second, minus the third to correct for the overcount: $87880000 + 87880000 - 43940000 = 131820000$. 


### Common mistakes 

- **Thinking that there are 9 digits in the range 0 through 9**: It's 10, not 9. 
- **Misinterpreting the word "or" in part 2:** The word "or" means -- and has always meant -- *one or the other condition, **or both***. Again, we have always taken this "inclusive" interpretation of the word "or" dating all the way back to the unit on logic (see the truth table for a [disjunction](https://publish.obsidian.md/mth225/Logic/Disjunction)). Some students misinterpreted this as an "exclusive" or ("one or the othe r*but not both*", which again is incorrect) or got it mixed up with "and". 
- **Not subtracting out the double-counted plates in part 2:** See above for why. Some of the instances of this mistake stemmed from misinterpreting "or" as described above. 

## C6

1. (a) $5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120$. 

   (b) $\displaystyle{\binom{700}{698} = \frac{700!}{698! \cdot 2!} = \frac{700 \cdot 699}{2} = 244650}$. 

2. This is a dots-and-dividers problem where there are 20 "dots" and 4 "dividers" (five people, so four changes between the people). The diagrams for this distribution would correspond to a binary string of length 24 and weight 4. Therefore the count is $\displaystyle{\binom{24}{4} = \frac{24!}{4! \cdot 20!} = \frac{24 \cdot 23 \cdot 22 \cdot 21}{4 \cdot 3 \cdot 2 \cdot 1} = 10626}$. 

### Common mistakes

Some of these are not "common" because they only happened 1-2 times, but it's instructive to see some plausible wrong answers and understand why they are wrong. 

- **Giving an answer of $5^{20}$ for part 2:** The reasoning here is that we treat it like a license plate problem where there are twenty slots (one per card) and 5 choices per slot -- basically look at each card and choose which person it will go to. The reason this doesn't work is that it overcounts: For example if I put "Alice" in the blank for the first 10 cards and "Bob" in the blank for the last 10 cards, that's one selection. If I put "Alice" in the blanks for the even numbered cards and "Bob" in the blanks for the odd numbered cards, that's considered to be a different distribution... but it's not, because Alice and Bob still end up with 10 cards each, and the cards are identical. All the possible ways to give Alice 10 cards and Bob 10 cards are going to be counted separately, which produces a massive overcount. 
- **Giving an answer of $20^5$ for part 2:** This is also treating it like a license plate problem where this time there would be five blanks with 20 options each. The blanks would correspond to the people, and the 20 options would correspond to the number of cards each person gets. But this also produces an overcount, this time because it counts some distributions that are impossible, such as giving 20 cards to each person. 
- **Giving an answer of $\binom{20}{5}$ for part 2:** This would represent a situation where we have 20 cards in a stack and we are going to pull out 5 of them, without regard for the order of the selection, and count the number of ways this can happen. It's like taking a 20-card deck of playing cards and counting the number of 5-card hands that can be dealt from that deck. But this assumes that the cards are distinguishable from each other, which is not the case. They are identical, so all selections of 5 cards from the stack will be the same. At any rate, choosing 5 cards from a stack of 20 is not what we are actually doing here, we are giving out all 20 cards to 5 people. 

---

[Remember from the last Checkpoint guide](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 


| $p$ | $q$ | $r$ | $\neg q$ | $p \wedge (\neg q)$ | $\neg r$ | $(p \wedge (\neg q)) \vee (\neg r)$ |
| --- | --- | --- | -------- | ------------------- | -------- | ----------------------------------- |
| T   | T   | T   | F        | F                   | F        | F                                   |
| T   | T   | F   | F        | F                   | T        | T                                   |
| T   | F   | T   | T        | T                   | F        | T                                   |
| T   | F   | F   | T        | T                   | T        | T                                   |
| F   | T   | T   | F        | F                   | F        | F                                   |
| F   | T   | F   | F        | F                   | T        | T                                   |
| F   | F   | T   | T        | F                   | F        | F                                   |
| F   | F   | F   | T        | F                   | T        | T                                   |


| $p$ | $q$ | $p \rightarrow q$ | $\neg(p \rightarrow q)$ | $\neg p$ | $(\neg p) \vee q$ |
| --- | --- | ----------------- | ----------------------- | -------- | ----------------- |
| T   | T   | T                 | F                       | F        | T                 |
| T   | F   | F                 | T                       | F        | F                 |
| F   | T   | T                 | F                       | T        | T                 |
| F   | F   | T                 | F                       | T        | T                 |

The statements are not logically equivalent (in fact they are negations of each other). 

## S4

1. (a) False

   (b) False ($11^2 = 121$ and this does not end in a 3)

   (c) False (counterexample: $x = 10$)

   (d) True (example: $x = 11$)
   
2. *Some trucks are inexpensive*. (Other correct formulations are possible)

 
## S5

- $a_2 = 2a_1 + 4a_0 = 2(5) + 4(1) = 14$
- $a_3 = 2a_2 + 4a_1 = 2(14) + 4(5) = 48$
- $a_4 = 2a_3 + 4a_2 = 2(48) + 4(14) = 152$
- $a_5 = 2a_4 + 4a_3 = 2(152) + 4(48) = 496$
- $a_6 = 2a_5 + 4a_4 = 2(496) + 4(152) = 1600$


## S6

1. $R(1) = 6$, $R(2) = 11$, $R(3) = 16$. 
2. In each step, the new step takes the figure in the old step and does two things to it: Adds one block to the upward-pointing part, and adds two blocks to each of the downward-pointing parts. That's 5 blocks total added on to the previous figure (and this doesn't vary with the step, it's always just 5). So the recurrence relation is $R(n) = R(n-1) + 5$. 

## S7

1. Function. Domain = $\lbrace 4,3,9,6,5 \rbrace$. Codomain = $\lbrace 5,0,4,1,6 \rbrace$. Range = $\lbrace 5,0,4,6 \rbrace$. 
2. Not a function ($q$ has no output)
3. Not a function ($g$ has two outputs)
4. Function. Domain = $\lbrace o,p,j,x \rbrace$. Comdomain and range = $\lbrace s,q,i,h \rbrace$. 
5. Function. Domain = $\lbrace n,s,e,o \rbrace$. Comdomain and range = $\lbrace 3,5,6 \rbrace$. 
6. Function. Domain = $\lbrace 0,4,6,8 \rbrace$. Comdomain and range = $\lbrace 2,8,1 \rbrace$. 


## S8

1. This function is surjective but not injective, because for example Albert Einstein and Angelina Jolie both map to "A". 
2. This function is injective but not surjective, because for example the bit string `1111111100000000` never appears as an output (since the outputs never contain a `1` in their first 8 bits). 
3. This is a bijection. 