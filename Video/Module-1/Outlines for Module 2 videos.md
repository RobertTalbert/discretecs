# Outlines for Module 2 videos 

## 2.1 What is a logical proposition

- Humans communicate with each other using language. Computers don't. How do we communicate with computers? 
- Through LOGIC -- reasoning that uses strict rules of validity
- Start with statements whose validity can be judged: Propositions
  - A complete sentence (verbal or mathematical) that has a definite and knowable truth value 
  - Examples: verbal and math
  - Non examples
    - Interjections
    - Opinions
    - Incomplete thoughts
    - Underdetermined statements 
- Practice: ID the propositions and non-propositions



## 2.2 AND, OR, and NOT

- Two kinds of propositions: 
  - Atomic 
  - Compound or "molecular" -- atomic statements joined by connectives
- The truth value of the molecular statement is determined by the truth values of its atomic statements and what kind of connective is being used. 
- Example: "this course requires both algebra and intro to python as prerequisites" vs "this course requires either algebra or intro to python as prerequisites" 
- AND (conjunction): A ^ B is true whenever A and B are both true, false otherwise. 
- OR (disjunction): A v B is true if either A or B or both are true, false otherwise ("inclusive or") 
- NOT (negation): ~A is true if A is false, ~A is false when A is true
- Examples (including code) 

## 2.3 Conditional statements 

- If-then statements -- they are everywhere -- another kind of connective 
- Conditional statement
  - Hypothesis 
  - Conclusion
- When is a CS true? 
  - When is a CS FALSE? -- Like a broken promise -- happens when the hypothesis is true and the conclusion is false
  - CS is true in ALL OTHER CASES
  - The truth table for a CS 
- Why isn't the CS false if the hypothesis is false?
  - That would mean that the promise is broken, but that's not always the case
  - Example: If 


## 2.4 Variations on conditional statements

- If A, then B 
- Converse: If B, then A
- Contrapositive: If not B, then not A
- Inverse: If not A, then not B
- Do they all mean the same? Look at "If it's raining, then it's cloudy"  (pause the video etc.) 
  - Converse; If it's cloudy then it;s raining
  - Contrapositive: If it's not cloudy then it's not raining
  - Inverse: If it's not raining then it's not cloudy
  - The original and the contrapositive both seem true. The converse and inverse don't. So converse and inverse are not "logically the same as" the original but the contrapositive might be. 

## 2.5 Truth tables for the basic connectives

- What is a truth table
- Truth table for AND
- OR
- NOT
- If, then
- Contrapositive 
- Converse 
- The concept of logical equivalence -- the converse is not logically equivalent to P -> Q but the contrapositive is 

## 2.6 Truth tables for more complex propositions

- General method for making truth tables 
  - Identify the atomic statements 
  - Convert the molecular statements into atomic with connectives 
  - Create rows for truth combinations: two variables = 4 rows, three variables = 8 rows, four variables = 16 rows etc. 
  - Work from the smallest combinations to the largest ones -- use a column for each one 
  - One column should hold the main proposition
- Example with two variables
- Example with three variables 

## 2.7 Logical equivalence 

(Two examples of using a truth table to determine logical equivalence of complex statements, one with two variables and another with three)

## 2.8 Predicates 

- Example: "x is an even number"
	- Not a proposition because the truth value can't be determined without x. It's true for some x and false for others. 
	- An example of a **predicate**
	- Predicates have **variables** that come from a particular **domain**. For example "x is an even number" has a variable (x) and it only makes sense if x is an integer. 
	- And the predicate takes on a truth value when a particular value of the variable is given. 
	- For example, if x = 2, the predicate is now the proposition "2 is an even number" which is true. If x = 5, the predicate is now the proposition "5 is an even number" which is false. 
- So predicates are like tiny little computer programs where you put in data of a certain type, and the output is a Boolean value TRUE or FALSE. More formally, a predicate is a *function* from a set into the set containing the two values TRUE or FALSE. Will talk more about functions later. 
- Other examples
	- "The length of S is 10"
	- The variable is S. The domain is all strings. 
	- Like this Python program: 
```python
def string_is_ten(S):
	return len(S) == 10
```
- We sometimes use program- or function-style notation for predicates, for example $P(x) =$ "x is an even number" 
- Another example 
	- P(A) = "Prof. A has a beard" 
	- Variable is "A", domain -- depends, needs to be specified. "Profs in the GVSU math department". 
	- Sometimes true, sometimes false. 
- Another
	- $P(x,y) = "xy > 0"$, where x,y are any real numbers. 
	- This one has two variables. Unless we know values for both x and y, there's not enough info to know true/false -- we say it's underdetermined. 
	- Domain is the set of real numbers. 
	- $P(-1, -2)$ is true. $P(-1, 10)$ is false. 
- Predicates can be true for EVERY value, for example $P(n) = n^2 + 1 > 0$ is true for all $n$. But other times predicates are true sometimes but not always 
- TRUTH SET of a predicate is the collection of input values that makes the predicate true. For example: 
	- Truth set of P(x) =$ "x is an even number" is $x = 0, \pm 2, \pm 4,$, etc. 
	- Truth set of P(A) is these guys
	- Truth set of $P(x,y) = "xy > 0"$ is the set of all x,y pairs that have the same signs
- What you learned

## 2.9 Quantification 

## 2.10 Double quantification and negation 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNzg0NTIyMzddfQ==
-->