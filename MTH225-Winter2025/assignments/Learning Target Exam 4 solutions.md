# MTH 225: Learning Target Exam 4 -- Solutions Guide 

## NOTES ON THIS GUIDE

**Answers for Learning Targets 1, 2, 3 and 5 are not given in this guide** because they can be checked using a technological tool. Please consult [the "How To Practice" guide](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/How%20to%20practice.md) for links to those tools. 

## Overall common mistakes


---


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: *If $p$ is a prime number, then $p$ is odd.*

1. State the hypothesis and conclusion of the implication.
2. State the converse of the implication.
3. State the contrapositive of the implication.
4. State the negation of the implication.

**Answers:**

1. 
   - Hypothesis: $p$ is a prime number. 
   - Conclusion: $p$ is odd.
2. Converse: If $p$ is odd, then $p$ is a prime number.
3. Contrapositive: If $p$ is not odd, then $p$ is not a prime number.
4. Negation: $p$ is a prime number and $p$ is not odd. 

You can say "even" instead of "not odd" if you want, but it is not necessary.

### Notes

- Some submissions did not list the hypothesis and conclusion separately, but instead just listed the implication. Or, the listed the hypothesis and conclusion joined with "and" ($p$ is a prime number and $p$ is odd). This is not correct because the work has to clearly show the difference between the hypothesis and conclusion. Joining the two with a connective creates a new, third statement. 
- Some submissions are still listing that the negation is another conditional statement, such "If $p$ is a prime number, then $p$ is not odd." This is incorrect. The negation of a conditional statement is a conjunction of the hypothesis and the negation of the conclusion.
- Some submissions for the negation were ambiguous or ill-formed sentences. Example: *If $p$ is a prime number and $p$ is not odd.*" This is not a complete sentence and it is not clear what the statement means. The negation must be a complete sentence that is clearly a conjunction and not an implication. 
- 
## Learning Target 6

>Given a predicate, I can state the free variable(s); determine whether quantified forms are true or false; and state its negation.


1. For each quantified predicate below, state whether it is True or whether it is false. The domain of each predicate is $\mathbb{N} = \lbrace 0, 1, 2, 3, \dots \rbrace$. 
   - a. $\forall n, n^2 < n$
   - b. $\exists n, n^2 \leq n$
2. State the free variable(s) in each predicate. If there are no free variables, say so. 
   - a. $\exists n, n^2 \leq n$
   - b. $\exists x \exists y, x + y + z= 0$
   - c. $\forall y, x + y = 0$
3. State the negation of the statement: *Some prime numbers are even.*  Phrase the result in clear English and do not just put the word "not" or "it is not the case that" in front of the

**Answers:**

1. 
   - a. False. (For example, $n = 2$ does not obey this inequality.) 
   - b. True. For example, $n = 1$ works.
2. 
   - a. No free variables. 
   - b. Free variable: $z$ 
   - c. Free variable: $x$. 
3. All prime numbers are odd. (Other correct statements are possible.)


### Notes

- Several submissions did not include part 3, the negation. It appears on the next page from the first parts. It's possible that the students missed the page turn. Please remember to check for awkward page turns and other formatting items. 

## Learning Target 7

>I can determine whether a sequence of statements is a valid rule of deduction and determine if two statements are logically equivalent. 

1. Use a truth table to determine if the argument with premises $p \rightarrow r$ and $q \rightarrow r$, and conclusion $p \rightarrow q$ forms a valid rule of deduction.
2. Use a truth table to determine if the propositions $p \land q$ and $(\neg p) \land (\neg q)$ are logically equivalent.

**Answers:**

1. The truth table for the argument is as follows:

| $p$ | $q$ | $r$ | $p \rightarrow r$ | $q \rightarrow r$ | $p \rightarrow q$ |
|-----|-----|-----|-------------------|-------------------|-------------------|
| T   | T   | T   | T                 | T                 | T                 |
| T   | T   | F   | F                 | F                 | T                 |
| T   | F   | T   | T                 | T                 | F                 |
| T   | F   | F   | F                 | T                 | F                 |
| F   | T   | T   | T                 | T                 | T                 |
| F   | T   | F   | T                 | F                 | T                 |
| F   | F   | T   | T                 | T                 | T                 |
| F   | F   | F   | T                 | T                 | T                 |

As shown in row 3 (where $p$ is true, $q$ is false, and $r$ is true), both premises are true but the conclusion is false, proving that this is not a valid rule of deduction.

1. The truth table for the propositions is as follows:

