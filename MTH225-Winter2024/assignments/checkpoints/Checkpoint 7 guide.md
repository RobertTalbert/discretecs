# Checkpoint 7 guide 

## C1

*"If it is raining outside, then I will bring an umbrella."*

1. It is raining outside
2. I will bring an umbrella
3. If I bring an umbrella, then it is raining outside. 
4. If I don't bring an umbrella, then it is not raining outside. 
5. If it is not rainig outside, then I will not bring an umbrella. 
6. It is raining outside but I don't bring an umbrella. 

### Common mistakes

These are the same common mistakes that have appeared on past Checkpoints, so please refer to past Checkpoint guides for details. **If you are making these common mistakes repeatedly, please speak with me (Talbert) about it.**

- **Writing the converse by simply switching the locations in the sentence without actually changing the hypothesis or conclusion**: "I will bring an umbrella if it is raining outside." Again, this is the same statement as the original. 
- **Not using the correct form of the negation:** It's not an if-then statement. 

## C2

For every integer $n \geq 5$ , $4n < 2^n$.

1. The predicate is $P(n): 4n < 2^n$. 
2. The base case is at $n = 5$. 
3. If $n = 5$, then the left side of the inequality is $4 \cdot 5 = 20$. The right side of the inequality is $2^5 = 32$. The left side is indeed less than the right side, so the base case holds. (The predicate is true when $n=5$.)
4. Assume that for some $k > 5$, that $4k < 2^k$. 
5. Now prove that $4(k+1) < 2^{k+1}$. 

### Common mistakes

- **Putting a quantifier on the predicate:** The phrase "For every integer $n \geq 5$ " *is not* part of the predicate. Quantifying a predicate in this way makes it no longer a predicate. Leave it off. 
- **Using "for all" instead of "for some" in the inductive hypothesis**: We are not assuming the predicate is true "for all" values of $n$ because then there would be no reason to prove anything. It's an existential quantifier, not a universal one. 
- **Not putting parentheses around $k+1$ in the inductive step:** That is, saying that we are going to prove that $4k+1$ is less than $2^{k+1}$. Those parentheses are necessary because $4(k+1)$ and $4k + 1$ aren't equal. 

## C3

Explanations are provided for study/review purposes; they aren't necessary in your submissions.

1. (a) False (because the number 2 is not a set, therefore it cannot be a subset of the set on the right)

   (b) True (because you're applying the function $n^2$ to the set containing 0, 1, 2, 3, 4 *and onward* -- that's what the dots mean -- so 5 belongs to that set.)

   (c) True ($\mathbb{Z}$ is the set of *all* integers)

   (d) True (every natural number is also an integer)

   (e) True (the empty set is a subset of every set; discussed in class)

2. (a) $\lbrace    3/2, 2, 5/2 \rbrace$ or $\lbrace  1.5, 2, 2.5 \rbrace$. This is mapping the "$n/2$" function over the set. 

   (b) $\lbrace  8,9, 10 \rbrace$. This is taking the set $\lbrace  8,9,10,11 \rbrace$ and filtering it using the predicate. 

   (c) $\lbrace  2, 4, 6, 8, 10 \rbrace$. This is taking the set $\lbrace  1, 2,\dots, 10 \rbrace$ and filtering it using the predicate. 

## C4 

1. $\lbrace  3 \rbrace$
2. $\lbrace  1,2,3,5 \rbrace$
3. $\lbrace  2 \rbrace$
4. $\lbrace  1,3,5 \rbrace$ (because $B \cap C$ is empty) 
5. $\lbrace  5 \rbrace$
6. 6


## C5 

