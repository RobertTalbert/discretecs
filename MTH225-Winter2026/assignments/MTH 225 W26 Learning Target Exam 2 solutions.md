# MTH 225 Learning Target Exam 2 Solution Guide 


## Learning Target 1

1. Quotient = 205. Remainder = 45. 
2. .
   (a) $45$ (this can be read directly from part 1)

   (b) $4$ (because `% 10` always returns the ones digit of the input)

   (c) $0$ (because the input is clearly divisible by 5)

3. The positive numbers that work are $3, 12, 21, 30, 39, 48, \dots$. The negative ones are $-6, -15, -24, -33, -42, \dots$. Any five of these that include at least one of the negatives is a correct list. 


## Learning Target 2

1. 302
2. 205
3. `2FB`
4. `1011110`

### Notes

- A number of submissions were using the base conversion algorithm on parts 1 and 2 to go to base 10. That is incorrect. The base conversion algorithm is used to go **from** base 10 **to** another base, not vice versa. 
- A number of submissions skipped the final step of part 4 and did not do an important last round of division, that results in the leftmost bit (`1`), ending up with an answer of `011110`. Remember always to reality check your work. If you arrive at an answer of `11110` when converting 94 to binary, it should strike you that that binary string is much too small. This is only a five bit string and so the resulting base 10 integer would have to be less than $2^6$ which is 64, so you can tell by looking that there's no way that could be right. 

## Learning Target 3

