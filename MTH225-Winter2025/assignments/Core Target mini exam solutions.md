# MTH 225 Core Learning Target Mini-Assessment solution guide 

## Learning Target 1

>(**CORE**) Given two integers $a$ and $b$, I can find the quotient and remainder when dividing $a$ by $b$, the greatest common divisor of $a$ and $b$ using the Euclidean Algorithm, and the value of `a % b`.

1. Use long division to find the quotient and remainder when dividing 88334 by 222.
2. Use the Euclidean Algorithm to find the greatest common divisor of 88334 and 222.
3. Find the value of the following: 
   - a. `88334 % 222`.
   - b. `222 % 88334`.
   - c. `222 % 222`.

**Answers:**

1. The quotient is 397 and the remainder is 200. To see the steps, use the long division calculator linked in earlier Learning Target exams. 
2. The greatest common divisor of 88334 and 222 is 2. Steps:
   - 88334 = 397 * 222 + 0
   - 222 = 111 * 2 + 0
   - 2 = 0 * 2 + 2
   - Therefore, the GCD is 2 since it is the last non-zero remainder.
3. 
   - a. `88334 % 222` = 200
   - b. `222 % 88334` = 222
   - c. `222 % 222` = 0


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: If $n$ is an even integer, then $n^2$ is an even integer.

1. State the hypothesis and conclusion of the implication.
2. State the converse of the implication.
3. State the contrapositive of the implication.
4. State the negation of the implication.

**Answers:**
1. The hypothesis is "n is an even integer" and the conclusion is " $n^2$ is an even integer".
2. The converse is "If $n^2$ is an even integer, then $n$ is an even integer".
3. The contrapositive is "If $n^2$ is not an even integer, then $n$ is not an even integer". (You can use "odd" in place of "not even" if you prefer.)
4. The negation is "The integer $n$ is even but $n^2$ is odd." 

### Notes

The only main note is that we are still getting submissions that get the basic form of these wrong, particularly the negation. **Just memorize the form!** Then put the hypothesis and conclusion in. 


## Learning Target 9

>(**CORE**) Given a statement to prove by mathematical induction, I can set up the framework for its proof.

Consider the statement: For all integers $n \geq 6$, $6n + 6 < 2^n$. 

Suppose we want to prove this statement by induction.

1. State the predicate involved in the proposition.
2. State the value of the variable that corresponds to the base case. 
3. Prove that the base case holds. 
4. State the inductive hypothesis. 
5. State the inductive step (what you would need to prove to complete the argument). Note, you do not need to provide a completed proof here. 

**Answers:**
1. The predicate is $P(n)$: $6n + 6 < 2^n$.
2. The base case is $n = 6$.
3. The base case holds because $6(6) + 6 = 42 < 64 = 2^6$.
4. Assume that $6k + 6 < 2^k$ is true for some integer $k$.
5. To complete the argument, we need to show that $6(k + 1) + 6 < 2^{k + 1}$.

**BONUS:** Here is a completed proof of the above statement, starting from the inductive step. Instead of a narrative, each step is numbered and justified.
1. We want to show that $6(k + 1) + 6 < 2^{k + 1}$. (Inductive step)
2. On the left, expanding gives $6k + 6 + 6 < 2^{k + 1}$. (Algebra)
3. Grouping the first two terms gives $(6k + 6) + 6$. (Algebra)
4. By the inductive hypothesis, we know that $6k + 6 < 2^k$. (Inductive hypothesis)
5. Therefore, we can replace $6k + 6$ with $2^k$ in the inequality. (Substitution)
6. Therefore $6k + 6 + 6 < 2^k + 6$. (Transitive property of inequalities)
7. We know that $2^k + 6 < 2^k + 2^k$ because $2^k > 6$ for all integers $k \geq 6$. (Algebra)
8. Therefore $2^k + 6 < 2^{k + 1}$. (Transitive property of inequalities)
9. Therefore $6(k + 1) + 6 < 2^{k + 1}$. (Transitive property of inequalities)
10. Therefore, by the principle of mathematical induction, $6n + 6 < 2^n$ for all integers $n \geq 6$. (Principle of mathematical induction)


