# MTH 225: Checkpoint 13

**All 15 Learning Targets are included on this Checkpoint!** 

The eight Core Learning Targets and are due in class. The seven non-Core can be done outside of class, but must be submitted to Blackboard by 11:59pm ET today, December 4. 

**Instructions**: 

* Do not attempt any problem for which one or both of the following is true; 
  * You **aren't ready to take it** because you need more practice; or 
  * You **don't need to take it** beause you are already at Level 2 (or at Level 1 and you don't intend to go to Level 2). 

* **A basic scientific or graphing calculator is the only technology allowed**. If you are using a smartphone app as your calculator, your phone *must* be switched to airplane mode. The use of any other technology, or phone apps with internet enabled, will be treated as academic dishonesty. 
* **You are not allowed any notes** on Checkpoints. 
* Make sure to **put your name on each page you are handing in.**
* Note that each problem has *Success Criteria* listed. These are the standards for what constitutes a "successful" demonstration of skill. Make sure to read through those criteria and double check your work against them before turning in your work. 



## Learning Target 1

> I can convert a positive integer from base 10 to base 2, 8, and 16 and vice versa and represent a negative integer in base 2 using two's complement notation.

Be sure to *show your work* and please *put a circle or box around each answer*. 

1. Convert the base 10 integer $378$ to octal (base 8) using the base conversion algorithm. (On this part, you *must* use the base conversion algorithm and no other method.)
2. Convert the base 16 integer $34B$ to base 10.  
3. Convert the base 2 integer `110011` to base 10. 
4. The 8-bit binary representation of the base 10 integer $32$ is `0010 0000`. Write the 8-bit binary representation of $-32$ using two's complement. 

**Success criteria:** Three of the four answers are correct, and the work leading to each answer is clear and legible. Up to two "simple errors" (as described in the *Standards for Student Work* document) are allowed. The first part must use the base conversion algorithm we learned in class. 



## Learning Target 2

> (**CORE**) I can add, subtract, multiply, and divide positive integers in base 2. 

1. Add the base-2 integers `10011000` and `10001111`. **Show your work and circle your answer**. 
2. Subtract the base-2 integers `10011000` and `10001111`. **Show your work and circle your answer**. 
3. Multiply the base-2 integers `1010` and `110`. **Show your work and circle your answer**. 
4. Divide the base-2 integer `100110` by `11`. **Show your work and circle your answers**. 

**Success criteria:** All four answers are correct, and the work leading to each answer is clear and legible. **All arithmetic must be done entirely in base 2 without converting to base 10 first.** Up to two "simple errors" (as described in the *Standards for Student Work* document) are allowed. 



## Learning Target 3

> (**CORE**) I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, inverse, and negation.

Consider the statement: **If x = 5, then print the next line.**  State, in clear English: 

1. The hypothesis of the statement
2. The conclusion of the statement
3. The converse of the statement
4. The contrapositive of the statement
5. The inverse of the statement
6. The negation of the statement (Do not just put "not" or "it is not the case that" in front of the statement)

**Success criteria:** All six statements are given correctly. (There is no "work" required on this one.)



## Learning Target 4

> I can construct truth tables for propositions involving two or three atomic propositions and use truth tables to determine if two propositions are logically equivalent.

1. Construct a truth table for $(p \vee q) \rightarrow (q \vee (\neg r))$. 
2. Construct truth tables for $\neg(p \wedge q)$ and for $(\neg p) \wedge (\neg q)$. Based on the truth tables, are these two statements logically equivalent? 

**Success criteria:** All truth tables have the correct number of rows with no duplicated rows. All intermediate columns are shown. No more than three total errors are permitted. (If you make a mistake in an intermediate column but the rest of the row is correct given that mistake, then the mistake only counts once.) The answer about whether the last two statements are logically equivalent is clearly indicated and is consistent with the truth table results. 



## Learning Target 5

> I can determine the truth value of a predicate at a specific input, the truth value of a quantified predicate, and the negation of a quantified predicate.

1. Let $P$ and $Q$ be these two predicates. Assume the domain of each is the set of all natural numbers: $0,1,2,3,4,\dots$ 

   - $P(x)$: The ones digit of $x$ is 3

   - $Q(x)$: $x-10 > 0$ 

     For each of the following, state whether the expression is **TRUE** or whether it is **FALSE**. 

     (a) $P(20)$ 

     (b) $Q(9)$ 

     (c) $\exists x P(x)$ 

     (d) $\forall x (\neg Q(x))$ 

2. Consider the statement: *All electric cars are expensive.* State the negation of this statement, without merely putting the word "not" or the phrase "it is not the case that" in front of the statement; that is, phrase the negation in terms of another quantified statement. 

**Success criteria:** At least three of the answers in the first part are correct; and the negation in the second part is correct and clearly stated. (No intermediate work is required.)



## Learning Target 6