**Reminder:** Learning Target 3 no longer appears on these solution guides because you should check your work with [a binary calculator](https://www.calculator.net/binary-calculator.html).

## Learning Target 4

1. Hypothesis: We are on break next week. Conclusion: There are no office hours. 
2. If there are no office hours, then we are on break next week. 
3. If there are office hours, then we are not on break next week. 
4. We are on break next week and there are office hours.

### Notes

- The word "If" *should not* be included with the hypothesis. Doing so causes problems later when forming the converse, contrapositive, and negation. 
- The converse is not simply moving the if part to the end of a sentence like this: **"There are no office hours, if we are on break next week."** This is the same statement as the original proposition, and the logic of cause and effect has not changed. Instead of simply relocating a phrase to the end of a sentence, you must replace the hypothesis with the conclusion and the conclusion with the hypothesis. 
- A number of submissions for the negation used a comma where the word "and" is, like this: **"We are on break next week, there are office hours"** This is, first of all, incorrectly formed English. Secondly, the comma is ambiguous. It could be taken to mean "and", but it could also be taken to mean "therefore", or "because", or any of a number of logical connectives that change the underlying logic of the statement. The word "and" (or the word "but") must be used and there are no substitutes for this. 

## Learning Target 5

Part 1: 

| p | q | ¬q | p → (¬q) |
|---|---|----|----------|
| T | T | F  | F        |
| T | F | T  | T        |
| F | T | F  | T        |
| F | F | T  | T        |

Part 2: 

| p | q | r | p ∨ q | ¬r | (p ∨ q) → ¬r |
|---|---|---|-------|----|---------------|
| T | T | T | T     | F  | F             |
| T | T | F | T     | T  | T             |
| T | F | T | T     | F  | F             |
| T | F | F | T     | T  | T             |
| F | T | T | T     | F  | F             |
| F | T | F | T     | T  | T             |
| F | F | T | F     | F  | T             |
| F | F | F | F     | T  | T             |


Part 3 (combined truth table for both propositions): 

| p | q | ¬q | p → q | ¬(p → q) | p ∧ (¬q) |
|---|---|----|-------|----------|----------|
| T | T | F  | T     | F        | F        |
| T | F | T  | F     | T        | T        |
| F | T | F  | T     | F        | F        |
| F | F | T  | T     | F        | F        |

We can see from the final result columns that the propositions $\neg (p \rightarrow q)$ and $p \wedge (\neg q)$ are logically equivalent. 

### Notes

- **Please use only the number of rows that are needed for a propositions truth table.** A number of submissions attempted to put all the truth tables together into a single large truth table with eight rows, even though the propositions in parts 1 and 3 only require four rows (since there are only two variables). This can be done correctly, but it caused a number of mistakes that ended up downgrading students because you have too many rows to keep track of. In the future, this will result in an immediate downgrade to *Proficient* or lower, even if the entries in the truth table are correct.  
- Don't cut corners on showing your work. A number of submissions, in addition to trying to do all four propositions in the same truth table were taking shortcuts: not labeling columns, not taking care to line up the entires in the row (so for example there were some columns with 8 entries and some with 10, in the same table), and so on. Remember your job on a learning target exam is to give me clear evidence of mastery. The more you obscure the evidence by making it hard to read, the less convincing the work. 
- **Remember to reality check your work**. A large number of submissions said that the two statements in part 3, $\neg (p \rightarrow q)$ and $p \wedge (\neg q)$, are not logically equivalent, even though we have stressed many times in class that the negation of "if P then Q" is "P and not Q" And this very question about logical equivalence was a major class exercise.  
- A number of submissions gave a correct truth table in part 3 but did not state whether the propositions are logically equivalent or not. The purpose of part 3 is to see if you can apply truth tables to deciding whether propositions are logically equivalent or not. So if you had a correct truth table but no answer about logical equivalence, it's not *Master* level work yet. 
- Remember too that when you're making a truth table, you must give all intermediate columns used in constructing the final result, or else I have no ability to see your thought processes. If you have a correct final result column, but lacking intermediate columns, it's downgraded from *Master*. 


## Learning Target 6

1. Please note I'm providing explanations here for learning purposes, but only the true/false answers were required on your exam. 

   (a) False (nothing is in the empty set)

   (b) False (for example $-1 \in \mathbb{Z}$ but not in $\mathbb{N}$)

   (c) True (sets do not respect ordering)

   (d) True ([the empty set is a subset of every set](https://publish.obsidian.md/discretecs/Sets+and+Functions/Subset))

   (e) False (1 is in the first set but not the second)

2. ,
   (a) $\lbrace -3, -2, -1, 0, 1, 2, 3 \rbrace$ (It's the set of all integers whose square is less than 10)

   (b) $\lbrace 0, 2, 4 \rbrace\$ 

### Notes 

- A number of submissions did not use set braces around the answers to part 2. They must be in set braces $\lbrace \rbrace$. Results that were given with no delimiters at all (for example, just "0, 2, 4" in 2b) resulted in a downgrade from *Master*. Those that did use a delimiter but not set braces (for example, [0,2,4] or (0,2,4) in part 2b)) were considered an error but if it was the only error in the entire problem (including part 1) then you were not downgraded. 

## Learning Target 7

1. 
   (a) $\lbrace 1,2,3,4,5,6,7 \rbrace$

   (b) $\lbrace 3,4,5 \rbrace$

   (c) $\lbrace 1, 2 \rbrace$

   (d) $\lbrace 6,7 \rbrace$

2. $\lbrace (a,1), (a,2), (a,3), (b,1), (b,2), (b,3) \rbrace$

3. $\emptyset$, $\lbrace x \rbrace$, $\lbrace y \rbrace$, $\lbrace x,y \rbrace$

### Notes

- In part 2, **the elements of the Cartesian product must be given as tuples in proper notation**. That is, they must be **ordered pairs** with the elements of the pair **separated by a comma and enclosed in parentheses**.  [As noted in the Standards for Student Work document](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2026/course-documents/MTH%20225%20Standards%20for%20Student%20Work%20Winter%202026.md#learning-targets), and as discussed in class, this is a requirement. Below are some of the ways that this can be done incorrectly, resulting   in a downgrade from *Master*: 
  - Using no notation at all to indicate the elements, for example $a1$ instead of $(a,1)$
  - Using parentheses but no comma separation, for example $(a1)$ instead of $(a,1)$
  - Using set brackets instead of parentheses, for example $\lbrace a,1 \rbrace$ instead of $(a,1)$ 
- Similarly, in part 3, listing the elements of the power set as tuples and not sets, for example $(x,y)$ instead of $\lbrace x,y \rbrace$ resulted in a downgrade. When working with sets, you must use the correct notation at all times, and that includes the delimiters.
- Listing $\lbrace \emptyset \rbrace$ as an element of $\cal{P}(S)$ instead of $\emptyset$ is an error. These are not the same and $\lbrace \emptyset \rbrace$ is not an element of $\cal{P}(S)$. This error was noted but did not result in a downgrade as long as it was the only error in the problem. 


## Learning Target 8

1. Neither (not surjective, because nothing maps to $h$; not injective because both 3 and 6 map to $u$)
2. Injective, but not surjective (because hothing maps to either $k$ or $w$)
3. Not a function (3 has two outputs) 
4. Surjective, but not injective (because $p$, $z$, and $y$ all map to 5)
5. Both (that is, it's bijective)
6. Not a function (8 has two outputs) 

### Notes

- I relaxed the standard on this one so that 5/6 correct earns *Master*. 