### Notes

- Several submissions included the quantifier on the predicate and just said the predicate was the entire statement "For all integers $n \geq 6$, $6n + 6 < 2^n$. " This is incorrect because that statement is not a predicate: It is a predicate all of whose free variables have been quantified, so it's a proposition now. 
- Several submissions left off the word "Assume" in the inductive hypothesis -- this is the most important part of the inductive hypothesis! Remember that the inductive hypothesis is a complete sentence that communicates something to a reader. It's not just a math expression with no context. 


## Learning Target 11

>(**CORE**) I can find the union, intersection, Cartesian product, and difference of two sets; the complement of a set; and the cardinality of a finite set.

**Note**: We usually indicate the complement of a set $A$ by putting a bar over the $A$. However this notation doesn't render well online or in some of the publishing tools I am using. Therefore we will use $A^c$ to indicate the complement of $A$ from here on out. 

Consider the sets $A = \lbrace 2, 3, 4, 5 \rbrace$ and $B = \lbrace 1, 2, 3, 4, 5 \rbrace$, $C = \lbrace  6,7 \rbrace$ and the universal set $U = \lbrace 1, 2, 3, 4, 5, 6, 7, 8, 9 \rbrace$.

1. State $A \cup B$.
2. State $A \cap C$.
3. State $A \times C$.
4. State $A \setminus B$.
5. State $A^c$.
6. State $|U|$.

**Answers:**

1. $A \cup B = \lbrace 1, 2, 3, 4, 5 \rbrace$.
2. $A \cap C = \emptyset$.
3. $A \times C = \lbrace (2,6), (2,7), (3,6), (3,7), (4,6), (4,7), (5,6), (5,7) \rbrace$.
4. $A \setminus B = \emptyset$.
5. $A^c = \lbrace 1, 6, 7, 8, 9 \rbrace$.
6. $|U| = 9$.

### Notes

- Several submissions did not understand the notation for Cartesian product $A \times C$, or cardinality $|U|$. Please note that the Learning Target directly addresses your understanding of these concepts, so the first thing you might do if you are confused about that notation is get clear on it, using the course materials such as slides, videos, and vault. 
- Several submissions for part 4 found $A \setminus B = \lbrace 1 \rbrace$ instead of $\emptyset$. This is incorrect because $A \setminus B$ is by definition $A \setminus B = \lbrace x \in U \ | \ x \in A \text{and} x \not \in B \rbrace$. Since $1 \not \in A$ it is not in $A \setminus B$. 
- If you are reading this, email Prof. Talbert with the subject line "I read the solutions guide" (without the quotes) before 5:00pm on Wednesday, April 2. I am trying to understand who, if anybody, is reading these notes that I am putting a lot of effort into creating. Students sending an email with the correct subject line and before the deadline will receive 5 engagement credits. No, this is not an April Fools joke. 



## Learning Target 13

>(**CORE**) I can solve simple counting problems that involve a combination of the Additive Rule, Multiplicative Rule, and Principle of Inclusion/Exclusion.

Solve the following counting problems. Be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 

1. A company has 2215 employees. Each employee is to be given an ID number that consists of one letter followed by 3 digits. How many different ID numbers are possible?
2. How many three-letter "words" can be made from the 10 letters `FGHIJKLMNO` if repetition of letters is allowed?
3. How many bitstrings of length 8 either start with a `10` (on the left) or end in `1` (on the right)?

**Answers:**

