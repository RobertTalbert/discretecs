# Standards for Student Work in MTH 225

## About this document

**This document contains all the details of what you will be asked to do on different assessments in the course, and what constitutes "successful" work on each task**. You should consider this document to be of equal importance as the [Syllabus](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/MTH%20225%20Winter%202025%20Syllabus.md) and [calendar](https://calendar.google.com/calendar/embed?src=00101de093246cb4a426b788997bab104cf4fd5a056846f4df83532449b477dc%40group.calendar.google.com&ctz=America%2FDetroitt) in terms of guiding your progress in the course. Study it carefully and refer to it each time before submitting an assignment, to ensure you're giving your best effort and to minimize the number of revisions and resubmissions you will do.


---

## Ground Rules for all work in MTH 225

Unless otherwise stated on the assignment, every assignment in MTH 225 operates under the following guidelines: 

- **It is not enough just to give a correct answer to a problem**: You must also give a clear, correct, and complete explanation. (There are some exceptions, for example multiple choice items on homework and exams typically don't require explanations.)
- **The target audience for your explanations is your classmates**. Your explanation should allow a person who has the same level of training and background as you -- but who has no familiarity with the problem you are solving -- to follow your solution from beginning to end and agree with your answer, without having to do much or any extra work. If your explanation skips steps; or simply asserts that something is true rather than explains why; or uses language that is unclear or hard to follow; or is disorganized or illogical; or other such things, you'll probably be asked to revise and resubmit. 
- **Solutions to problems should generally be free of any significant errors, and you should try to submit work that is totally free of these.** The next section below goes into detail about what is considered an "error". 
- **On the other hand, minor errors are typically ignored as long as there are not too many of them.** Again, the next section below explains what a "minor error" is and gives examples.  

## What is an "error" and what is a "minor error" 

An **error** in a submission is **anything that brings your mastery of the core concepts of the work into question**. And, the ultimate question asked of any work you submit is: **Does the submission show sufficient mastery of the concepts and processes that the assignment focuses on?** Your goal in every item of work you submit for grading is to **show clear evidence that you have mastered the concepts and processes in the assignment**. 

**This goes beyond simply having "right answers" or "wrong answers"**. Sometimes a wrong answer to a problem might be wrong for reasons unrelated to the core ideas of the problem, and your grasp of the core concepts is still evident; on the flip side, a submission might have a right answer but the means by which you got that right answer does not show evidence of mastery of the core concepts. And in some cases a problem may not even have a single right or wrong answer. 

There are four main kinds of errors that can happen in your work: 

1. *Computational errors*. This is when you simply make a mistake in computing something, like adding $5+3$ and getting $9$. 
2. *Logical errors*. This is when you draw incorrect conclusions from data. For example, if you know that there are 10 computer science majors in a class and 5 math majors, and conclude that there are $10+5=15$ students that are either math or computer science majors. This is a logical error because it doesn't take double-majors into account. (We'll study this, as the [Principle of Inclusion and Exclusion](https://publish.obsidian.md/discretecs/Combinatorics/Principle+of+Inclusion+and+Exclusion).)
3. *Factual errors*. This results from misstating definitions, theorems, steps of an algorithm, or parameters in a problem statement. For example, if you are using the formula for the [Binomial Coefficient](https://publish.obsidian.md/discretecs/Combinatorics/Binomial+coefficient) and leave off one of the terms in the denominator, that's a factual error. Or, if a problem states that there are 100 objects that need to be sorted but you mis-copy the problem and write down 10 objects instead, that's a factual error. **Many errors in MTH 325 result from incorrectly reading or copying down information. These errors are easy to avoid, simply by slowing down and double-checking your steps.**
4. *Semantic errors*. This happens when you make a statement that is grammatically correct, but the statement itself has no meaning. For example the statement "*MTH 325 is a very purple unicorn*" obeys the rules of the English language, but it makes no sense. The same is true of the statement, "*The function of the set is 3*" because the phrase "the function of the set" has no meaning (there is no such thing). Semantic errors can be hard for those learning the subject to catch before making them. They will be politely pointed out in your feedback to help you spot and correct them. 


**Errors in your work can be either "significant" or "minor":** 

- A **significant** error is one that pertains directly to the core concepts of the problem or assignment and calls your understanding and mastery of those concepts into question. 
- On the other hand a **minor** error is one that does not pertain directly to the core concepts of the problem or assignment, and your understanding and master of those concepts is still evident despite the error. 

Whether an error is significant or minor, is a judgment call made by me (Talbert) in the context of the problem using my professional expertise. (Please note, all grading consists of those kinds of judgment calls.) 

## Examples of different kinds and levels of error

Here are some examples of different ways that errors can occur on a single problem. The problem is an instance of Learning Target 1: 

> Let $x = 1000$ and $y = 13$. (a) Find the quotient and remainder when dividing $x$ by $y$. (b) Use the Euclidean algorithm to find the greatest common divisor of $x$ and $y$. (c) State the value of `x % y`. 

For reference, here is a solution to this problem that would be marked *Success*. 

(b) 


Here are some examples of both significant and minor errors in each of the four types of error discussed above, in the context of different Learning Targets.

| Kind of error | Example of a minor error                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Example of a significant error                                                                                                                                                                                                                                                                                                                                                                          |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Computational | **In the last step of part (a), computing $90-78$ and getting $2$ instead of 12 due to a subtraction error,** and then stating that the quotient is 78 and the remainder is 2. This is a minor error because the core idea in part (a) is using long division to find the quotient and remainder and then labelling them correctly. A single subtraction error doesn't cast doubt on the student's grasp of that idea (but several errors might).                                           | In the last step of part (a), **getting a remainder of 12, but then stating that the remainder is 78 and the quotient is 12** (instead of the other way around). This is significant because knowing the difference between quotient and remainder is a core concept in this target; confusing them calls mastery of this into question.                                                                |
| Logical       | In part (a), **switching $x$ and $y$ so that we are dividing 13 by 1000 instead of the other way around**, and then doing correct work to get a quotient of 0 and a remainder of 13. This stems from misunderstanding the order of operations in "divide $x$ by $y$" (it might also be a "factual" error due to miscopying) and as long as the process is done correctly on this new version of the problem, it could be considered minor. (However -- see below about oversimplification.) | In part (b), doing all the Euclidean Algorithm work correctly and then **concluding that the GCD of 1000 and 13 is 0,** because that is the last remainder in the sequence of calculations. That's the incorrect conclusion to draw from the work (which is done correctly) and casts doubt on the student's understanding of the algorithm.                                                            |
| Factual       | **Getting the remainder wrong in part (a) but using that remainder as the answer in part (c).** The core concept of part (c) is knowing that `1000 % 13` is the remainder when dividing 1000 by 13. If the answer in (a) is wrong, demonstrating understanding of this concept in (c) is still possible. The answer is wrong, in other words, but it's because of another error "upstream" from it and there is actually no factual error at all here.                                      | Having the quotient and remainder right in part (a) but then **using the quotient (78) as the answer in part (c) instead of the remainder**. (That is, stating `1000 % 13 = 78`.) This is significant because it shows misunderstanding of the definition of `a % b`.                                                                                                                                   |
| Semantic      | In part (b), **stating: "The GCD of the two numbers is either GCD(1000) or GCD(13), whichever is greater" but then going on to use the Euclidean Algorithm correctly and getting a correct answer**. The statement in quotes is nonsense; but it does not impact the main idea of the solution so it's considered "minor" (since it can just be ignored).                                                                                                                                   | In part (b), **stating that the GCD of the two numbers is both 500 and 1**, with the reasoning that the largest number that divides 1000 is 500 and the largest number that divides 13 is 1. It doesn't make semantic sense for the GCD of two integers to be anything other than a single number. Not only is the answer wrong, it's not clear that the student really understands the concept of GCD. |

Please note, **an error that results in an oversimplified version of the problem is considered "significant"**. For example, if a student mis-copied the problem above to have $y=1$ instead of $y = 13$, then this copy error drastically oversimplifies the problem, to the extent that it's no longer evident from correct work that the concepts and processes have been mastered. On the other hand, mis-copying the problem to have $y=31$ of $y=13$, is an error, but it does not make the rest of the problem any easier, so *Success*-ful work is still possible. 



---


## Standards for Class Prep and Application/Analysis homework assignments

Class Prep and Application/Analysis Homework assignments (not to be confused with Application/Analysis exams) are graded solely on the basis of **completeness and effort**. Errors of any type or any level of severity are not taken into account. Instead, to earn a *Success* mark


## Standards for Application/Analysis exams

## Standards for Learning Targets


