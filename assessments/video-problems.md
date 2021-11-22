Here are the video problems you requested. Read the instructions carefully before making any videos: https://hackmd.io/@rtalbert235/BJC3EJZ7F


CA.1
Compute: 
10011000 + 01111111
10011000 - 01111111
11011 x 11
110011001 divided by 11  

L.1

Take the statement "If I copy my work from Stack Exchange, I will be dismissed from GVSU" and...
- Identify the hypothesis and conclusion
- State the negation, converse, and contrapositive.

L.2

Use truth tables to determine whether the two statements ~(P ^ Q) and (~P) v (~Q) are logically equivalent.
Make a truth table for the statement (P --> Q) ^ (Q --> R). Include columns for all intermediate steps. 

L.3

Consider these two predicates whose domain is the entire set of integers:
P(n):  The last two digits of n are 42
Q(n):  The square root of n is an integer

- State the truth values of ∃n P(n), ∃n Q(n), and ∀n P(n). Give a one-sentence explanation for each.
- State the negation of: "Every time I drive through Grand Rapids, I get lost."

SF.1

- Restate the following in roster notation:
{ x in N : The tens digit of x is 5 }
{ x in N : x**2 + 1 = 1}
{ a in Z : a - 4 > 0 }
{ b - 4  : b in {0,1,2,3,4}}


- Write the set {3, 33, 333, 3333, 33333, ... } using set builder notation.
- Write the set {1,3} using set builder notation. 




SF.2

Let A = {2,5}, B = {n in N : n % 5 = 0}, and C = {1, 2, ...., 10}. The universal set is the set of all natural numbers. Determine all the following:
- A U C
- A ∩ B
- A x {q,r,s}
- | C \ B | 
 

Let A = {1,3,5,7,9}, B = {1,2,4,8}, C = {1,7}. The universal set for these is U = {0,1,2,..., 10}. Find each of the following. 
A ∩ C
B U C
A \ B
B x C
|P(A)| 


SF.3

Below are three mappings from {0,1,2,3,4} to {0,1,2,3,4}. For each one, state whether the mapping is a function. If it is not, give a specific explanation why not. Otherwise, if the mapping is a function, state the domain, range, and codomain. 

f: {0,1,2,3,4} --> {0,1,2,3,4}  given by f(x) = (x+1) % 4
g: {0,1,2,3,4} --> {0,1,2,3,4} given by g(x) = 1 for all x
h: {0,1,2,3,4} --> {0,1,2,3,4} given by h(0) = 1, h(1) = 2, h(2) = 3, h(3) = 4, h(4) = 0, h(0) = 4


SF.4
For each of the following, determine whether the function is injective, then determine if it is surjective, then determine if it is bijective. If the function FAILS to have a property, give a specific example that demonstrates this. 

f: N --> N given by f(n) = n + 1
f: {All possible binary strings} --> {0,1} defined by f(string) = rightmost bit of that string. For example f(110011)  = 1. 
g: {0,1,2,3} --> {1,2,4,8} given by g(n) = 2**n (2 to the nth power) 
g: Z --> Z given by g(n) = n**3  
h: Z --> N given by h(n) = n**2 (n squared) 
h: N --> N given by h(n) = n + 1

C.1

- Identification numbers at a university look like a string of 8 characters --- the first character is either the letter ``F'', ``S'', or ``A'' (for faculty, students, administrators) and the other 7 are one-digit numbers. How many valid ID numbers are possible?
- Among 25 kids in a kindergarten class, 20 have brown hair, 22 are girls, and 8 are girls with brown hair. How many kids are either girls or have brown hair?
- How many 16-bit binary strings either start with two 1's on the left or end with two 1's on the right? 
- How many 10-digit hexadecimal numbers are possible? 


C.2
We will use the notation binom(n,k) to mean the binomial coefficient "n choose k". Solve each problem --- show your work and explain your reasoning. 


- Compute binom(7,2), binom(10,9) and binom(10,1) and show work/explain your reasoning. 
- How many subsets of {1,2,3,...,50} have exactly 37 elements? 
- How many 16-bit binary strings have exactly 5 1's? 




C.3

Solve each problem --- show your work and explain your reasoning. 

- How many ways are there to select a president and vice president from a group of 20 people? Show the setup and give the numerical answer.
- How many ways are there to rearrange the letters of the word "grand"? Show the setup and give the numerical answer.

C.4

Solve each problem --- show your work and explain your reasoning. 

- How many natural number solutions are there to the equation a + b + c + d = 6? 
- How many *positive integer* solutions are there to the equation a + b + c + d = 6? 
- How many ways are there to give out 10 identical brochures to 5 students? 
- How many ways are there to give out 10 identical brochures to 5 students if each student must get at least one brochure?  


RI.1 
List the first six terms of each sequence.

a(n) = 2*4^n - 1 where n = 1, 2, 3, ...
b(0) = 1, b(n) = 2b(n-1) + n for n > 0
c(0) = 2, c(1) = 4, c(n) = 3c(n-1) - c(n-2) for n > 1
d(n) = 4 + 2n where n = 0, 1, 2, 3, ... 

RI.2

- Compute the following sums: 

- Write the sum 3 + 6 + 9 + 12 + 15 + 18 using correct sigma notation. 
- Write the sum 1 + 0.1 + 0.01 + 0.001 using correct sigma notation. 


RI.4 
Determine whether the function f(n) = 2*5^n is a solution to the recurrence relation a(0) = 2, a(n) = 5a(n-1) for n > 0. 

RI.5 
Solve the recurrence relation a(n) = 5*a(n-1) - 6*a(n-2), a(0) = 2 and a(1) = 4.

RI.6 
Suppose we want to prove the following statement using mathematical induction: For all n >= 8 (that is, greater than or equal to 8), n**2 > 7n + 1.  Here n**2 means n squared. 
- State and prove the base case. 
- State the inductive hypothesis. 
- Outline the rest of the proof following the inductive hypothesis. Your outline must be specific.  