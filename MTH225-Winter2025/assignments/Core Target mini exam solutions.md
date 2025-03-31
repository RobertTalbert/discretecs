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
2. The number of 3-element subsets containing the letter A is $\binom{6}{2} = \frac{6!}{2!(6-2)!} = \frac{6!}{2!4!} = \frac{6 \cdot 5}{2 \cdot 1} = 15$.
3. The number of bitstrings of length 8 that contain exactly six `0`s is $\binom{8}{6} = \binom{8}{2} = \frac{8!}{2!(8-2)!} = \frac{8!}{2!6!} = \frac{8 \cdot 7}{2 \cdot 1} = 28$.