1. This is the very definition of a [license plate problem](https://publish.obsidian.md/mth225/Combinatorics/License+plate+problem). There are six slots to fill. Each of the first three can be filled in 26 different ways. The last three can be filled in 36 different ways (with a letter or with a number). So the [Multiplicative Principle](https://publish.obsidian.md/mth225/Combinatorics/Multiplicative+principle) says the total count is $26 \cdot 26 \cdot 26 \cdot 36 \cdot 36 \cdot 36 = 820,025,856$. 
2. We use the [Principle of Inclusion and Exclusion](https://publish.obsidian.md/mth225/Combinatorics/Principle+of+Inclusion+and+Exclusion): The total count is the number of license plates that start with a vowel, plus the number that end in an even number, minus the number that both start with a vowel *and* end in an even number. If a license plate starts with a vowel, there are five choices for the first enty, then 26 for the next two, then 36 for the remaining three which gives a count of $5 \cdot 26^2 \cdot 36^3 = 157697280$. If a license plate ends in an even number, there are 26 choices for each of the first three entries, 36 for each of the next two, and then 5 for the final one (0,2,4,6, or 8) giving a total count of $26^3 \cdot 36^2 \cdot 5 = 113892480$. If a license plate does both, then there are 5 choices for the first and last entries, 26 for the second and third, and 36 for the fourth and fifth giving $5^2 \cdot 26^2 \cdot 36^2 = 21902400$ in all. So the total count we seek is: $157697280 + 113892480 - 21902400 = 249,687,360$. 

## C6

1. (a) $9! = 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 362880$. 

   (b) $\displaystyle{\binom{199}{197} = \frac{199!}{197! \cdot 2!} = \frac{199 \cdot 198}{2} = 19701}$. 


2. This number is given by the binomial coefficient $\displaystyle{\binom{6}{3} = 20}$. (Note, the set $\lbrace  0,1,2,3,4,5 \rbrace$ has six elements.)

---

## S1, S2, and S3

There were no attempts on S1, only one attempt on S2, and only two on S3. If you attempted S2, please [use a calculator](https://www.calculator.net/binary-calculator.html) to check your work. If you attempted S3, please use the [Truth Table generator](https://web.stanford.edu/class/cs103/tools/truth-table-tool/) to check your answers. 

## S4

1. (a) True 

   (b) False ($13^2 = 169$ which does not end in a 3)

   (c) False (because, for example, $9^2 \neq 100$)

   (d) True (for example, $13$ from part (b))

2. Some problems on this quiz have different answers. (*Yes, this is the same statement that was on Checkpoint 6, I forgot to change it.*) 

## S5

$a_0 = 2$ and $a_1 = 3$. 

- $a_2 = 2a_1 + a_0 = 2(3) + 2 = 8$
- $a_3 = 2a_2 + a_1 = 2(8) + 3 = 19$
- $a_4 = 2a_3 + a_2 = 2(19) + 8 = 46$
- $a_5 = 2a_4 + a_3 = 2(46) + 19 = 111$
- $a_6 = 2a_5 + a_4 = 2(111) + 46 = 268$. 

## S6

1. $R(1) = 1, R(2) = 5, R(3) = 11$. 
2. In each step, the image copies the image from the previous step and sandwiches it between two new rows of blocks. The number of blocks in each new row is equal to the current step number (2 blocks in each row in step 2, 3 blocks in each row in step 3, etc.). Therefore $R(n) = R(n-1) + 2n$. 

## S7

Explanations for the non-functions are provided, but not necessary in your submissions.

1. Function. Domain = $\lbrace c,u,v,z\rbrace$. Codomain = $\lbrace e,m,q,g,x \rbrace$. Range = $\lbrace e,m,g \rbrace$. 
2. Not a function. ($9$ has no output)
3. Function. Domain = $\lbrace k,d,n,y \rbrace$. Codomain = $\lbrace r,p,o,m,c \rbrace$. Range = $\lbrace r,p,m,c \rbrace$. 
4. Not a function. ($4$ maps to two things)
5. Function. Domain = $\lbrace 1,2,9,6,4 \rbrace$. Codomain = $\lbrace 7,9,4 \rbrace$. Range = $\lbrace 9,4 \rbrace$. 
6. Not a function. ($a$ maps to two things)

## S8

1. The function is bijective. 
2. The function is injective, but it is not surjective because for example, the number $0$ cannot be an output. (The only outputs are $2,5,8,11,14,\dots$.)
3. The function is not injective, because $1,2,3,4$ all map to $b$. It is also not surjective, because $a$ is never output. (Notice, this is the same function as mapping #5 from Skill C7, with the points renamed.)