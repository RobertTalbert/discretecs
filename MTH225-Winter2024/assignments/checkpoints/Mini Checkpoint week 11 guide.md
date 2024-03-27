# Mini-Checkpoints from Week 11

Click below for the Mini Checkpoints: 
- [C3 and C4](https://docs.google.com/document/d/1os1cKeSy091qydib4d9XhU5zBFOBXThsTKnPfZrzl-Q/edit?usp=sharing)
- [C5 and C6](https://drive.google.com/file/d/1fzGn8x4pNvaBFf9mrcKXr8BJ77pf0RjZ/view?usp=sharing)
- C1 and C2

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
2. There are 20 integers in the set that are multiples of 5 (5, 10, 15, 20, ..., 95) and 14 that are multiples of 7 (7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98). There are two numbers -- 35 and 70 -- that are multiples of both 5 and 7. So by the Principle of Inclusion and Exclusion, the count we seek is $20 + 14 - 2 = 32$. (This can be checked fairly quickly by brute force, for example in Python run `print([n for n in range(1, 101) if n % 5 == 0 or n % 7 == 0])`.)

## Skill C6 (Wednesday March 27)

1. (a) $6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720$. 

   (b) $\displaystyle{\binom{99}{96} = \frac{99!}{96! \cdot 3!} = \frac{99 \cdot 98 \cdot 97}{3 \cdot 2 \cdot 1} = 156849}$. 

2. This is a license plate problem where we pick the President first, the Vice President second, then the Treasurer. There are 6 choices for the first office, then 5 for the second, then 4 for the third: $6 \cdot 5 \cdot 4 = 120$. Or, recognize that this is a $3$-permutation and compute $\frac{6!}{3!} = 120$. 

## Skill C1 (Friday March 29)

## Skill C2 (Friday March 29)