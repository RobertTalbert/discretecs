# Application/Analysis Homework 7

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 7**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. A true-false test contains 9 questions. In how many different ways can the 9-question test be answered?
2. Standard automobile license plates in a country display 2 numbers, followed by 2 letters, followed by 3 numbers. How many different standard plates are possible in this system?
3. A girl owns 8 pairs of pants, 8 shirts, 1 ties, and 8 jackets. How many different outfits can the girl wear to school if each outfit must consist of one of each item?


 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

1. A set $A$ has 10 elements and a set $B$ has 14 elements. Their union $A \cup B$...
   - (a) Has exactly 4 elements 
   - (b) Has exactly 24 elements
   - (c) Has at least 24 elements, possibly more
   - (d) Has at most 24 elements, possibly less
   - (e) None of these 

2. A "ternary string" is made up of 0's, 1's, and 2's -- for example, `12002210`. The number of ternary strings of length 8 is 
   - (a) 24
   - (b) 256
   - (c) 512
   - (d) 6561
   - (e) Cannot be determined from this information alone

3. The number of 8-bit binary strings that either start (on the left) with a `1` or end (on the right) with a `0` is 
   - (a) 256
   - (b) 448
   - (c) 512
   - (d) 576
   - (e) None of these 

4. The number $\binom{8}{3}$ counts 
   - (a) The number of 8-bit binary strings that have exactly three `0` bits
   - (b) The number of three-element subsets of the set $\lbrace a,b,c,d,e,f,g,h \rbrace$  
   - (c) The number of ways to select three elements from the set $\lbrace a,b,c,d,e,f,g,h \rbrace$ and arrange them in alphabetical order
   - (d) All of the above
   - (e) Just (a) and (b)

5. Consider the counting problem: *"At a restaurant there are 5 kinds of pasta and 2 types of sauce. How many different ways can a customer order one kind of pasta and one type of sauce?"* The principle or tool most likely to be used to solve this problem is
    - (a) The Additive Principle
    - (b) The Multiplicative Principle
    - (c) The Principle of Inclusion and Exclusion
    - (d) The Binomial Coefficient
    - (e) None of these 


## Problems to solve 


1. Consider strings of eight uppercase English letters, like `HELLODAD` or `XYRTPPGH`. How many such strings are there...
- (a) If letters can be repeated? 
- (b) If letters cannot be repeated? 
- (c) That start with `X`, if letters can be repeated? 
- (d) That start with `X`, if letters cannot be repeated? 
- (e) That start and end with `X`, if letters can be repeated? 
- (f) That either start or end with `X`, if letters can be repeated? 
- (g) That do not contain any vowels (A, E, I, O, or U) and letters cannot be repeated? 
- (h) That contain exactly one vowel, and letters cannot be repeated? 
Note, in this problem -- as always -- you must show your work clearly and explain your reasoning process. Simply putting down an answer without explanation, or with insufficient or unclear explanation, will result in a *Semi-Complete* or *Incomplete* mark. 

2. An observation we made in class is that if you look at Pascal's Triangle and add up all the binomial coefficients in a single row of the triangle, you get a power of 2: 

![Pascal triangle row sums](pascal3.png)

We can state this as a formal conjecture: If $n$ is any natural number, then 
$$\binom{n}{0}  + \binom{n}{1} + \binom{n}{2} + \cdots + \binom{n}{n} = 2^n$$
Set up the framework for a proof of this conjecture that uses mathematical induction. That is: State and prove the base case, state the inductive hypothesis, and then state the inductive step. You do not need to provide a completed proof. (But if you want to try it, I'll give feedback on the attempt.) 


3. Here is a proposed proof of the conjecture above, that does *not* try to use mathematical induction but rather a different line of reasoning: 

>Consider the set $B_n$ of all bitstrings having length $n$. We can split this set into the set of all bistrings of length $n$ having weight $0$, the set of all bitstrings of length $n$ having weight $1$, the set of all bitstrings of length $n$ having weight $2$, and so on, up to the set of all bitstrings of length $n$ having weight $n$. Note that the cardinality of each individual set is a binomial coefficient: The cardinality of the set of all bitstrings with length $n$ and weight $k$ is $\binom{n}{k}$ by definition. And notice that the union of all of these sets is the set $B_n$ of all bitstrings having length $n$, because each bitstring of length $n$ has weight 0, or weight 1, or weight 2, etc., or weight $n$. Furthermore, all of these sets are disjoint, since any given bitstring can have only one weight (so it cannot belong to two of them). Therefore because of the Additive Principle, the sum $\binom{n}{0}  + \binom{n}{1} + \binom{n}{2} + \cdots + \binom{n}{n}$ gives the total number of bitstrings of length $n$. 
>
> But on the other hand, we know that this total number is also $2^n$ since each bitstring of length $n$ has $n$ bits and each bit has two choices, so there are $2^n$ of these by the Multiplicative Principle. 
>
> Therefore since $\binom{n}{0}  + \binom{n}{1} + \binom{n}{2} + \cdots + \binom{n}{n}$ and $2^n$ count the same thing, they are equal. 

What, if anything, is wrong with this proposed proof? 

Possible responses include: 
- Nothing is wrong with this proof. 
- This proof has no major issues with being clear, correct, or complete but it does have one or more minor ones -- then you should list those and explain why they are issues, and why they are minor. 
- This proof has one or more major issues with being clear, correct, or complete -- then you should list those and explain why they are issues, and why they are major.