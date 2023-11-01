# MTH 225: Checkpoint 7

**Learning Targets on this Checkpoint: 2, 3, and 6–13.** Learning Targets 12 and 13 are new. 

Learning Targets 2, 3, 6, 7, 8, 9, 12 and 13 are CORE Learning Targets and *must* be completed in class and on paper. 

Learning Targets 10 and 11 are non-CORE, and may be completed outside of class before 11:59pm ET today. **You must turn in your work on these as a PDF uploaded to the correct Blackboard assignment. Paper submissions are not accepted.** Submit a different PDF for each of these Learning Targets. 

**Instructions**: 

* Do not attempt any problem for which one or both of the following is true; 
  * You **aren't ready to take it** because you need more practice; or 
  * You **don't need to take it** beause you are already at Level 2 (or at Level 1 and you don't intend to go to Level 2). 

* **A basic scientific or graphing calculator is the only technology allowed**. If you are using a smartphone app as your calculator, your phone *must* be switched to airplane mode. The use of any other technology, or phone apps with internet enabled, will be treated as academic dishonesty. 
* **You are not allowed any notes** on Checkpoints. 
* Make sure to **put your name on each page you are handing in.**
* Note that each problem has *Success Criteria* listed. These are the standards for what constitutes a "successful" demonstration of skill. Make sure to read through those criteria and double check your work against them before turning in your work. 



## Learning Target 2

> (**CORE**) I can add, subtract, multiply, and divide positive integers in base 2. 



1. Add the base-2 integers `11000001` and `10100101`. **Show your work and circle your answer**. 
2. Subtract the base-2 integers `11000001` and `10100101`. **Show your work and circle your answer**. 
3. Multiply the base-2 integers `1111` and `101`. **Show your work and circle your answer**. 
4. Divide the base-2 integer `110011` by `101`. **Show your work and circle your answers**. 

**Success criteria:** All four answers are correct, and the work leading to each answer is clear and legible. **All arithmetic must be done entirely in base 2 without converting to base 10 first.** Up to two "simple errors" (as described in the *Standards for Student Work* document) are allowed. 



## Learning Target 3

> (**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, inverse, and negation.

Consider the statement: *If the input is a list, then an error is returned*.  State, in clear English: 

1. The hypothesis of the statement
2. The conclusion of the statement
3. The converse of the statement
4. The contrapositive of the statement
5. The inverse of the statement
6. The negation of the statement (Do not just put "not" or "it is not the case that" in front of the statement)

**Success criteria:** All six statements are given correctly. (There is no "work" required on this one.)



## Learning Target 6

> (**CORE**) I can determine elements of a recursively-defined sequence using a recurrence relation and derive a recurrence relation for a recursively-defined sequence.



1. Consider the sequence of numbers $a_n$ given by the recursive formula $a_0 = 1$, $a_1 = 5$, and for $n > 1$, $a_n = (a_{n–1})^2 - 2a_{n-2}$. Find the values of $a_2$, $a_3$, $a_4$ and $a_5$. (Note that $a_0$ and $a_1$ are already stated. ) Show your work on each calculation. 
2. Consider the sequence of numbers: $2, 6, 18, 54,  \dots$. If $a_0 = 2$, give a recurrence relation that generates the rest of the sequence. (Do *not* give a closed formula, but a recursive definition. The base case is $a_0 = 2$.) 

**Success criteria:** On the first part, the recursive formula must be used correctly with the correct base cases, and the mathematical work leading to the answers must be shown. On the second part, the recurrence relation must be recursive (not a closed formula) and correctly generate the terms of the sequence. No "work" is required on the second part. No more than two simple errors are allowed total. 



## Learning Target 7

> (**CORE**) Given a statement to prove using mathematical induction, I can state the framework of a proof. (Identify the predicate, identify and prove the base case, state the inductive hypothesis, and state what needs to be proven in the inductive step)

Suppose we want to prove the following statement using mathematical induction: 

> For every positive integer $n \geq 4$, $2^n < n!$. 



1. Write out the predicate involved in this statement: $P(n)$ says…
2. What value of $n$ corresponds to the base case? 
3. Prove that the base case holds, by direct computation or demonstration. 
4. Clearly state the inductive hypothesis without using the notation "$P(n)$". 
5. Clearly state what needs to be proven in the inductive step. Do not use the notation "$P(n)$" . You do NOT have to actually prove this statement; just state it. 

**Success criteria:** The predicate is correctly identified and does not include a quantifier. The correct value of $n$ for the base case is identified. The proof of the base case is clearly written and is correct. The inductive hypothesis is correctly and clearly stated and does not include "$P(n)$". The statement to be proven in the inductive step is correctly and clearly stated and does not include "$P(n)$". 



## Learning Target 8

> (**CORE**) I can convert a set given in roster notation to set-builder notation and vice versa; and determine if an object is an element of the set.



1. Here are three sets written in set-builder notation. For each, if the set is written using correct set syntax, rewrite it using roster notation. If the set is written using incorrect syntax, write **INCORRECT SYNTAX**. *See the success criteria below for what constitutes correct roster notation.* 

   a) $\{x \in \{a,b,c,d,e,f,g,h\} \, : \, x \ \text{is a vowel} \}$   (Reminder:A "vowel" is one of the letters A, E, I, O, or U).

   b) $\{x \in \{1,2,3,\dots, 20\} \, : \, x +3  \}$

   c) $\{x \in \{1,2,3,\dots, 20\} \, : \, x  \leq 3  \}$