> (**CORE**) I can determine elements of a recursively-defined sequence using a recurrence relation and derive a recurrence relation for a recursively-defined sequence.

1. Consider the sequence of numbers $a_n$ given by the recursive formula $a_0 = 1$, $a_1 = 4$, and for $n > 1$, $a_n = -a_{n-1} + 2a_{n-2}$. Find the values of $a_2$, $a_3$, $a_4$ and $a_5$. Show your work on each calculation. **Note the minus sign.** 
2. Consider the sequence of numbers: $3, 6, 9, 12, 15  \dots$. If $a_0 = 3$, give a recurrence relation that generates the rest of the sequence. (Do *not* give a closed formula, but a recursive definition.) 

**Success criteria:** On the first part, the recursive formula must be used correctly with the correct base cases, and the mathematical work leading to the answers must be shown. On the second part, the recurrence relation must be recursive (not a closed formula) and correctly generate the terms of the sequence. No "work" is required on the second part. No more than two simple errors are allowed total. 



## Learning Target 7

> (**CORE**) Given a statement to prove using mathematical induction, I can state the framework of a proof. (Identify the predicate, identify and prove the base case, state the inductive hypothesis, and state what needs to be proven in the inductive step)w

Suppose we want to prove the following statement using mathematical induction: 

> For every integer $n \geq 5$, $4n < 2^n$.  

1. Write out the predicate involved in this statement: $P(n)$ says…
2. What value of $n$ corresponds to the base case? 
3. Prove that the base case holds, by direct computation or demonstration. 
4. Clearly state the inductive hypothesis without using the notation "$P(n)$". 
5. Clearly state what needs to be proven in the inductive step. Do not use the notation "$P(n)$" . You do NOT have to actually prove this statement; just state it. 

**Success criteria:** The predicate is correctly identified and does not include a quantifier. The correct value of $n$ for the base case is identified. The proof of the base case is clearly written and is correct. The inductive hypothesis is correctly and clearly stated and does not include "$P(n)$". The statement to be proven in the inductive step is correctly and clearly stated and does not include "$P(n)$". 



## Learning Target 8

> (**CORE**) I can convert a set given in roster notation to set-builder notation and vice versa; and determine if an object is an element of the set.

1. Here are three sets written in set-builder notation. For each, if the set is written using correct set syntax, rewrite it using roster notation. If the set is written using incorrect syntax, write **INCORRECT SYNTAX**. *See the success criteria below for what constitutes correct roster notation.* 

   a) $\{4n : n \in \mathbb{N} \}$

   b) $\{x \in \mathbb{N} \, : \, 2^n \}$ 

   c) $\{x \, \text{is odd} \, : \, x\in \{1,2,3,\dots 10\}\}$

2. Rewrite the set $S = \{0, 2, 4\}$  using set-builder notation. There is more than one way to do this correctly; your answer must equal $S$ and must use correct set notation and syntax. You may not use "$\{x \, : x \in \{0,2,4\} \}$" as an answer. 



**Success criteria:** On the first part, all sets with incorrect syntax must be indicated; sets with correct syntax must: 

- Have ALL its elements listed if there are 4 or fewer elements; 
- Have AT LEAST FOUR elements listed if there are 5 or more elements; 
- If the set is infinite, the roster notation must reflect this and not give a finite roster like {1,2,3,4}
- If the set is finite, the roster notation must reflect this and not give an infinite roster like {1,2,3,4,...}
- Have no more than two errors in the elements

On the second part, the set must equal $S$ and the syntax of the set notation must be correct and rephrase the set in a meaningful way. 



## Learning Target 9

> (**CORE**) I can find the intersection, union, difference, symmetric difference, power set, cardinality, cartesian product, and complement of sets.

Let $A = \{1, 3,5\}$, $B = \{2,3\}$, $C = \{0, 5\}$, and $D = \{7\}$.  Find each of the following. You do not need to show intermediate steps, but this is often helpful for you (and for the person grading your work). 

1. $A \cap B$ 
2. $A \cup B$
3. $B \setminus A$ 
4. $A \cup (B \cap C)$ 
5. $(A \cup B) \cap C$ 
6. $|A \times D|$ 

**Success criteria:** At least five of the six are correct. 



## Learning Target 10

> I can determine if a mapping is a function; identify the domain, range, and codomain of a function; and determine the image of a specific input in one function or a composition of functions.

Below are six mappings. For each one: 

- State whether the mapping is a function or whether it is not a function. 
- If the mapping is a function, state its domain, range, and codomain. Phrase each one as a set using correct notation and syntax and make sure to label which one is which. 

<img src="/Users/talbertr/Library/CloudStorage/OneDrive-GrandValleyStateUniversity/1 Projects/MTH 225 F23/lt10-cp13.png" alt="Functions" style="zoom:50%;" />

**Success criteria**: All mappings are correctly labeled as "function" or "not a function". Up to two misakes are allowed otherwise. You do not need to justify your reasoning (although having reasoning present might help you). 