I'll create a truth table to determine if the propositions $p \land q$ and $(\neg p) \land (\neg q)$ are logically equivalent.

Two propositions are logically equivalent if they have the same truth value in all possible cases.

| $p$ | $q$ | $p \land q$ | $\neg p$ | $\neg q$ | $(\neg p) \land (\neg q)$ |
|-----|-----|-------------|----------|----------|---------------------------|
| T   | T   | T           | F        | F        | F                         |
| T   | F   | F           | F        | T        | F                         |
| F   | T   | F           | T        | F        | F                         |
| F   | F   | F           | T        | T        | T                         |


Since the two propositions have different truth values in some cases, they are not logically equivalent.

## Learning Target 8

>Given a recurrence relation for a sequence or other structure, I can find several instances of the sequence or structure.

**Note**: The recurrence relations here use subscripts instead of function notation. So, $a_n$ means $a(n)$, $a_{n-1}$ means $a(n-1)$, and so on. 

1. Consider the recurrence relation $a_n = a_{n-1} + 2a_{n-2}$ with initial conditions $a_0 = 5$ and $a_1 = 3$. Find the first six terms of the sequence.
2. Consider the recurrence relation $a_n = a_{n-1} + n^2$ with initial condition $a_0 = 1$. Find the first five terms of the sequence.
3. Consider the following set defined recursively: The numbers $2$ and $3$ are elements of the set, and if $a$ is an element of the set then $2a$ is also an element of the set. List at least five elements of the set.

**Answers:**

1. 
   - $a_0 = 5$
   - $a_1 = 3$
   - $a_2 = a_1 + 2a_0 = 3 + 2(5) = 13$
   - $a_3 = a_2 + 2a_1 = 13 + 2(3) = 19$
   - $a_4 = a_3 + 2a_2 = 19 + 2(13) = 45$
   - $a_5 = a_4 + 2a_3 = 45 + 2(19) = 83$
   - So the first six terms are: $5, 3, 13, 19, 45, 83$.
2. 
   - $a_0 = 1$
   - $a_1 = a_0 + 1^2 = 1 + 1 = 2$
   - $a_2 = a_1 + 2^2 = 2 + 4 = 6$
   - $a_3 = a_2 + 3^2 = 6 + 9 = 15$
   - $a_4 = a_3 + 4^2 = 15 + 16 = 31$
   - So the first five terms are: $1, 2, 6, 15, 31$.
3. You can double the 2 multiple times to get 2, 4, 6, 8, 10,... Or double the 3 to get 3, 6, 12, 24, 48,... Or you can mix and match to get 2, 3, 4, 6, 8, 9, 12, 18, 24,...


## Learning Target 9

>(**CORE**) Given a statement to prove by mathematical induction, I can set up the framework for its proof.

*For all positive integers $n$, $3^n - 1$ is even*. Suppose we want to prove this statement by induction.

Suppose we want to prove this statement by induction.

1. State the predicate involved in the proposition.
2. State the value of the variable that corresponds to the base case. 
3. Prove that the base case holds. 
4. State the inductive hypothesis. 
5. State the inductive step (what you would need to prove to complete the argument). Note, you do not need to provide a completed proof here. 

**Answers:**

1. The predicate is $P(n)$: $3^n - 1$ is even.
2. The base case is $n = 1$.
3. When $n=1$, note $3^1 - 1 = 2$ is even. So the base case holds. 
4. Assume that for some positive integer $k$, $3^k - 1$ is even.
5. To complete the argument, we need to show that $3^{k+1} - 1$ is even. 

**BONUS:** Here is a completed proof. This was not necessary in the problem, it's only included here for learning purposes. 

**Proof by induction.** The base case is $n=1$. In this case $3^1 - 1 = 2$, which is even.
Assume that for some positive integer $k$, $3^k - 1$ is even. This means that there exists an integer $m$ such that $3^k - 1 = 2m$. This implies that $3^k = 2m+1$. We want to show that $3^{k+1} - 1$ is even.
We have:
$$3^{k+1} - 1 = 3 \cdot 3^k - 1 = 3(3^k) - 1 = 3(2m + 1) - 1 = 6m + 2 = 2(3m + 1).$$
Thus $3^{k+1} - 1$ is even, and we have shown that if $P(k)$ is true, then $P(k+1)$ is true. By the principle of mathematical induction, $P(n)$ is true for all positive integers $n$.

### Notes

