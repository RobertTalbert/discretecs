# Learning Target Reassessment April 14 Solutions guide

**Note:** Learning Target 1 does not appear here because you have tools that can be used to check the solution. [Please see the "How to Practice" document](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/How%20to%20practice.md) for more information.


## Learning Target 4

>(**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, and negation.

Consider the implication: *If I drive to Detroit, then I will arrive at the concert on time.*

1. State the hypothesis and conclusion of the implication.
2. State the converse of the implication.
3. State the contrapositive of the implication.
4. State the negation of the implication.

**Answers:** 

1. Hypothesis: I drive to Detroit. Conclusion: I will arrive at the concert on time.
2. Converse: If I arrive at the concert on time, then I drive to Detroit.
3. Contrapositive: If I do not arrive at the concert on time, then I do not drive to Detroit.
4. Negation: I drive to Detroit and I do not arrive at the concert on time.


## Learning Target 9

>(**CORE**) Given a statement to prove by mathematical induction, I can set up the framework for its proof.

Consider the statement: *For all positive integers $n \geq 5$, $n^2 < 2^n$. Suppose we want to prove this statement by induction.

1. State the predicate involved in the proposition.
2. State the value of the variable that corresponds to the base case. 
3. Prove that the base case holds. 
4. State the inductive hypothesis. 
5. State the inductive step (what you would need to prove to complete the argument). Note, you do not need to provide a completed proof here. 

**Answers:**    

1. Predicate: $P(n): n^2 < 2^n$.
2. Base case: $n = 5$.
3. Base case: $5^2 < 2^5$ is true since $25 < 32$.
4. Inductive hypothesis: Assume $k^2 < 2^k$ is true for some integer $k \geq 5$.
5. Inductive step: Show that  $(k+1)^2 < 2^{k+1}$.

## Learning Target 10

>Given a set in roster notation, I can rewrite it in set-builder notation and vice versa, and I can determine its elements and subsets.


1. Here are three sets written in set-builder notation. For each, if the set is written using correct set syntax, rewrite it using roster notation. If the set is written using incorrect syntax, write **INCORRECT SYNTAX**. 

    - (a) $\lbrace x \in \lbrace 0, 1, 2, 3, \dots \rbrace | x^2 -1 = 0\rbrace$
    - (b) $\lbrace x^2 + 1 | x \in \mathbb{Z} \rbrace$
    - (c) $\lbrace x \in \mathbb{Z} | x^2  \rbrace$

2. Below are several statements about sets and elements. Label each one as **TRUE** or **FALSE**. 

    - (a) $0 \in \emptyset$ 
    - (b) $\{1,2,3\} \subseteq \{1,2,3,4\}$
    - (c) $0 \in \mathbb{Z}$
    - (d) $\mathbb{Z} \subseteq \mathbb{N}$
    - (e) $\emptyset \subseteq \{1,2,3,4,5\}$

**Answers:**

1. 
   - (a) Correct syntax and equal to $\lbrace 1 \rbrace$.
   - (b) Correct syntax and equal to $\lbrace 1, 2, 5, 10, 17, \dots \rbrace$.
   - (c) Incorrect syntax because $x^2$ is not a predicate.
2. 
   - (a) FALSE (because the empty set has no elements)
   - (b) TRUE 
   - (c) TRUE
   - (d) FALSE (because $\mathbb{Z}$ contains negative integers)
   - (e) TRUE (because the empty set is a subset of every set)



## Learning Target 11


>(**CORE**) I can find the union, intersection, Cartesian product, and difference of two sets; the complement of a set; and the cardinality of a finite set.

**Note**: We usually indicate the complement of a set $A$ by putting a bar over the $A$. However this notation doesn't render well online or in some of the publishing tools I am using. Therefore we will use $A^c$ to indicate the complement of $A$ from here on out. 

Consider the sets $A = \lbrace 0, 1, 2, 3, 4 \rbrace$,  $B = \lbrace 4, 5, 6 \rbrace$, $C = \lbrace  6,7,8 \rbrace$ and the universal set $U = \lbrace 0, 1, 2, \dots, 10  \rbrace$.


1. State $C \cap A$.
2. State $A \cup B$.
3. State $A \times C$.
4. State $C \setminus A$.
5. State $B^c$.
6. State $|A|$.

**Answers:**

1. $C \cap A = \lbrace 6, 7, 8 \rbrace \cap \lbrace 0, 1, 2, 3, 4 \rbrace = \emptyset$.
2. $A \cup B = \lbrace 0, 1, 2, 3, 4 \rbrace \cup \lbrace 4, 5, 6 \rbrace = \lbrace 0, 1, 2, 3, 4, 5, 6 \rbrace$.
3. $A \times C = \lbrace (0,6), (0,7), (0,8), (1,6), (1,7), (1,8), (2,6), (2,7), (2,8), (3,6), (3,7), (3,8) \rbrace$.
4. $C \setminus A = \lbrace 6, 7, 8 \rbrace \setminus \lbrace 0, 1, 2, 3, 4 \rbrace = \lbrace 6, 7, 8 \rbrace$.
5. $B^c = \lbrace 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 \rbrace \setminus \lbrace 4, 5, 6 \rbrace = \lbrace 0, 1, 2, 3, 7, 8, 9, 10 \rbrace$.
6. $|A| = 5$.

## Learning Target 13

>(**CORE**) I can solve simple counting problems that involve a combination of the Additive Rule, Multiplicative Rule, and Principle of Inclusion/Exclusion.

Solve the following counting problems. Be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 


1. Think about 10-character strings where the only letters used are `x` and `y`. For example, `xxyyxyyyyx`. How many of these strings are possible, that either start with an `x` or end with a `y`?
2. An ice cream store offers 5 flavors of ice cream. How many different sundaes can be made with 2 scoops of ice cream if the order of the scoops does not matter?
3. Standard automobile license plates in a country display 2 numbers, followed by 2 letters, followed by 3 numbers. How many different standard plates are possible in this system? (Assume repetition of letters and numbers is allowed.)

**Answers:**

1. The number of these strings that start with an `x` is $2^9 = 512$. The number of these strings that end with a `y` is also $2^9 = 512$. However, the number of these strings that start with an `x` and end with a `y` is $2^8 = 256$. Therefore, by the principle of inclusion/exclusion, the total number of strings that either start with an `x` or end with a `y` is $512 + 512 - 256 = 768$.
2. **Note: A detail was left out of this problem, namely that you cannot have double scoops of the same flavor.** 
   - Assuming this detail, there are $5$ choices for the first scoop and $4$ choices for the second scoop. However, since the order of the scoops does not matter, we must divide by $2$ because otherwise we are double-counting different orderings of the same two flavors (for example, chocolate then vanilla would be counted as a different sundae than vanilla followed by chocolate). Therefore, the total number of different sundaes is $\frac{5 \cdot 4}{2} = 10$. Note, this is the same thing as $\binom{5}{2}$. 
   - If you did not make the assumption that the scoops must be different, then you have to consider two cases: First the case where the scoops are different flavors, and then where they are the same flavor. The first case is considered above and comes out to 10 choices. Then there are five possible sundaes where the scoops are the same flavor (one for each flavor). Therefore, the total number of different sundaes is $10 + 5 = 15$.
3. The first two numbers can be any digit from 0 to 9, so there are $10 \cdot 10 = 100$ choices for the first two numbers. The next two letters can be any letter from A to Z, so there are $26 \cdot 26 = 676$ choices for the letters. Finally, the last three numbers can also be any digit from 0 to 9, so there are $10 \cdot 10 \cdot 10 = 1000$ choices for the last three numbers. Therefore, the total number of different standard plates is $100 \cdot 676 \cdot 1000 = 67,600,000$.


##  Learning Target 14 

>(CORE) I can compute a binomial coefficient and solve simple counting problems that involve combinations, permutations, or k-permutations.

On the following, be sure to show all work, and explain your reasoning. Responses that consist only of answers, even if correct, will not be rated as *Master*. Responses that are illegible or very difficult to follow will also not be rated as *Master*. 

1. Compute the following. 
   - a. $\binom{11}{9}$
   - b. $\binom{25}{20}$
   - c. $\binom{1000}{1}$
2. Think about 10-character strings where the only letters used are `x` and `y`. For example, `xxyyxyyyyx`. How many of these strings are possible that contain exactly 4 `x`'s? 
3. A committee of 3 people is to be chosen from a group of 12 people. How many different committees are possible if the order in which the committee members are chosen does not matter?

**Answers:**

1. 
   - a. $\binom{11}{9} = \frac{11!}{9!2!} = \frac{11 \cdot 10}{2} = 55$.
   - b. $\binom{25}{20} = \frac{25!}{20!5!} = \frac{25 \cdot 24 \cdot 23 \cdot 22 \cdot 21}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = 53130$.
   - c. $\binom{1000}{1} = \frac{1000!}{1! 999!} = \frac{1000}{1} = 1000$. Or, just notice that this binomial coefficient counts the number of ways to select one item from a group of 1000, and there are 1000 ways to do this (one for each item that might be selected). 
2. The number of these strings that contain exactly 4 `x`'s is the same as the number of ways to choose 4 positions from 10 for the `x`'s. This is $\binom{10}{4} = \frac{10!}{4!6!} = \frac{10 \cdot 9 \cdot 8 \cdot 7}{4 \cdot 3 \cdot 2 \cdot 1} = 210$.
3. The number of different committees of 3 people that can be chosen from a group of 12 people is $\binom{12}{3} = \frac{12!}{3!9!} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220$.

## Learning Target 15

>I can determine if a sequence is arithmetic or geometric; and I can state closed-form and recursive formulas for arithmetic and geometric sequences.

**PLEASE NOTE: The instructions on this one have changed from Learning Target Exam 4.** 

Below are four integer sequences. For each one, determine if it is arithmetic, geometric, or neither and clearly state "arithmetic", "geometric", or "neither". Then, if a sequence is either arithmetic or geometric, **give both a closed formula and a complete recursive definition for the sequence**. Please note, *both* kinds of formulas are required for *each* sequence that you label as arithmetic or geometric. No further explanation is needed if you decide a sequence should be labeled as "neither".

**You are to assume that all starting indexes are 0, not 1**. You do not need to show your work, but your answers must conform to the Standards for Student Work Document.


1. $2, 6, 18, 54, \dots$
2. $3, 3, 7, 6, 4, \dots$
3. $10, 12, 14, 16, \dots$
4. $-1, 1, -1, 1,-1, 1, \dots$

**Answers:**

1. Geometric. 
   - Closed formula: $a_n = 2 \cdot 3^n$.
   - Recursive formula: $a_0 = 2$, $a_n = 3 a_{n-1}$ for $n \geq 1$.
2. Neither.    
3. Arithmetic. 
   - Closed formula: $a_n = 10 + 2n$.
   - Recursive formula: $a_0 = 10$, $a_n = a_{n-1} + 2$ for $n \geq 1$.
4. Neither.