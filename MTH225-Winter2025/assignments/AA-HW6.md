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
    - (b) $\overline{B \setminus A}$
    - (c) $A \cap \overline{B}$ 
    - (d) $\overline{A} \cup B$
    - (e) None of these 

3. The cardinality of the power set of $A = \lbrace 1,2,3,\dots 10\rbrace$ is 

    - (a) $0$ 
    - (b) $10$
    - (c) $50$ 
    - (d) $1024$
    - (e) None of these 

4. If $A = \lbrace 1,2,3,\dots 10\rbrace$ and $B = \lbrace 1,2,3 \rbrace$ then the cardinality of $A \times B$ is 

    - (a) $13$
    - (b) $30$
    - (c) $1000$
    - (d) $59049$
    - (e) None of these 

5. If $A$ \cap B = \emptyset$ then we say that $A$ and $B$ are 

    - (a) Empty 
    - (b) Disjoint
    - (c) Separate 
    - (d) Mutually exclusive
    - (e) None of these 

## Problems to solve 

As mentioned in class, your goal in MTH 225 isn't to *write* mathematical proofs but to *read* them for comprehension. These two problems will give you practice with that. They are completed proofs by induction, but there may be flaws in them, and those flaws might be minor or they might be serious. You're to read each and give a thorough critique. Specific instructions follow. 

1. Consider the proposition: **For all positive integers $n$, $11^n - 6$ is a multiple of $5$.** Here is a *proposed* proof by induction. (It's not a "real proof" until we verify that it's complete, clear, and correct.)

>**Proof:** We prove this with mathematical induction. So assume that for some positive integer $k$, $11^k - 6$ is a mulitple of $5$. We want to show that $11^{k+1} - 6$ is a multiple of $5$. Looking at $11^{k+1} - 6$, we can factor out an $11$ to get $11(11^k - 6)$. But, in the inductive hypothesis we assumed that $11^k-6$ is a multiple of $5$. Since $11^{k+1} - 6 = 11(11^k - 6)$ and the expression in parentheses is a multiple of $5$, it means that $11^{k+1} - 6$ is $11$ times a multiple of $5$, so therefore $11^{k+1} - 6$ is also a multiple of $5$. This is what we wanted to show, so the proposition is proven. 

What, if anything, is wrong with this proof? 

Possible responses include: 
- Nothing is wrong with this proof. 
- This proof has no major issues with being clear, correct, or complete but it does have one or more minor ones -- then you should list those and explain why they are issues, and why they are minor. 
- This proof has one or more major issues with being clear, correct, or complete -- then you should list those and explain why they are issues, and why they are major.


2. Consider the proposition: **For all positive integers $n$, $1 + 2 + 3 + \cdots + n = n$.** Here is a *proposed* proof by induction. 

>**Proof:** We will prove this with induction. The base case is when $n=1$, and in this case, on the left side of the equation we would just have the number $1$ because nothing else is being added; and on the right side we would have $1$ as well. Those are obviously equal so the base case holds. 
>
>Now assume that for some positive integer $k$, $1 + 2 + 3 + \cdots + k = k$. We want to show that $1 + 2 + 3 + \cdots + (k+1) = k+1$. Start from the induction hypothesis, where we have assumed that $1 + 2 + 3 + \cdots + k = k$. Add $k+1$ to both sides to get $1 + 2 + 3 + \cdots + k + (k+1) = k + (k+1)$. By the induction hypothesis, the first $k$ terms of the left side are just equal to $k$, so the left side becomes $k + (k+1)$. This equals the right hand side. Therefore we have proven that the sum holds when $n = k+1$, so the proposition is true. 

What, if anything, is wrong with this proof? 

Possible responses include: 
- Nothing is wrong with this proof. 
- This proof has no major issues with being clear, correct, or complete but it does have one or more minor ones -- then you should list those and explain why they are issues, and why they are minor. 
- This proof has one or more major issues with being clear, correct, or complete -- then you should list those and explain why they are issues, and why they are major.