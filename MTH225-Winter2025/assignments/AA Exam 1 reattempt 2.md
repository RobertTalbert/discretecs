# Application/Analysis Exam 1 Reattempt 2

**Instructions -- Read Carefully**

1. Please reattempt only the sections that you need to reattempt from the original Exam 2. Those sections are listed on the paper copy of Exam 2. Your work is available for pickup at the beginning of this exam session. 
2. Please do not use any resources other than a graphing or scientific calculator, and a pen or pencil. 
3. Please do all work in the spaces provided. 
4. Instructions for individual sections are provided in the exam.

## Multiple Choice

For each of the questions in this part, circle the letter of the one response that you believe is most correct. 

1. The quantity `a % b` represents 
   - (a) The quotient obtained when dividing $a$ by $b$
   - (b) The quotient obtained when dividing $b$ by $a$
   - (c) The remainder obtained when dividing $a$ by $b$
   - (d) The remainder obtained when dividing $b$ by $a$
   - (e) None of these

2. If two propositions are logically equivalent, it means that 
    - (a) They have the same number of variables
    - (b) They have the same number of "True" entries in their truth tables
    - (c) They have the same truth values for every possible combination of truth values of their variables
    - (d) They are both always True
    - (e) None of these 

3. What is the negation of the statement "If it rains, then the ground is wet"?
   - (a) If it rains, then the ground is not wet
   - (b) If it does not rain, then the ground is wet
   - (c) It rains and the ground is not wet
   - (d) It does not rain and the ground is wet
   - (e) None of these

4. What is the negation of the statement "Every student in this class is a math major"?
   - (a) No student in this class is a math major
   - (b) Some student in this class is not a math major
   - (c) Every student in this class is not a math major
   - (d) Some student in this class is a math major
   - (e) None of these

   <div style="page-break-after: always;"></div>
   
5. The statement "If $x$ is a real number, then $x^2 \geq 0$" is        
   - (a) True for all real numbers $x$
   - (b) True for some real numbers $x$
   - (c) False for all real numbers $x$
   - (d) False for some real numbers $x$
   - (e) Both (b) and (d)

6. The statement $P \land Q$ is known as 
   - (a) A conjunction
   - (b) A disjunction
   - (c) An implication
   - (d) A biconditional
   - (e) None of these

7. Consider the proposition: For all integers $n \geq 4$, $n^2 \leq 2^n$. Suppose we wanted to prove this using mathematical induction. To prove the base case, we would need to
   - (a) Show that the statement is true for $n = 0$
   - (b) Show that the statement is true for $n = 1$
   - (c) Show that the statement is true for $n = 4$
   - (d) Show that the statement is true for $n = 16$
   - (e) None of these

8. The number of rows (other than the header) in a truth table for a proposition with 6 variables is
   - (a) 6
   - (b) 12
   - (c) 24
   - (d) 64
   - (e) None of these

9. The greatest common divisor of $12$ and $18$ is
   - (a) 2
   - (b) 3
   - (c) 6
   - (d) 12
   - (e) None of these

10. To use the base conversion algorithm to convert the number $123$ from decimal to binary, we would first divide $123$ by
    - (a) 2
    - (b) 8
    - (c) 10
    - (d) 16
    - (e) None of these

<div style="page-break-after: always;"></div>

## Problem Group 1

Do EXACTLY ONE of the following problems. If you do the first one, you need to do both parts. Turning in work on both problems will result in the entire group being discarded. **Do not merely give an answer, or just the setup for a calculation followed by an answer, but a complete explanation for your approach, in clear English written in complete sentences that explains why your solution is correct.** Any solution that is not accompanied by such an explanation will not be considered a successful attempt. 

1.	Convert the number 483726 from base 10 to base 36 using the base conversion algorithm. For symbols, use ordinary 0-9 for zero through nine, then lower case letters a through z for 10 through 35. 
2.	Using the “repeated squaring” algorithm from Application/Analysis Homework 2, find the last two digits of the number $7^{89}$ . The number 89 in binary form is 1011001. 

<div style="page-break-after: always;"></div>

## Problem Group 2

1. Below is a recursive Python function that finds the maximum value of a list of real numbers. The input `lst` is a Python list of real numbers. Recall that if `lst` is a list then `lst[1:]` is the list that contains all the elements of `lst` except the first one, and `lst[0]` is the first element of the list. Manually work through this code to find the maximum value of the list `lst = [3, 5, 2, 8, 1]`. Show your work in detail. 

```python
def recursive_max(lst):
    if len(lst) == 1:
        return lst[0]
    else:
        sub_max = recursive_max(lst[1:])
        return lst[0] if lst[0] > sub_max else sub_max
```

2. Consider the proposition: For all integers $n \geq 4$, $n^2 \leq 2^n$. Below is a proposed proof of this statement by mathematical induction. What, if anything, is wrong with this proof? If there are no major issues, say so. If there are no major issues but it does have one or more minor ones, then list those and explain why they are issues, and why they are minor. If there are major issues with being clear, correct, or complete, then list those and explain why they are issues, and why they are major.

>**Proof:** For the base case, note that $4^2 = 16 \leq 2^4 = 16$. Now assume that for some integer $k$, $k^2 \leq 2^k$. We want to show that $k^2 + 1 \leq 2^{k+1}$. Start with the inequality $k^2 \leq 2^k$ from the induction hypothesis. Adding $1$ to both sides gives $k^2 + 1 \leq 2^k + 1$. Now $1 < 2$, so $2^k + 1 < 2^k + 2$. But on the right, $2^k + 2 = 2^k + 2^1 = 2^{k+1}$. Putting all this together we have that $k^2 + 1 \leq 2^k + 1 \leq 2^k + 2 = 2^{k+1}$. Therefore $k^2 + 1 \leq 2^{k+1}$ which is what we wanted to prove. 

<div style="page-break-after: always;"></div>

## Problem Group 3

1. 	Use a truth table to determine whether the following argument is valid or invalid: The premises are $p \land q$ and $(\neg p) \land r$, and the conclusion is $q \lor r$. Be sure to clearly state whether the argument is valid or invalid, and how you know this from the truth table. 
2. In computer science there are two logical operators used frequently in circuits: $NAND$ and $NOR$. The proposition $p \ NAND \ q$ is true when either $p$ or $q$, or both, are false, and it is false when both $p$ and $q$ are true. The proposition $p \ NOR \ q$ is true when both $p$ and $q$ are false, and it is false when either $p$ or $q$, or both, are true. 
   - (a) Construct a truth table for $p \ NAND \ q$ and for $p \ NOR \ q$. 
   - (b) Use a truth table to show that $p \ NAND \ q$ is logically equivalent to $\neg (p \land q)$, and that $p \ NOR \ q$ is logically equivalent to $\neg (p \lor q)$.

<div style="page-break-after: always;"></div>



### This page intentionally left blank for overflow space