## Learning Target 11

> I can determine if a function is injective, surjective, or bijective.

For each of the functions below, state whether the function is *injective but not surjective*, *surjective but not injective*, *neither injective nor surjective*, or *bjective*. (Note that every function must fall into exactly one of these categories.) If a function **DOES HAVE** a property, you **DO NOT ** have to explain why; just state it. (For example "$F$ is injective".) If a function **DOES NOT HAVE** a property (for example if the function is not surjective) then **give a specific, concrete example where the property fails**. 

1. The function $f: \mathbb{R} \rightarrow \mathbb{R}$ given by the formula $f(x) = 3x + 2$. (Reminder, $\mathbb{R}$ is the set of all real numbers.)
2. The function $g: \mathbb{N} \rightarrow \mathbb{N}$ given by the formula $g(n) = 3n+2$. (Reminder, $\mathbb{N} = \{0,1,2,3,4,\dots\}$)
3. The function shown as #6 in the problem for Learning Target 10 above (in the lower-right of the grid).

**Success criteria**: All three parts have a good-faith effort at an attempt -- none are skipped -- and each one includes a clear explanation of reasoning. And, at least two of the three answers and explanations must be correct. 



## Learning Target 12

> **(CORE)**  I can apply the Additive and Multiplicative Principles and the Principle of Inclusion/Exclusion to formulate and solve basic combinatorics problems.

Find the following and show your steps: 

1. Sharona is at the store shopping for a new phone. There are 12 different kinds of Android phones for sale, 5 different kinds of iPhones, and 20 different kinds of flip-phones (which are neither Android nor iPhones). No other phones are for sale. She's buying one phone. How many total ways can she make this purchase? 
2. Sharona's sister, Ramona, is at the store with her and is also getting a phone, as well as a case and a charging cable. There are five different kinds of phones she could buy, 38 different cases avilable, and 10 different charging cables. She intends to buy one of each (phone, case, and cable). How many different ways are there for Ramona to make her purchase? 

**Success criteria**: All items use a correct method for counting; correct computations are set up and shown clearly; and all answers are correct except for no more than two simple errors. 



## Learning Target 13

> **(CORE)** I can compute factorials and binomial coefficients, and apply the these concepts to solve basic combinatorics problems. (permutations, selections, distributions)

1. Compute the values of each of the following, and show your steps: 

   (a) $8!$

   (b) $\displaystyle{\binom{30}{2}}$    

2. How many 4-element subsets containing the letter A can be formed from the set $\lbrace A, B, C, D, E, F, G \rbrace$?   An example of one such subset would be $\{A, B, F, G\}$, but not $\{A,B,G\}$ (because it doesn't have four elements) and not $\{C,D,E,F\}$ (because it doesn't contain "A"). 

**Success criteria**: Both parts of the first item are correct except for no more than one simple error. On the second part, a correct method for counting is used, correct computations are set up and shown clearly, and the answers are correct except for no more than one simple error. 



## :new: Learning Target 14

> I can determine if a sequence of numbers is arithmetic or geometric and derive both closed-form and recursive formulas for them.

Below are four integer sequences. Label each one as **arithmetic**, **geometric**, or **neither** (if the sequence is neither arithmetic nor geometric). If a sequence is either arithmetic or geometric. give both a closed formula and a complete recursive definition for the sequence. You do not need to show your work but your answers must be complete and correct. **Assume that the starting index is $0$.** 

1. $4, 3.9, 3.8, 3.7, \dots$
2. $1, 5, 25, 125, \dots$ 
3. $8, 6, 4, 2, \dots$
4. $$4, 8, 12, 20, 32, 52, \dots$$ 

**Success criteria**: All four sequences are correctly labelled. For sequences that are either geometric or arithmetic, a correct closed formula with a starting index of $n=0$ is given; and a complete and correct recursive definition is given. A *complete* recursive definition consists of a recurrence relation that correctly relates the current term to the previous term, *and* a correct initial condition. **Recursive definitions without the initial condition stated are not complete!** 



## Learning Target 15

> I can use the characteristic root method to find a closed-form solution for a first- or second-order linear homogeneous recurrence relation.

Consider the recurrence relation defined for $n \geq 2$:

$$a_n = -3a_{n-1} + 10 a_{n-2}$$

with initial conditions $a_0 = 2$  and $a_1 = 3$. **Note the negative sign in front of the 3.**

Solve the recurrence relation using the characteristic root method. **Show all your work! See the success criteria for details.** 



**Success criteria:**  *Every* step of the solution should be clearly shown and legibly written. **This includes solving equations and solving systems of linear equations**. Simpler mathematical steps such as adding two numbers, or factoring a polynomial do not need explanation. **The more detail you show, the more likely a successful attempt.** Finally, the closed-form solution for the recurrence relation must be clearly visible and put in a circle or a box. (You do not need to show work checking your solution, though it's not a bad idea to do so in your notes.)