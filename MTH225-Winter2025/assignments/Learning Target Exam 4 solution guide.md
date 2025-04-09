# MTH 225: Learning Target Exam 4 -- Solutions Guide 

## NOTES ON THIS GUIDE

**Answers for Learning Targets 1, 2, 3 and 5 are not given in this guide** because they can be checked using a technological tool. Please consult [the "How To Practice" guide](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/How%20to%20practice.md) for links to those tools. 

---


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: If $p$ is a prime number, then $p$ is odd.

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
- Some submissions for the negation were ambiguous or ill-formed sentences. Example: If $p$ is a prime number *and* $p$ is not odd." (Emphasis on "and") This is not a complete sentence and it is not clear what the statement means. The negation must be a complete sentence that is clearly a conjunction and not an implication. 

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

Consider the proposition: For all positive integers $n$, $3^n - 1$ is even. Suppose we want to prove this statement by induction.

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

- Several submissions left off the important phrase "is even" from the predicate, inductive hypothesis, or inductive step. Note that the expression $3^n - 1$ by itself is not a predicate. A predicate is a statement that can be true or false depending on the value of the variable. The statement $3^n - 1$ is not a statement that can be true or false, it is just an expression. Since it cannot be true or false, we can neither "assume" it nor "prove" it. For example in the inductive hypothesis, the statement "for some positive integer $k$, $3^k - 1$" does not make sense because we cannot "assume $3^k - 1$". We have to assume that something is *true about* $3^k - 1$, namely that it is even. 
- Some submissions had an incorrect base case, commonly $n=0$. This is not the base case because the proposition is claimed to be true "for all positive integers", and $0$ is not a positive integer.

## Learning Target 10

>Given a set in roster notation, I can rewrite it in set-builder notation and vice versa, and I can determine its elements and subsets.
 

1. Below are several statements about sets and elements. Label each one as **TRUE** or **FALSE**. 

   a) $5 \in \emptyset$

   b) $\lbrace 6,7,8\rbrace \subseteq \lbrace 5,7,9\rbrace$

   c) $\frac{1}{2} \in \mathbb{Z}$ 

   d) $\mathbb{Z} \subseteq \mathbb{N}$ 

   e) $\emptyset \subseteq \lbrace 1,2,3,4,5\rbrace$

   

2. Here are three sets written in set-builder notation. For each, if the set is written using correct set syntax, rewrite it using roster notation. If the set is written using incorrect syntax, write **INCORRECT SYNTAX**. 

   a) $\lbrace n \in \mathbb{N} \ : \ n \ \\% \ 3 = 1 \rbrace$ 

   b) $\lbrace n \in \mathbb{N} \ : \ 2^n \rbrace$ 

   c) $\lbrace  x \ \\% \ 3 \ : \ x\in \lbrace 1,2,3,\dots 10 \rbrace \rbrace$


**Answers:** 

1. (Explanations are not necessary; they're just here to help you understand the answers.)
   - a) FALSE. The empty set has no elements, so $5$ cannot be in it. 
   - b) FALSE. The set $\lbrace 6,7,8\rbrace$ is not a subset of $\lbrace 5,7,9 \rbrace$ because $6$ and $8$ are not in the second set. 
   - c) FALSE. The set of integers $\mathbb{Z}$ contains whole numbers, but not fractions like $\frac{1}{2}$. 
   - d) FALSE. The set of integers $\mathbb{Z}$ contains negative numbers, while the set of natural numbers $\mathbb{N}$ only contains non-negative whole numbers. 
   - e) TRUE. The empty set is a subset of every set.

2. 
   - a) $\lbrace 1, 4, 7, 10, 13, 16, 19, 22, \dots \rbrace$ (This is the set of all natural numbers that are congruent to $1$ modulo $3$.)
   - b) INCORRECT SYNTAX. The expression following the vertical bar is not a predicate, it's a formula, so it cannot be used as a condition for filtering. 
   - c) $\lbrace 1, 2, 0 \rbrace$ This is mapping the "mod 3" function onto the given set. Notice, we do not repeat anything in a set, so $\lbrace 1, 2, 0, 1, 2, 0, 1, 2, 0, 1 \rbrace$ is incorrect. 


### Notes

- Having 1(d) as "True" was a common mistake. Please be aware of the definitions of the special named sets (integers, natural numbers, real numbers). 
- Several submissions included negative numbers in the response for 2(a). Those are not natural numbers, so they are not in the set that is being filtered. 
- Several submissions gave $\lbrace 1, 2, 0, 1, 2, 0, 1, 2, 0, 1 \rbrace$ as the response to 2(c), not realizing that sets do not repeat elements. If this was the ONLY mistake on this Learning Target, it was treated as a "simple" error and Master rating was awarded, but this may not be the case in the future. Remember: No repetitions in sets! This is very important in CS applications. 
- Several submissions continue to not distinguish between correct and incorrect syntax on set-builder notation. If this is you, a primary goal for you should be to come to terms with that distinction as soon as possible. 


## Learning Target 11

>(**CORE**) I can find the union, intersection, Cartesian product, and difference of two sets; the complement of a set; and the cardinality of a finite set.

**Note**: We usually indicate the complement of a set $A$ by putting a bar over the $A$. However this notation doesn't render well online or in some of the publishing tools I am using. Therefore we will use $A^c$ to indicate the complement of $A$ from here on out. 

Consider the sets $A = \lbrace 0, 1, 2, 3, 4 \rbrace$,  $B = \lbrace 4, 5, 6 \rbrace$, $C = \lbrace  6,7,8 \rbrace$ and the universal set $U = \lbrace 0, 1, 2, \dots, 10  \rbrace$.