- Several submissions left off the important phrase "is even" from the predicate, inductice hypothesis, and inductive step. Note that just the expression $3^n - 1$ is not a predicate. A predicate is a statement that can be true or false depending on the value of the variable. The statement $3^n - 1$ is not a statement that can be true or false, it is just an expression. Similarly, in the inductive hypothesis, the statement "for some positive integer $k$, $3^k - 1$" does not make sense because we cannot "assume $3^k - 1$". We have to assume that something is *true about* $3^k - 1$, namely that it is even. 
- Some submissions had an incorrect base case, commonly $n=0$. This is not the base case because the proposition is claimed to be true "for all positive integers", and $0$ is not a positive integer.

## Learning Target 10

>Given a set in roster notation, I can rewrite it in set-builder notation and vice versa, and I can determine its elements and subsets.
 

1. Below are several statements about sets and elements. Label each one as **TRUE** or **FALSE**. 

   a) $5 \in \emptyset$

   b) $\{6,7,8\} \subseteq \{5,7,9\}$

   c) $\frac{1}{2} \in \mathbb{Z}$ 

   d) $\mathbb{Z} \subseteq \mathbb{N}$ 

   e) $\emptyset \subseteq \{1,2,3,4,5\}$

   

2. Here are three sets written in set-builder notation. For each, if the set is written using correct set syntax, rewrite it using roster notation. If the set is written using incorrect syntax, write **INCORRECT SYNTAX**. 

   a) $\lbrace n \in \mathbb{N} \, : \, n \, \% \, 3 = 1 \rbrace$

   b) $\lbrace n \in \mathbb{N} \, : \, 2^n \rbrace$ 

   c) $\lbrace  x \, \% \, 3 \, : \, x\in \lbrace 1,2,3,\dots 10 \rbrace \rbrace$


**Answers:** 

1. (Explanations are not necessary; they're just here to help you understand the answers.)
   - a) FALSE. The empty set has no elements, so $5$ cannot be in it. 
   - b) FALSE. The set $\{6,7,8\}$ is not a subset of $\{5,7,9\}$ because $6$ and $8$ are not in the second set. 
   - c) FALSE. The set of integers $\mathbb{Z}$ contains whole numbers, but not fractions like $\frac{1}{2}$. 
   - d) FALSE. The set of integers $\mathbb{Z}$ contains negative numbers and zero, while the set of natural numbers $\mathbb{N}$ only contains positive whole numbers. 
   - e) TRUE. The empty set is a subset of every set.

2. 
   - a) $\lbrace 1, 4, 7, 10, \dots \rbrace$ (This is the set of all natural numbers that are congruent to $1$ modulo $3$.)
   - b) INCORRECT SYNTAX. The expressio following the vertical bar is not a predicate, it's a formula. 
   - c) $\lbrace 1, 2, 0 \rbrace$ (This is mapping the "mod 3" function onto the given set. Notice, we do not repeat anything in a set, so \lbrace 1, 2, 0, 1, 2, 0, 1, 2, 0, 1, 2, 0 \rbrace$ is incorrect.)

## Learning Target 11

>(**CORE**) I can find the union, intersection, Cartesian product, and difference of two sets; the complement of a set; and the cardinality of a finite set.

**Note**: We usually indicate the complement of a set $A$ by putting a bar over the $A$. However this notation doesn't render well online or in some of the publishing tools I am using. Therefore we will use $A^c$ to indicate the complement of $A$ from here on out. 

Consider the sets $A = \lbrace 1, 2, 3 \rbrace$ and $B = \lbrace 2, 3, 4 \rbrace$, $C = \lbrace  6,7,8 \rbrace$ and the universal set $U = \lbrace 1, 2, 3, 4, 5 \rbrace$.


## Learning Target 12

>I can determine if a mapping between two sets is a function; if it is, I can determine if it is injective, surjective, and/or bijective.

Below are six mappings between sets, numbered 1 through 6. For each mapping, state if it is a function, and if it is a function, also state if it is injective, surjective, and/or bijective or none of these. 

<img src = "lt12-exam3.png" height = 250></img>

**Answers:**

1. This is a function. It is neither injective nor surjective. 
2. This is a function. It is injective but not surjective.
3. This is not a function (3 maps to two outputs). 
4. This is a function. It is surjective but not injective.
5. This is a function. It is bijective.
6. This is not a function (8 maps to two outputs). 


## Learning Target 13

>(**CORE**) I can solve simple counting problems that involve a combination of the Additive Rule, Multiplicative Rule, and Principle of Inclusion/Exclusion.

Solve the following counting problems. Be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 

## Learning Target 14

## Learning Target 15

