# MTH 225 Learning Target Exam 3 answers and notes 

## Learning Target 2

1. $555$
2. $86$
3. $1373$
4. `1000011`

### Notes 

- Remember that when converting from a non-decimal base to base 10, this just uses place value. And make sure to get the right place value. Converting from base 10 to a non-decimal base requires the base conversion algorithm, and you must show every step of that algorithm anywhere it's asked of you. 

---


## Learning Target 5

1. 
| p | q | ¬q | p ∧ q | (¬q) → (p ∧ q) |
|---|---|----|-------|----------------|
| T | T | F  | T     | T              |
| T | F | T  | F     | F              |
| F | T | F  | F     | T              |
| F | F | T  | F     | F              |

2. 
| p | q | r | p ∨ q | p ∨ r | (p ∨ q) ∧ (p ∨ r) |
|---|---|---|-------|-------|-------------------|
| T | T | T | T     | T     | T                 |
| T | T | F | T     | T     | T                 |
| T | F | T | T     | T     | T                 |
| T | F | F | T     | T     | T                 |
| F | T | T | T     | T     | T                 |
| F | T | F | T     | F     | F                 |
| F | F | T | F     | T     | F                 |
| F | F | F | F     | F     | F                 |



3. 
| p | q | ¬q | p → q | ¬(p → q) | p ∧ (¬q) |
|---|---|----|-------|----------|----------|
| T | T | F  | T     | F        | F        |
| T | F | T  | F     | T        | T        |
| F | T | F  | T     | F        | F        |
| F | F | T  | T     | F        | F        |

Based on the last two columns we see that the two statements are logically equivalent. 


### Notes

- A number of submissions lacked intermediate columns. For example, in the first question, not giving a column for p ∧ q. You must show all intermediate columns that are used for a truth table or it will be downgraded to Proficient. 
- A number of submissions attempted to put all three parts into the same truth table with eight rows. [On Learning Target Exam 2, this happened as well, and I created a rule](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2026/assignments/MTH%20225%20W26%20Learning%20Target%20Exam%202%20solutions.md#notes-2) that said if you use more rows in a truth table than are necessary, it will be immediately downgraded to proficient. Parts 1 and 3 do not require eight rows. They only require four. If you used eight, this resulted in downgrading. 
- The third item is exactly the same one that was given on the last learning target exam. And as on that exam, The third item is exactly the same one that was given on the last learning target exam. And as on that exam, A large number of submissions said that the two statements in part 3, are not logically equivalent, even though we have stressed many times in class that the negation of "if P then Q" is "P and not Q" And this very question about logical equivalence was a major class exercise.

---


## Learning Target 9

1. The value of the variable for the base case is $n=0$. In this case, we have $4^0 - 1$ which equals $1-1$ or $0$. The integer $3$ divides $0$ because `0 % 3 = 0`. So the base case holds. 
2. Assume that for some $k$, $3$ divides $4^k - 1$. 
3. Prove that $3$ divides $4^{k+1} - 1$. 




## Learning Target 10 

1. This is a situation where we are selecting one object from disjoint bins, so we use the Additive Principle. The count is $4 + 7 + 3 = 14$. 
2. This is literally a license plate problem. There are $26$ letter choices for the first letter, then $25$ for the second one, then $24$ for the third, followed by $10$ choices for each of the digits. So the count is $26 \cdot 25 \cdot 24 \cdot 10^3 = 15,600,000$. 
3. The number of integers in this range divisible by $3$ is $33$ and the number divisible by $5$ is $20$. There are $6$ integers in this range that are divisible by both $3$ and $5$ (that is, divisible by $15$). So we need to use the Principle of Inclusion and Exclusion, and the count is $33 + 20 - 6 = 47$. 

### Notes

- A number of submissions used multiplication instead of addition in part one, but we are not making a sequence of choices. We're making one choice as is stated in the problem parameters. 
- A number of solutions for number two set up a license plate problem, but added the letter choices to the digit choices, for example $26 \cdot 25 \cdot 24 + 10 \cdot 10 \cdot 10$. There is no justification for adding these two groups of numbers since we are engaged in a sequence of six choices, not two sequences of three choices. 
- A number of solutions not take into account that the letters cannot be repeated. And so we ended up with $26^3 \cdot 10^3$. 
- Number of solutions failed to account for numbers that are divisible by both 3 and 5 and didn't subtract off a 6. You must use the Principle of Inclusion and Exclusion here because of the overlap between the criteria that you're counting. 

---

## Learning Target 11

1. $\binom{12}{9} = \frac{12!}{9! 3!} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220$. 
2. Order doesn't count when forming a committee, so the count is $\binom{20}{5} = 15504$. 
3. All the letters in the word are distinct, so the count is $8! = 40320$. 
4. It's best to think of this as a license plate problem. We have three slots to fill and no repetitions (since once we select a letter, it can't be selected again). This gives $8$ choices for the first character, $7$ for the second, and $6$ for the third giving a count of $8 \cdot 7 \cdot 6 = 336$. This is the same as $P(8,3)$. 

NOTE: In part 4 the problem uses the term "substring" to refer to strings made by selecting letters from a larger string. This is not what this word typically means, however -- a "substring" is a chunk of contiguous characters taken from the main string, so neither `OER` nor `ETR` in that way would be considered as "substrings" of `COMPUTER`. Grading will proceed by looking at your work on a case-by-case basis, especially looking for the main idea: No repetition is allowed, and order matters (because however you look at it, `OER` and `EOR` woud be considered different strings, hence order matters.) 

### Notes

- A number of solutions did not use a correct formula for the binomial coefficient in either part one or part two, often by leaving off a factorial on the bottom of the fraction. (For example, saying $\binom{12}{9} = \frac{12!}{9!}$.)
- Some solutions used a correct formula for part one, but an incorrect formula for the binomial coefficient on part two, or vice versa. It is the same binomial coefficient, so you'll want to use the same formula. 
- In the fourth problem, a number of solutions simply used the binomial coefficient formula on the problem, but didn't take into account that ordering of strings counts. If you reorder a string, it is a different string, and each reordering must be counted separately. 

## Learning Target 12 

1. Geometric. Closed formula: $a(n) = 3 \cdot 2^n$. Recurrence relation: $a(0) = 3$ and $a(n) = 2 \cdot a(n-1)$ for $n > 0$. 
2. Aritmetic. Closed formula: $a(n) = 3n+3$. Recurrence relation: $a(0) = 3$ and $a(n) = 3+ a(n-1)$ for $n > 0$.  
3. Neither. 
4. Arithmetic. Closed formula: $a(n) = 3 - 2n$. Recurrence relation: $a(0) = 3$ and $a(n) = a(n-1) - 2$ for $n > 0$. 