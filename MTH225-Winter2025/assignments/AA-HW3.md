# Application/Analysis Homework 3

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 2**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

Application/Analysis Exam 1, scheduled for Friday February 21, will consist of problems taken verbatim from all the Application/Analysis Homework sets up to that point, including this one. So it is to your strong advantage to maximize your understanding of the problems and questions you find below --- you will see these on a test later.  


---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. Use truth tables to determine whether each pair of statements below is logically equivalent. 
- (a) $p \rightarrow q$ and $(\neg p) \vee q$ 
- (b) $\neg(p \wedge q)$ and $(\neg p) \vee (\neg q)$ 
- (c) $(p \rightarrow r) \wedge (q \rightarrow r)$ and $(p \wedge q) \rightarrow r$

1. Use a truth table to show that the following argument is valid: 
   - Premises: $p \rightarrow q$ and $q \rightarrow r$
   - Conclusion: $p \rightarrow r$ 

This rule of reasoning is called **hypothetical syllogism** in logic. 


 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

1. The number of rows (other than the header) in a truth table for a proposition that uses six different variables is
- A) 6
- B) 12
- C) 36
- D) 64

2. If two propositions are logically equivalent, it means that 
- A) Every row in a truth table containing those propositions is "True"  
- B) Each proposition has the same number of "True" rows as it does "False" rows
- C) The first proposition is "True" the same number of times that the second proposition is "True" 
- D) The first proposition is "True" whenever the second proposition is "True" 

3. Which of the following is NOT logically equivalent to the proposition $A \rightarrow (\neg B)$? 
- A) $B \rightarrow (\neg A)$ 
- B) $(\neg A) \vee B$
- C) $\neg(A \wedge B)$ 
- D) $\neg(A \vee B)$ 

4. If a logical argument is valid, it means that
- A) The conclusion is never False 
- B) The premises are never all False at the same time
- C) The conclusion is True in all cases where the premises are all True
- D) There is at least one condition where all the premises are True and the conclusion is True

5. Consider a logical argument whose premises are $P \rightarrow Q$ and $\neg Q$. Which of the following conclusions would result in the argument being valid? 
- A) $P$
- B) $Q$ 
- C) $\neg P$
- D) $Q \vee P$


## Problems to solve 

1. In Application/Analysis Homework 2, we introduced a new connective called the **biconditional** and you were asked to build a truth table for it. You can click here for the solutions to that assignment where it shows the correct truth table. Use this table to show that $P \leftrightarrow Q$ is logically equivalent to each of the following: 
- (a) $(\neg P) \leftrightarrow (\neg Q)$ 
- (b) $(P \wedge Q) \vee ((\neg P) \wedge (\neg Q))$ 


2. Logic is full of useful frameworks for valid reasoning that you can apply in everyday life to think carefully about just about anything, and they have special names so you can refer to them. A few that we have seen in the class are: 

| Name | Premises | Conclusion | Example | 
| --- | ----- | ----- | ---- | 
| *Modus ponens* | $p$, and $p \rightarrow q$ | $q$ | If it rains, I get wet. It's raining. So I'm geting wet. | 
| *Modus tollens* | $\neg q$, and $p \rightarrow q$ | $\neg p$ | If it rains, I get wet. I'm not wet. So it's not raining. | 
| Hypothetical syllogism (see practice exercises) | $p \rightarrow q$ and $q \rightarrow r$ | $p \rightarrow r$ | If it rains, I get wet. If I get wet, I'll need to change clothes. So, if it rains I'll need to change clothes. | 

Here are a few more common rules for deduction. Use truth tables to show each one is valid. Then, state an English example for each. 

- (a) **Disjunctive syllogism**: Premises are $p \vee q$ and $\neg p$; conclusion is $q$. 
- (b) **Addition:** Premise is $p$; conclusion is $p \vee q$. 
- (c) **Simplification:** Premise is $p \wedge q$; conclusion is $p$. 
- (d) **Resolution:** Premises are $p \vee q$ and $(\neg p) \vee r$; conclusion is $q \vee r$. 

3. Logic also helps us to catch *invalid* reasoning and call it out by name. Forms of invalid reasoning are called **fallacies**. Use truth tables to show each one is invalid. Then, state an English example for each fallacy.  

- (a) **Affirming the conclusion:** Premises are $p \rightarrow q$ and $q$; conclusion is $p$. 
- (b) **Denying the hypothesis:** Premises are $p \rightarrow q$ and $\neg p$; conclusion is $\neg q$.   