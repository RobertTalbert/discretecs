# Application/Analysis Homework 5

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 2**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

Application/Analysis Exam 1, scheduled for Friday February 21, will consist of problems taken verbatim from all the Application/Analysis Homework sets up to that point, including this one. So it is to your strong advantage to maximize your understanding of the problems and questions you find below --- you will see these on a test later.  


---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

Set up the framework for a proof by mathematical induction for each of the following propositions. See your class notes for what this involves. 

1. For all positive integers $n$, $11^n - 6$ is a multiple of $5$.
2. For all positive integers $n$, $1^2 + 2^2 + 3^3 + \cdots + n^2 = \dfrac{n(n+1)(2n+1)}{6}$$. 



 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

All of the multiple choice items refer to the following proposition that we might want to prove by mathematical induction: 

**For all integers $n \geq 4$, $n^2 \leq 2^n$.**

1. The predicate involved in this proposition is 
   - (a) $n^2$
   - (b) $2^n$ 
   - (c) $n^2 \leq 2^n$
   - (d) For all integers $n \geq 4$, $n^2 \leq 2^n$
   - (e) None of these  

2. The value of the variable that corresponds to the base case is 
   - (a) $n = 0$
   - (b) $n = 1$
   - (c) $n = 2$
   - (d) $n = 4$ 
   - (e) None of these 
  
3. To prove the base case, we would need to 
   - (a) Show by direct demonstration that $0^2$ is less than or equal to $2^0$
   - (b) Show by direct demonstration that $1^2$ is less than or equal to $2^1$
   - (c) Show by direct demonstration that $4^2$ is less than or equal to $2^4$
   - (d) Show by direct demonstration that $2^4$ is less than or equal to $4^2$
   - (e) None of these 

4. In the induction proof, the induction hypothesis would say 
   - (a) Assume $2^k$ for some integer $k$. 
   - (b) Assume $n^2$ for some integer $n$.
   - (c) Assume $k^2 \leq 2^k$ for some integer $k$. 
   - (d) Assume $(k+1)^2 \leq 2^{k+1}$ for some integer $k$
   - (e) None of these 

5. You might notice that if $n = 3$, the proposition isn't true, because the left side of the inequality is $3^2 = 9$ but the right side is $2^3 = 8$, and $9 \not \leq 8$. This means
   - (a) The proposition is false because it is not always true 
   - (b) The proposition is false because we have found a counterexample  
   - (c) The proposition is true because the example does not fall in the stated range of the variable
   - (d) Nothing, because the proposition does not claim to be true when $n = 3$ 
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


1. Consider the proposition: *For all positive integers $n$, $1 + 2 + 3 + \cdots + n = n$.* Here is a *proposed* proof by induction. 

>**Proof:** We will prove this with induction. The base case is when $n=1$, and in this case, on the left side of the equation we would just have the number $1$ because nothing else is being added; and on the right side we would have $1$ as well. Those are obviously equal so the base case holds. 
>
>Now assume that for some positive integer $k$, $1 + 2 + 3 + \cdots + k = k$. We want to show that $1 + 2 + 3 + \cdots + (k+1) = k+1$. Start from the induction hypothesis, where we have assumed that $1 + 2 + 3 + \cdots + k = k$. Add $k+1$ to both sides to get $1 + 2 + 3 + \cdots + k + (k+1) = k + (k+1)$. By the induction hypothesis, the first $k$ terms of the left side are just equal to $k$, so the left side becomes $k + (k+1)$. This equals the right hand side. Therefore we have proven that the sum holds when $n = k+1$, so the proposition is true. 

What, if anything, is wrong with this proof? 

Possible responses include: 
- Nothing is wrong with this proof. 
- This proof has no major issues with being clear, correct, or complete but it does have one or more minor ones -- then you should list those and explain why they are issues, and why they are minor. 
- This proof has one or more major issues with being clear, correct, or complete -- then you should list those and explain why they are issues, and why they are major.