1. State $B \cup C$.
2. State $A \cap B$.
2. State $B \times C$.
3. State $C \setminus A$.
4. State $B^c$.
5. State $|A|$.

**Answers:**

1. $B \cup C = \lbrace 4, 5, 6, 7, 8 \rbrace$.
2. $A \cap B = \lbrace 4 \rbrace$.
3. $B \times C = \lbrace (4,6), (4,7), (4,8), (5,6), (5,7), (5,8), (6,6), (6,7), (6,8) \rbrace$.
4. $C \setminus A = \lbrace 6, 7, 8 \rbrace$.
5. $B^c = \lbrace 0, 1, 2, 3, 7, 8, 9, 10 \rbrace$.
6. $|A| = 5$.

### Notes

- A few submissions were not using the correct delimiters (braces, brackets, etc.) in part 3, the Cartesian product. A common incorrect response was to write $B \times C = \lbrace \lbrace 4,6 \rbrace, \lbrace 4,7 \rbrace, \lbrace 4,8 \rbrace, \lbrace 4,6 \rbrace, \dots, \lbrace 6,8 \rbrace \rbrace$. This is incorrect because the Cartesian product is a set of ordered pairs, so the entire set must be enclosed in braces; and the objects inside the set must be enclosed in parentheses because they are ordered pairs -- not enclosed in set braces. 
- Some submissions simply gave the set $A$ in part 5 rather than its cardinality. Others found the cardinality (5) and put it inside set braces, for a response of $\lbrace 5 \rbrace$. This is incorrect. The cardinality of a set is a number, not a set.



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

1. Standard automobile license plates in a country display 2 numbers, followed by 2 letters, followed by 3 numbers. How many different standard plates are possible in this system? (Assume repetition of letters and numbers is allowed.)
2. A ternary string is a string made up of 0's, 1's. and 2's. How many ternary strings of length 8 are there?
3. Every one of the 4000 students at Southern Michigan University owns either a tablet or a smartwatch (or both). Surveys show that 3500 students own a tablet, and 1000 students own a smartwatch. How many students own both a tablet and a smartwatch?

**Answers:**

1. This is literally a license plate problem! There are 10 ways to fill in each of the five number slots and 26 ways to fill in each of the letter slots, so the total is $10^5 \cdot 26^2 = 67600000$. 
2. There are 8 slots to fill and 3 free choices for each slot, so the total is $3^8 = 6561$. 
3. The number of students who have either a tablet or a smartwatch (which is all 4000 students) is the number who have a tablet (3500), plus the number who have a smartwatch (1000), minus the number of students who have both. This last quantity is what we want to find this time; give it the variable $x$ for the moment. Then $4000 = 3500 + 1000 - x$, so $4000 = 4500 - x$ which means $x = 500$ students who own both devices.  


## Learning Target 14

On the following, be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 

1. Compute the following. 
   - a. $\binom{10}{3}$
   - b. $\binom{20}{7}$
   - c. $\binom{100}{0}$
2. A club has 25 members. How many ways are there to choose 5 members from the club to represent the club at an activity fair? 
3. A club has 25 members. How many ways are there to choose the president, vice president, and secretary of the club if no one can hold more than one office?

**Answers:**

1. .
    - $\binom{10}{3} = \dfrac{10!}{3! 7!} = \dfrac{10 \cdot 9 \cdot 8}{3 \cdot 2 \cdot 1} = 120$
    - $\binom{20}{7} = \dfrac{20!}{7! 13!} = \dfrac{20 \cdot 19 \cdot 18 \cdot 17 \cdot 16 \cdot 15 \cdot 14}{7 \cdot 6 \cdot \cdots \cdot 2 \cdot 1} = \dfrac{390700800}{5040} = 77520$
    -  $\binom{100}{0} = 1$  (Because this number counts the number of 100-bit binary strings with no `1` bits, and there is only one of those, the zero string.)
2. We are merely selecting 5 members from a group of 25 with no other restrictions. So the count is $\binom{25}{5} = 53130$. 
3. This is a license plate situation: There are 25 people who can be chosen for president, then 24 for vice-president, then 23 for secretary. So the count is $25 \cdot 24 \cdot 23 = 13800$. This is the same as $P(25,3) = \dfrac{25!}{22!}$. 

### Notes

- Several submissions used the binomial coefficient on part 3, which is incorrect. The binomial coefficient counts the number of ways to choose a subset of a set, but this problem is asking for the number of ways to choose an ordered list of three people from a set of 25. The binomial coefficient does not count ordered lists, so it is not appropriate here. The best way to view it is as a license plate problem, where we have 25 choices for the first slot, 24 for the second, and 23 for the third.

## Learning Target 15

Below are four integer sequences. Label each one as **arithmetic**, **geometric**, or **neither**. Then, if a sequence is either arithmetic or geometric, give *both* a closed formula *and* a complete recursive definition for the sequence. **You are to assume that all starting indexes are 0, not 1**. You do not need to show your work, but your answers must conform to the Standards for Student Work Document. 

1. $4, 2, 1, 1/2, 1/4, \dots$
2. $1, 5, 6, 11, \dots$
3. $4, 8, 12, 16, 20, 24, \dots$ 
4. $0, 1, 0, 1,0, 1, \dots$

**Answers:**

1. Geometric (with common factor of $1/2$.) 
    - Closed formula: $a(n) = 4 \cdot \left( \frac{1}{2} \right)^n$. 
    - Recursive: $a_0 = 4$ and $a_n = \frac{1}{2}a_{n-1}$ when $n > 0$. 
2. Neither. 
3. Arithmetic (with common step size $4$.)
    - Closed formula: $a(n) = 4 + 4n$. 
    - Recursive: $a_0 = 4$ and $a_n = 4 + a_{n-1}$ when $n > 0$. 
4. Neither. 