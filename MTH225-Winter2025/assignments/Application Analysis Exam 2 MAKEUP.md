# Application/Analysis Exam 2

## Multiple Choice

For each of the ten items below, circle the letter of the response that is most correct. You do not need to give any explanation; only correct answers count on this part. 

1. Consider the function $f: \mathbb{N} \rightarrow \mathbb{N}$ that takes a natural number as input and returns the sum of its digits. For example $f(123) = 6$. Here, $\mathbb{N} = \lbrace 0, 1, 2, 3, 4 \dots \rbrace$ is the set of natural numbers. This function is 

    - (a) Neither injective nor surjective 
    - (b) Injective, but not surjective 
    - (c) Surjective, but not injective
    - (d) Bijective
    - (e) None of these 

2. The cardinality of the power set of $A = \lbrace 1,2,3 \rbrace$ is 

    - (a) $0$ 
    - (b) $3$
    - (c) $8$ 
    - (d) $9$
    - (e) None of these 

3. If $A = \lbrace 1,2,3,\dots, 10\rbrace$ and $B = \lbrace 1,2,3 \rbrace$ then the cardinality of $A \times B$ is 

    - (a) $13$
    - (b) $30$
    - (c) $1000$
    - (d) $59049$
    - (e) None of these 

4. A set $A$ has 10 elements and a set $B$ has 14 elements. Their intersection $A \cap B$...
   - (a) Has exactly 4 elements 
   - (b) Has exactly 10 elements
   - (c) Has at least 4 elements, possibly more
   - (d) Has at most 14 elements, possibly less
   - (e) None of these 

5. The number $\binom{8}{3}$ counts 
   - (a) The number of 8-bit binary strings that have exactly three `0` bits
   - (b) The number of three-element subsets of the set $\lbrace a,b,c,d,e,f,g,h \rbrace$  
   - (c) The number of ways to select three elements from the set $\lbrace a,b,c,d,e,f,g,h \rbrace$ and arrange them in alphabetical order
   - (d) All of the above
   - (e) Just (a) and (b)

6. The binomial coefficient is used in counting problems that involve 
    - (a) Selections of items from a set where the order of selection matters
    - (b) Selections of items from a set where the order of selection does not matter
    - (c) Arrangements of items in a sequence
    - (d) All of the above
    - (e) Just (a) and (b)

7. The number of ways to select a committee of 5 people from a group of 10 people, where the order of selection does not matter, is 
   - (a) $\binom{10}{5}$
   - (b) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6$
   - (c) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5$
   - (d) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4$
   - (e) None of these

8. The number of ways select $k$ items from a set of $n$ items where repetition is not allowed, is given by
    - (a) $n^k$
    - (b) $n!/(n-k)!$
    - (c) $\binom{n}{k}$
    - (d) $n!/k!$
    - (e) None of these

9. The number of ways to pick two books from a collection of four different books is 
    - (a) $\binom{4}{2}$
    - (b) $4!$
    - (c) $P(4,4)$
    - (d) $4 \times 3 \times 2$
    - (e) None of these

10. If $A \cap B = \emptyset$ then we say that $A$ and $B$ are 
    - (a) Empty 
    - (b) Disjoint
    - (c) Separate 
    - (d) Mutually exclusive
    - (e) None of these 

<div style="page-break-after: always;"></div>

## Problem Group 1

Do EXACTLY ONE of the following problems. If you do the first one, you need to do both parts. Turning in work on both problems will result in the entire group being discarded. **Do not merely give an answer, or just the setup for a calculation followed by an answer, but a complete explanation for your approach, in clear English written in complete sentences that explains why your solution is correct.** Any solution that is not accompanied by such an explanation will not be considered a successful attempt. 

1. Suppose we have 10 identical apples and 3 distinct boxes. How many ways are there to distribute the apples into the boxes? 
   - (a) Here is an *incorrect* approach: Number the boxes 1, 2, and 3. For each apple, we can choose to put it in box 1, box 2, or box 3. So there are $3^{10}$ ways to distribute the apples. Explain why this approach is incorrect.
   - (b) Apply the method discussed in Homework 8 to find the correct answer. Show all your work and explain your reasoning and setup in plain English. **Do not just state a formula and plug in numbers!** If you use a formula, explain what it means and how you arrived at it.
2. Here is an identity involving binomial coefficients: For all natural numbers $n$ and $k$ with $n \geq k$, $\binom{n}{k} = \binom{n}{n-k}$. Prove that this identity is true, *without* using the closed formula or induction, but instead by using an argument based on counting and an interpretation of the meaning of $\binom{n}{k}$. Explain your reasoning in detail; there should not be any calculations involved, just clear English explanations. 

<div style="page-break-after: always;"></div>

## Problem Group 2

Do EXACTLY ONE of the following problems. Whichever one you do, you need to do all parts. Turning in work on both problems will result in the entire group being discarded.  **Do not merely give an answer, or just the setup for a calculation followed by an answer, but a complete explanation for your approach, in clear English written in complete sentences that explains why your solution is correct.** Any solution that is not accompanied by such an explanation will not be considered a successful attempt. 

1. Recall that $\mathbb{S} = \lbrace a, b, c, d, e, f, g \rbrace$. 
   - (a) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is injective, but not surjective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is injective and how you know that it is not surjective. 
   - (b) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is surjective, but not injective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is surjective and how you know that it is not injective. 
   - (c) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is both injective and surjective, but not just the "identity" function that maps every number to itself. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function both injective and surjective. 
   - (d) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is neither injective nor surjective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is not injective and how you know that it is not surjective. 
2. Consider strings of eight uppercase English letters, like `HELLODAD` or `XYRTPPGH`. How many such strings are there...
   - (a) If letters can be repeated? 
   - (b) That start with `X`, if letters cannot be repeated? 
   - (c) That do not contain any vowels (A, E, I, O, or U) and letters cannot be repeated?  

<div style="page-break-after: always;"></div>


## Problem Group 3

Do EXACTLY ONE of the following problems. If you do the second one, you need to do all three parts. Turning in work on both problems will result in the entire group being discarded.  **Do not merely give an answer, or just the setup for a calculation followed by an answer, but a complete explanation for your approach, in clear English written in complete sentences that explains why your solution is correct.** Any solution that is not accompanied by such an explanation will not be considered a successful attempt. 

1. Think about making strings using only the letters a, b, and c, for example `bbaabcaaaa`. How many strings of length 10 can be made using these letters, that have exactly 3 a's or exactly 4 b's? 
2. How many subsets of a set with ten elements 
   - (a) Either start with `aa` or end with `cc`? 
   - (b) Have at least 6 elements?

<div style="page-break-after: always;"></div>

### This page left blank in case you need extra room. If you use this space, please clearly indicate which problem you are putting on this page. 
