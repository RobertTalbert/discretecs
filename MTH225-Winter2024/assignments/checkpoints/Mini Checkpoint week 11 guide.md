# Mini-Checkpoints from Week 11

Click below for the Mini Checkpoints: 
- [C3 and C4](https://docs.google.com/document/d/1os1cKeSy091qydib4d9XhU5zBFOBXThsTKnPfZrzl-Q/edit?usp=sharing)
- [C5 and C6](https://drive.google.com/file/d/1fzGn8x4pNvaBFf9mrcKXr8BJ77pf0RjZ/view?usp=sharing)
- [C1 and C2](https://drive.google.com/file/d/1LD1ru5pwyqf0g_0ebFmUjGaxi0214wRn/view?usp=sharing)

## Skill C1 (Friday March 29)

1. The water is boiling
2. The temperature is over 200 degrees
3. If the temperature is over 200 degrees then the water is boiling
4. If the temperature is not over 200 degrees then the water is not boiling
5. If the water is not boiling then its temperature is not over 200 degrees
6. The water is boiling but its temperature is not over 200 degrees

## Skill C2 (Friday March 29)

1. The predicate $P(n)$ is the statement that $9^n - 1$ is divisible by $8$. 
2. $n = 0$ is the base case
3. If $n = 0$ then $9^n - 1 = 9^0 - 1 = 1 - 1 = 0$, and $0$ is divisible by $8$. So the base case holds. 
4. Assume $9^k - 1$ is divisible by $8$ for some nonnegative integer $k$. 
5. Prove that $9^{k+1} - 1$ is divisible by $8$. 

### Common mistakes: 

- **Saying $n=1$ is the base case:** The smallest nonnegative integer is $0$, not $1$. 
- **Using $k-1$ instead of $k+1$ in the inductive step**: That is, saying that we will prove that $9^{k-1} - 1$ is divisible by $8$. This *has* to be $k+1$ since the way induction works is to assume that the proposition is true at a certain level $k$ and then prove that the proposition is true at **the next level**. That "next level" is $k+1$ not $k-1$. 


## Skill C3 (Monday March 25)

1. (a) False

   (b) False

   (c) True

   (d) True

   (e) False 

2. (a) $\lbrace -2, 1, 4 \rbrace$

   (b) $\lbrace 3,5 \rbrace$

   (c) Incorrect syntax; or $\lbrace True, False \rbrace$

### Common mistakes

- **Stating that 1(d) is False:** That is, that $\mathbb{N}$ is not a subset of $\mathbb{Z}$. But $\mathbb{N}$ *is* a subset of $\mathbb{Z}$ because $\mathbb{N}$ consists of all integers greater than or equal to $0$, so by definition every element of $\mathbb{N}$ is an element of $\mathbb{Z}$. 
- **Stating that 1(e) is True:** That is, that $\emptyset \in \lbrace 1,2,3 \rbrace$. This would say that $\emptyset$ is an *element* of the set $\lbrace 1,2,3 \rbrace$, but this is not so --- the only elements of this set are the numbers 1, 2, and 3. It's possible there was confusion between the concept of "subset" and the concept of "element". The empty set $\emptyset$ is a subset of $\lbrace 1,2,3 \rbrace$ but is not one of its elements. 
- **Stating that the set in 2(c) is correct syntax and is equal to $\lbrace -4, 4 \rbrace$**: This would be the case if the predicate $x^2 = 16$ were at the *end* of the set, so we'd have a set followed by a filter. But here the predicate is first, which as we discussed in the class meeting is incorrect. 


## Skill C4 (Monday March 25)

1. $\emptyset$
2. $\lbrace 1,2,3,4,5,6 \rbrace$
3. $\lbrace 5 \rbrace$
4. $\lbrace 7,8,9,10 \rbrace$ 
5. $\lbrace (5,6), (5,7), (5,8), (6,6), (6,7), (6,8) \rbrace$
6. 16 

### Common mistakes

- **Writing the first response as $\lbrace \emptyset \rbrace$:** The correct answer is $\emptyset$. This is not the same as $\lbrace \emptyset \rbrace$. Whereas $\emptyset$ has zero elements, the set $\lbrace \emptyset \rbrace$ has one element. *This is counted as a "simple" error".* 
- **Not giving the complement of the set in item 4:** Instead, giving a response that is identical to item 2. It says on the form that the superscript "c" means [complement](https://publish.obsidian.md/mth225/Sets+and+Functions/Complement). 
- **Using incorrect set notation in item 5:** The Cartesian product is a *set*, whose elements are *pairs* (or tuples). Some responses did not include the set braces on the outside but just gave a comma-separated list of tuples. Some responses gave the pairs as two-element sets, like $\lbrace 5, 6 \rbrace$ instead of $(5,6)$. Some did both; none of these is fully correct. You'll need set braces around the outside, and the elements of the set must be pairs, enclosed in parentheses not set braces. *This is counted as a "simple" error.*
- **Giving the full power set in item 6 instead of its cardinality:** The vertical bars around a set mean [cardinality](https://publish.obsidian.md/mth225/Sets+and+Functions/Cardinality). Having both the full power set and the cardinality is OK; but not having the cardinality is not OK. 


## Skill C5 (Wednesday March 27)

1. This is a sequence of choices so we will use the Multiplicative Principle (a.k.a. treating it like a license plate problem). There are 5 shirts to choose, then 3 pairs of pants, then 17 bowties so the total count is $5 \cdot 3 \cdot 17 = 255$. 
2. There are 20 integers in the set that are multiples of 5 (5, 10, 15, 20, ..., 95) and 14 that are multiples of 7 (7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98). There are two numbers -- 35 and 70 -- that are multiples of both 5 and 7. So by the Principle of Inclusion and Exclusion, the count we seek is $20 + 14 - 2 = 32$. (This can be checked fairly quickly by brute force, for example in Python run `len([n for n in range(1, 101) if n % 5 == 0 or n % 7 == 0])` or just write them all out. However a brute force solution is not considered a successful demonstration of the skill, because it does not use the counting concepts of the class.)

### Common mistakes

- **Not subtracting out the double-counted numbers in part 2:** That is, just adding $20+14$ and saying the answer is 34. Again this double counts any number that falls into both categories, of which there are two (35 and 70). 
- **A bunch of simple errors resulting from carelessness:** For example skipping numbers in the individual lists in part 2; or making arithmetic mistakes like $100/5 = 25$; or mis-copying numbers in the problem statement. You are allowed two simple errors without penalty but please be careful! 

## Skill C6 (Wednesday March 27)

1. (a) $6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720$. 

   (b) $\displaystyle{\binom{99}{96} = \frac{99!}{96! \cdot 3!} = \frac{99 \cdot 98 \cdot 97}{3 \cdot 2 \cdot 1} = 156849}$. 

2. This is a license plate problem where we pick the President first, the Vice President second, then the Treasurer. There are 6 choices for the first office, then 5 for the second, then 4 for the third: $6 \cdot 5 \cdot 4 = 120$. Or, recognize that this is a $3$-permutation and compute $\frac{6!}{3!} = 120$. 

### Common mistakes

- **Not knowing/misremembering the formula for the binomial coefficient:** [Memorize it!](https://publish.obsidian.md/mth225/Combinatorics/Binomial+coefficient) 
- **Having the right formula for the binomial coefficient but not simplifying the factorials:** If you try to compute $99!$, then $96!$, then $3!$ and plug the results into the formula, you will either get a calculator error because the numbers are so large, or an answer that is not an integer due to roundoff errors. Both are incorrect. 
- **Using the binomial coefficient to find the count in part 2:** The answer is not $\binom{6}{3}$ because this ignores the ordering of the selection. Sometimes this is appropriate, but not here, since it says in the problems statement that "committee positions have specific roles" so reordering a selection results in a truly different selection. (Imagine if Kamala Harris were president of the USA and Joe Biden were vice-president.)