1. The first letter can be any of 26 letters, and the three digits can be any of 10 digits. Therefore, the total number of ID numbers is $26 \cdot 10^3 = 26000$.
2. The first letter can be any of 10 letters, the second letter can be any of 10 letters, and the third letter can be any of 10 letters. Therefore, the total number of three-letter words is $10^3 = 1000$.
3. The number of bitstrings of length 8 that start with `10` is $2^6 = 64$ (the last 6 bits can be anything). The number of bitstrings of length 8 that end with `1` is $2^7 = 128$ (the first 7 bits can be anything). However, the bitstrings that start with `10` and end with `1` are counted twice, so we need to subtract those. The number of bitstrings that start with `10` and end with `1` is $2^5 = 32$. Therefore, the total number of bitstrings is $64 + 128 - 32 = 160$.

### Notes

- Several submissions in part 2 used the binomial coefficient $\binom{10}{3} = 120$. This is incorrect because $\binom{10}{3}$ is the number of 3-element subsets of the set $\lbrace F, G, H, I, J, K, L, M, N, O \rbrace$, but in those subsets repetition of letters is *not* allowed. (Repetition is never allowed in a set.) So for example the string `AAB` is not counted by $\binom{10}{3}$. However it states directly in the problem statement that repetition of letters here *is* allowed. So $\binom{10}{3}$ does not count any of the strings with repeated letters, therefore it is a significant under-count of the true number. 
- Many submissions for part 3 failed to realize that the Principle of Inclusion and Exclusion should be used. 

## Learning Target 14

>(**CORE**) I can compute a binomial coefficient and solve simple counting problems that involve combinations, permutations, or k-permutations.

1. Compute the exact values of each of the following: 
   - (a) $\binom{8}{3}$
   - (b) $\binom{10}{5}$
   - (c) $\binom{15}{7}$
2. How many 3-element subsets containing the letter A can be formed from the set $\lbrace{A,B,C,D,E,F,G}\rbrace$? 
3. How many bitstrings of length 8 contain exactly six `0`s?

**Answers:**

1. 
   - (a) $\binom{8}{3} = \frac{8!}{3!(8-3)!} = \frac{8!}{3!5!} = \frac{8 \cdot 7 \cdot 6}{3 \cdot 2 \cdot 1} = 56$.
   - (b) $\binom{10}{5} = \frac{10!}{5!(10-5)!} = \frac{10!}{5!5!} = \frac{10 \cdot 9 \cdot 8 \cdot 7 \cdot 6}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = 252$.
   - (c) $\binom{15}{7} = \frac{15!}{7!(15-7)!} = \frac{15!}{7!8!} = 6435$.
2. Choosing a 3-element subset from $\lbrace{A,B,C,D,E,F,G}\rbrace$ that must include the letter A, is the same process as choosing a 2-element subset from the 6-element set $\lbrace{B,C,D,E,F,G}\rbrace$. And the number of 2-element subsets of a 6-element set is, by definition,  $\binom{6}{2} = \frac{6!}{2!(6-2)!} = \frac{6!}{2!4!} = \frac{6 \cdot 5}{2 \cdot 1} = 15$.
3. The number of bitstrings of length 8 that contain exactly six `0`s is the same as the number of bitstrings of length 8 that have exactly 2 `1` bits. And that number is, by definition, $\binom{8}{2} = \frac{8!}{2!(8-2)!} = \frac{8!}{2!6!} = \frac{8 \cdot 7}{2 \cdot 1} = 28$.

### Notes

- Several submissions had answers for binomial coefficients but no work was shown (as above). To get a *Master* rating, you must at least show how you apply the closed formula for the specific binomial coefficient you are computing. The minimal work needed would be something like this:  $\binom{8}{3} = \frac{8!}{3!(8-3)!} = 56$. But without showing the closed formula and how you're applying it, there is nothing to verify that you didn't simply use a button on a calculator, and so there's not enough evidence to support your mastery of the Learning Target. 
- Several submissions used an incorrect formula, usually by dividing by only one factorial, such as:  $\binom{8}{3} = \frac{8!}{3!}$ 
- Many submissions used $\binom{7}{3}$ in part 2 instead of $\binom{6}{2}$. The number $\binom{7}{3}$ is incorrect because this counts the number of 3-element subsets of a 7-element set, but this would include sets without the letter A in them. Remember: **Don't throw formulas at things.** 