# MTH 225: Learning Target Exam 3

## Instructions

- The formatting of this one is different: Put **each** Learning Target you do on a **separate page** with your name at the top. There is no space provided on this form for your work. **Do not put more than one Learning Target on a single page.** Turn all of your pages in at the end. 
- As always: **Do not attempt any Learning Target on which you already have a rating of *Master*.** 
- As always: **You must show your work and explain your reasoning clearly and in complete sentences in order to earn a rating of *Master* unless the problem clearly says otherwise** -- for example if it asks you merely to "State" something. 

---

## Learning Target 1

>(**CORE**) Given two integers $a$ and $b$, I can find the quotient and remainder when dividing $a$ by $b$, the greatest common divisor of $a$ and $b$ using the Euclidean Algorithm, and the value of `a % b`.

1. Use long division to find the quotient and remainder when dividing 44667 by 123.
2. Use the Euclidean Algorithm to find the greatest common divisor of 44667 and 123.
3. Find the value of the following: 
   - a. `44667 % 123`.
   - b. `123 % 44667`.
   - c. `44667 % 44667`.



## Learning Target 2

>I can convert a positive integer between bases 2, 8, 10, and 16; and I can represent a negative integer in binary using twos complement.

1. Convert the decimal (base 10) number 44667 to hexadecimal using the base conversion algorithm. 
2. Convert the binary number 10110111 to decimal (base 10). 
3. Convert the octal number 127 to decimal (base 10).



## Learning Target 3

>I can perform arithmetic operations on binary numbers. 

1. Compute the sum of the binary numbers 10110111 and 11001100.
2. Compute the difference of the binary numbers 11110111 and 10001100.
3. Compute the product of the binary numbers 1011 and 11.
4. Compute the quotient of the binary numbers 10111 and 11.


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: *If $n$ is an odd integer, then $n^2$ is an odd integer.*

1. State the hypothesis and conclusion of the implication.
2. State the converse of the implication.
3. State the contrapositive of the implication.
4. State the negation of the implication.


## Learning Target 5

>I can write the truth table for a statement containing two or three variables.

Write the truth tables for the following statements. Be sure to include all intermediate columns. 

1. $(p \land q) \lor r$
2. $(p \lor q) \land r$
3. $p \rightarrow (q \land r)$

## Learning Target 6

>Given a predicate, I can state the free variable(s); determine whether quantified forms are true or false; and state its negation.

1. For each quantified predicate below, state whether it is True or whether it is false. The domain of each predicate is $\mathbb{N} = \lbrace 0, 1, 2, 3, \dots \rbrace$. 
   - a. $\forall n, n^2 \geq n$
   - b. $\exists n, n^2 = 2n$
2. State the free variable(s) in each predicate. If there are no free variables, say so. 
   - a. $\forall n, n^2 \geq n$
   - b. $\exists x \exists y, x + y = 0$
   - c. $\forall x, x + y = 0$
3. State the negation of the statement: *Every natural number is either even or odd.* Phrase the result in clear English and do not just put the word "not" or "it is not the case that" in front of the original statement. 



## Learning Target 7

>I can determine whether a sequence of statements is a valid rule of deduction and determine if two statements are logically equivalent. 

1. Use a truth table to determine if the argument with premises $p \rightarrow q$ and $q \rightarrow r$, and conclusion $p \rightarrow r$ forms a valid rule of deduction.
2. Use a truth table to determine if the propositions $p \lor q$ and $(\neg p) \land (\neg q)$ are logically equivalent.

## Learning Target 8

>Given a recurrence relation for a sequence or other structure, I can find several instances of the sequence or structure.

1. Consider the recurrence relation $a_n = 2a_{n-1} - 3a_{n-2}$ with initial conditions $a_0 = 1$ and $a_1 = 2$. Find the first five terms of the sequence.
2. Consider the recurrence relation $a_n = 3a_{n-1} + n$ with initial condition $a_0 = 1$. Find the first five terms of the sequence.
3. Consider the following set defined recursively: The number $2$ is an element of the set, and if $a$ is an element of the set then $a/2$ is also an element of the set. List at least five elements of the set.


## Learning Target 9

>(**CORE**) Given a statement to prove by mathematical induction, I can set up the framework for its proof.

Consider the statement: *For all positive integers $n$, $1 + 2 + 3 + \dots + n = \dfrac{n(n+1)}{2}$.* Suppose we want to prove this statement by induction.

1. State the predicate involved in the proposition.
2. State the value of the variable that corresponds to the base case. 
3. Prove that the base case holds. 
4. State the inductive hypothesis. 
5. State the inductive step (what you would need to prove to complete the argument). Note, you do not need to provide a completed proof here. 

## Learning Target 10

>Given a set in roster notation, I can rewrite it in set-builder notation and vice versa, and I can determine its elements and subsets.

1. Given the set $A = \lbrace 1, 2, 3 \rbrace$, list all the subsets of $A$.
2. Given the set $B = \lbrace x \in \mathbb{N} \, | \, 1 \leq x \leq 5 \rbrace$, list all the elements of $B$. If you believe this is incorrect set syntax, state why.
3. Given the set $C = \lbrace x \, | \, x \in \mathbb{Z} \, \text{and} \, x \, \text{is even} \rbrace$, write $C$ in roster notation. If you believe this is incorrect set syntax, state why.
4. Given the set $D = \lbrace x \, \% 10 \, | \, x \in \mathbb{N} \rbrace$, write $D$ in set-builder notation. If you believe this is incorrect set syntax, state why.

## Learning Target 11

>(**CORE**) I can find the union, intersection, Cartesian product, and difference of two sets; the complement of a set; and the cardinality of a finite set.

Note: We usually indicate the complement of a set $A$ by putting a bar over the $A$. However this notation doesn't render well online or in some of the publishing tools I am using. Therefore we will use $A^c$ to indicate the complement of $A$ from here on out. 

Consider the sets $A = \lbrace 1, 2, 3 \rbrace$ and $B = \lbrace 2, 3, 4 \rbrace$, $C = \lbrace  6,7,8 \rbrace$ and the universal set $U = \lbrace 1, 2, 3, 4, 5 \rbrace$.

1. Find $A \cup B$.
2. Find $A \cap B$.
3. Find $A \times C$.
4. Find $A \setminus B$.
5. Find $A^c$.
6. Find $|A|$.

## Learning Target 12

>I can determine if a mapping between two sets is a function; if it is, I can determine if it is injective, surjective, and/or bijective.

Below are six mappings between sets, numbered 1 through 6. For each mapping, state if it is a function, and if it is a function, also state if it is injective, surjective, and/or bijective or none of these. 

![alt text](lt12-exam3.png)

## Learning Target 13

>(**CORE**) I can solve simple counting problems that involve a combination of the Additive Rule, Multiplicative Rule, and Principle of Inclusion/Exclusion.

Solve the following counting problems. Be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 


1. A student owns 8 pairs of pants, 8 shirts, 2 ties, and 8 jackets. How many different outfits can the student wear to school if each outfit must consist of one of each item?
2. A standard Missouri state license plate consists of a sequence of two letters, one digit, one letter, and one digit. An example is `CX8 W2`. There are no other restrictions on the contents of the plate. How many such license plates can be made?
3. In a class of 30 students, 18 students like basketball, 15 students like soccer, and 12 students like both basketball and soccer. How many students like basketball or soccer (or both)?