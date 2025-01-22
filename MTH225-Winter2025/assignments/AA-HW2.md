# Application/Analysis Homework 2

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 2**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

Application/Analysis Exam 1, scheduled for Friday February 21, will consist of problems taken verbatim from all the Application/Analysis Homework sets up to that point, including this one. So it is to your strong advantage to maximize your understanding of the problems and questions you find below --- you will see these on a test later.  


---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. For each of the following, state the hypothesis and conclusion, the converse, the contrapositive, and the negation. 
- If it's raining, take your umbrella.
- When the temperature drops below freezing, turn on the car heater.
- If you have more than 5 unread emails, set aside 30 minutes to process them.
- When someone sends you a question, read it twice before responding.
- If a meeting runs over time, send a quick update to your next appointment.

2. Write truth tables for each of the following: 
   - (a) $P \wedge (P \vee (\neg Q))$
   - (b) $(P \vee Q) \rightarrow (\neg R)$ 

 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

1. Which of the following is a logical proposition?
- A) 5 + 3 = 8
- B) What time is it?
- C) Please close the door.
- D) x + 2 = 10

2. Which logical connective is used to denote "and"?
- A) ∨ 
- B) ⇒ 
- C) ∧ 
- D) ¬ 

3. In a conditional statement "If p, then q", what is p called?
- A) Conclusion
- B) Hypothesis
- C) Consequent
- D) Proposition

4. What is the truth value of the expression p ∧ q when p is false and q is true?
- A) True
- B) False
- C) Undefined
- D) True only if q is true

5. Consider the truth values of p and q in the following truth table:

| p     | q     | p ∨ q |
|-------|-------|-------|
| True  | True  |       |
| True  | False |       |
| False | True  |       |
| False | False |       |

What are the missing values in the p ∨ q column?
- A) True, True, True, False
- B) True, False, True, False
- C) True, True, False, False
- D) True, True, True, True



## Problems to solve 

1. One logical connective that we did not cover directly in class is called the **biconditional**. This connective uses a double-headed arrow to notate it: $P \leftrightarrow Q$, and this is pronounced "$P$ if and only if $Q$". We didn't cover it because it can actually be expressed in terms of simpler connectives. Namely, the statement $P \leftrightarrow Q$ means the same thing as: $(P \rightarrow Q) \wedge (Q \rightarrow P)$. In this problem, **make a truth table for $P \leftrightarrow Q$**, showing all intermediate columns as well as the final column. Then, in an English sentence, state the conditions under which $P \leftrightarrow Q$ is true and the conditions under which it is false. 

2. (*This problem goes back to earlier material on integer representation*.) An operation done on a computer very frequently is **raising a number to a large power mod another integer**, for example $2^{100000000} \,  \% \, 1000$. (For example, encrypting data using the RSA encryption system involves taking a medium-sized integer (3-6 decimal digits) and raising to a power that can be in the thousands of decimal digits in length, then reducing modulo another large integer.) Computers *do not* do this by first finding the power, then applying the modulus function because the power is far too large for memory. Instead, they use the following algorithm. Here, we are raising $a$ to the $b$ power ($a^b$), and finding the result mod $n$. 
 
   - Convert $b$ from decimal to binary. 
   - Use the binary to write $b$ in base 10 as a sum of powers of 2. 
   - Replace $b$ in the exponent of $a^b$ with this sum. 
   - Use basic exponent rules from high school algebra to rewrite $a^b$ as a *product* of copies of $a$ raised to powers of 2. 
   - Compute each power modulo $n$ separately. 
   - Then multiply the results back together and reduce mod $n$. 

The operation in the next to last point, computing the powers separately, can be done by **repeated squaring**. [Here is a video example showing a complete walkthrough](https://gvsu.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=7c542261-4957-4bd6-8f85-b26d01244f9e) of computing $3^{671} \, \% \, 5$. Notice that the numbers involved never get larger than two digits, so the computation is very fast. [Here is another example](https://www.youtube.com/watch?v=EHUgNLN8F1Y). If you do a search for "fast exponentiation", "modular exponentiation", or "repeated squaring" you can get more. 

**In this problem:** Take your birthdate and write it in year-month-day form. For example if you were born on February 1, 2005 then write it as 2005-2-1. (Don't pad the day and month with zeroes, like 2005-02-01.) Now remove the hyphens to get an integer that is between 6 and 10 digits (for example, 200521). Call this number $b$ (for "birthdate").Then **use this exponentiation algorithm to find the last two digits** (that is, the tens and ones digit) **of $7^b$.** Show all your steps and clearly indicate your answer. 