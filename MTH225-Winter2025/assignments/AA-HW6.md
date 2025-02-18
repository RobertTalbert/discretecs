# Application/Analysis Homework 6

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 2**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

Find the domain and the range (not the codomain) of the following functions: 

1. The function that assigns to each nonnegative integer its last digit. 
2. The function that assigns the next largest integer to a positive integer. 
3. The function that assigns to a bit string the number of `1` bits in the string

For practice involving basic concepts of sets and set operations, you are referred to the WebWorK online homework set. 

 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

1. Consider the function $f: \mathbb{N} \rightarrow \mathbb{N}$ that takes a natural number as input and returns the digit that is in the ones place. This function is 

    - (a) Neither injective nor surjective 
    - (b) Injective, but not surjective 
    - (c) Surjective, but not injective
    - (d) Bijective
    - (e) None of these 

2. If $A$ and $B$ are any two sets, then the set $A \ B$ is equal to 

    - (a) $B \setminus A$ 
    - (b) $\overline{B \setminus A}$ (Note: The bar should go over the entire set $B \setminus A$.)
    - (c) $A \cap \overline{B}$ 
    - (d) $\overline{A} \cup B$
    - (e) None of these 

3. The cardinality of the power set of $A = \lbrace 1,2,3,\dots 10\rbrace$ is 

    - (a) $0$ 
    - (b) $10$
    - (c) $50$ 
    - (d) $1024$
    - (e) None of these 

4. If $A = \lbrace 1,2,3,\dots, 10\rbrace$ and $B = \lbrace 1,2,3 \rbrace$ then the cardinality of $A \times B$ is 

    - (a) $13$
    - (b) $30$
    - (c) $1000$
    - (d) $59049$
    - (e) None of these 

5. If $A \cap B = \emptyset$ then we say that $A$ and $B$ are 

    - (a) Empty 
    - (b) Disjoint
    - (c) Separate 
    - (d) Mutually exclusive
    - (e) None of these 

## Problems to solve 

1. When we claim that two sets are equal, that equality is called a **set identity**. For example, one common set identity says that for any three sets $A, B$ and $C$, we have $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$. To establish that a set identity is true requires a **proof** and one simple way to prove an identity is through what's called a **membership table**. This is like a truth table, and it's constructed like this: Look at the identity and consider all the individual sets involved in it. Then, make a table with one row for each combination of sets that an element can belong to and verify that that the elements in the same combinations of sets belong in both the set on the left of the identity and the set on the right. To indicate that an element is in a set, use a `1`, and if an element is not in a set, use a `0`. Here is a membership table for the identity $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$; here is a video showing how it was made and why it proves that $A \cap (B \cup C)$ equals $(A \cap B) \cup (A \cap C)$. 

| $A$ | $B$ | $C$ | $B \cup C$ | $A \cap (B \cup C)$ | $A \cap B$ | $A \cap C$ | $(A \cap B) \cup (A \cap C$) |
| --- | --- | --- | ---------- | ------------------- | ---------- | ---------- | ---------------------------- |
| 1   | 1   | 1   | 1          | 1                   | 1          | 1          | 1                            |
| 1   | 1   | 0   | 1          | 1                   | 1          | 0          | 1                            |
| 1   | 0   | 1   | 1          | 1                   | 0          | 1          | 1                            |
| 1   | 0   | 0   | 0          | 0                   | 0          | 0          | 0                            |
| 0   | 1   | 1   | 1          | 0                   | 0          | 0          | 0                            |
| 0   | 1   | 0   | 1          | 0                   | 0          | 0          | 0                            |
| 0   | 0   | 1   | 1          | 0                   | 0          | 0          | 0                            |
| 0   | 0   | 0   | 0          | 0                   | 0          | 0          | 0                            |

**In this problem**: Use a membership table to prove the following set identities. Just as with truth tables, be sure to show all the intermediate columns. 

- (a) $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$ 
- (b) $\overline{A \cap B} = \overline{A} \cup \overline{B}$ (Note: On the left the bar should go over the entire set $A \cap B$.) 

2. Recall that $\mathbb{N} = \lbrace 0, 1, 2, 3, \dots \rbrace$. (Note, due to formatting limitations this may not look like the "N" we normally use for this set.)
   - (a) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is injective, but not surjective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is injective and how you know that it is not surjective. 
   - (b) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is surjective, but not injective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is surjective and how you know that it is not injective. 
   - (c) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is both injective and surjective, but not just the "identity" function that maps every number to itself. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function both injective and surjective. 
   - (c=d) Give an example of a function from $\mathbb{N}$ to $\mathbb{N}$ that is neither injective nor surjective. State explicitly how your function works (through a formula, a verbal description, diagram, etc.) and then explain how you know that the function is not injective and how you know that it is not surjective. 