2. Rewrite the set $S = \{2, 6, 18, 54,  \dots\}$  using set-builder notation. There is more than one way to do this correctly; your answer must equal $S$ and must use correct set notation and syntax. You may not use "$\{x \, : x \in S \}$" as an answer. 



**Success criteria:** On the first part, all sets with incorrect syntax must be indicated; sets with correct syntax must: 

- Have ALL its elements listed if there are 4 or fewer elements; 
- Have AT LEAST FOUR elements listed if there are 5 or more elements; 
- If the set is infinite, the roster notation must reflect this and not give a finite roster like {1,2,3,4}
- If the set is finite, the roster notation must reflect this and not give an infinite roster like {1,2,3,4,...}
- Have no more than two errors in the elements

On the second part, the set must equal $S$ and the syntax of the set notation must be correct and rephrase the set in a meaningful way. 



## Learning Target 9

> (**CORE**) I can find the intersection, union, difference, symmetric difference, power set, cardinality, cartesian product, and complement of sets.



Let $A = \{r,s,t,u,v\}$, $B = \{o,u,y\}$, $C = \{q,r,s,t\}$, and $D = \{u,v\}$  and suppose the universal set is $U = \{o,p,q,r,\dots, x,y,z\}$. Find each of the following. You do not need to show intermediate steps, but this is often helpful for you (and for the person grading your work). 

1. $A \cap C$
2. $B \cup C$
3. $D \setminus B$ 
4. $\overline{A}$
5. $D \setminus (B \cup C)$ 
6. $((A \cap B) \cup (C \cap D)) \cap \emptyset$ 
7. ${\cal{P}}(B)$ 
8. $|A \times D|$ 



**Success criteria:** The final two items are correct; and at least 5 of the first 6 are correct. 



## Learning Target 10

>  I can determine if a mapping is a function; identify the domain, range, and codomain of a function; and determine the image of a specific input in one function or a composition of functions.



Below are eight mappings. For each one: 

- State whether the mapping is a function or whether it is not a function. 
- If the mapping is a function, state its domain, range, and codomain. Phrase each one as a set using correct notation and syntax and make sure to label which one is which. 

<img src="/Users/talbertr/Desktop/cp7-lt10-2.png" alt="cp7-lt10-2" style="zoom:50%;" />

**Success criteria**: All mappings are correctly labeled as "function" or "not a function". Up to two misakes are allowed otherwise. You do not need to justify your reasoning (although having reasoning present might help you). 



## Learning Target 11

> I can determine if a function is injective, surjective, or bijective.



**NOTE: The instructions and success criteria have changed on this item. Please read both carefully before submitting work.** 

For each of the functions below, state whether the function is *injective but not surjective*, *surjective but not injective*, *neither injective nor surjective*, or *bjective*. (Note that every function must fall into exactly one of these categories.) If the function **does** have a particular property, simply state this fact without explanation. If the function **does not** have a particular property, give a *specific example* that shows that it does not have the property. Example: If a function is surjective but not injective, you can simply state that the function is surjective; but give a specific example that shows the function is not injective. See the Success Criteria for what constitutes a "specific" example. 



1. The function $f$ that maps {2,4,6,8} to {A,B,C} given by the rule: $f(2) = B$, $f(4) = C$, $f(6) = C$, $f(8) = B$. 

2. The function $f: \mathbb{N} \rightarrow \mathbb{N}$ given by the formula $f(n) = 3n$. 

3. The function $f$ that maps the set of all $8$-bit bitstrings to the set of all $8$-bit bitstrings, which works by taking the input and flipping all its bits. For example $f(10010101) = 01101010$.  



**Success criteria**: An attempt must be made on all three parts. At least two of the three parts are correctly labelled, and specific examples are given for any property that the function fails to hold. *General arguments* that merely restate a definition or its negation are not accepted – the explanation must reference specific elements in the domain or codomain that cause the function not to have the property. (Example: "There is a collision" is not specific. Which points are colliding?) 



## :new: Learning Target 12

> **(CORE)**  I can apply the Additive and Multiplicative Principles and the Principle of Inclusion/Exclusion to formulate and solve basic combinatorics problems.



Find the following and show your steps: 

1. The number of five-letter "words" that can be made from the 26 letters of the alphabet (It doesn't have to be a real word, for example `DDXXT` is allowed.)
2. The number of five letter "words" that can be made from the 26 letters of the alphabet that begin (on the left) with either `Q` or `X` 
3. The numbert of five letter "words" that can be made from the 26 letters of the alphabet that begin (on the left) with a `Q` or end (on the right) with a `T`

**Success criteria**: All three items use a correct method for counting; correct computations are set up and shown clearly; and all three answers are correct except for no more than two simple errors. 



## :new: Learning Target 13

> **(CORE)** I can compute factorials and binomial coefficients, and apply the these concepts to solve basic combinatorics problems. (permutations, selections, distributions)



1. Compute the values of each of the following, and show your steps: 

   (a) 8!

   (b) $\binom{8}{6}$   

   (c) $\binom{100}{100}$ 

2. Find the following and show your steps: 

   (a) The number of ways to rearrange the letters in the word `GRAND` 

   (b) The number of ways to form a Python list of length 3, containing only the numbers 0, 1, 2, 3, 4, 5, and 6 with no repetitions



**Success criteria**: All three parts of the first item are correct except for no more than one simple error. On the second part, a correct method for counting is used on each, correct computations are set up and shown clearly, and the answers are correct except for no more than one simple error. 