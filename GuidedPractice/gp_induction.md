# MTH 325 Guided Practice: Induction Review


## Overview

We are about to transition into our next topic group on _graphs_ having just finished the unit on _recursion_. In the middle of these two topics is the all-important mathematical technique of _proof by induction_. You first saw (or should have seen) proofs using mathematical induction in MTH 225, but (1) it's been a few months since MTH 225 and (2) this topic is so important moving forward that it's worth taking a day to review. This one-day unit is considered part of the Recursion learning bundle, because there are natural connections -- as you will see -- between recursive algorithms and inductive proofs. 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ Determine when proof by mathematical induction would be a good choice for a proof technique. 
+ Determine the base case for a proof by induction, and prove the base case. 
+ State the induction hypothesis in a proof by mathematical induction. 
+ State the proposition that needs to be proven in a proof by mathematical induction, following the induction hypothesis. 
+ Explain how one might finish an induction proof, having proven the base case and assumed the induction hypothesis. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Write a complete and correct proof by mathematical induction for propositions arising from sums, recursive sequences, recurrence relations, or recursive algorithms. 

## Learning resources 

Since this is a review, it's recommended that you skip the resources at first and try the exercises, to see how much you remember and how fluent you are. If you are able to complete the exercises with little to no trouble, you may skim or even skip the resources. However if one or more particular points are giving you difficulty, stop work on those and come back to read and watch video. Continue by reading and watching as much as you need in order to get back up to speed. 

+ [The Traveler and the Strange Staircase](https://youtu.be/9LwAtbXSB3A) (3:18)
+ [Mathematical induction, part 1](https://www.youtube.com/watch?v=JTj6ID4-084) (5:22)
+ [Mathematical induction, part 2](https://www.youtube.com/watch?v=1H0gg3fMYVA) (6:16)
+ [Mathematical induction: Example with integer division](https://www.youtube.com/watch?v=ayX6PxB3z40&list=PL2419488168AE7001&index=55) (7:05)
+ [Mathematical induction: Example with inequality](https://www.youtube.com/watch?v=upzROTcbAnk&list=PL2419488168AE7001&index=56) (4:45)
+ [Mathematical induction: Example with calculus](https://www.youtube.com/watch?v=GQ9fUZxmN8I&list=PL2419488168AE7001&index=57) (8:27)
+ [The Extended Principle of Mathematical Induction](https://www.youtube.com/watch?v=9PMvJn-J608&list=PL2419488168AE7001&index=58) (9:16)
+ [Extended Principle of Mathematical Induction: Example from computational geometry](https://www.youtube.com/watch?v=Z9sYIWHIvNc&list=PL2419488168AE7001&index=59) (7:56)


## Exercises

Consider the following predicate $S(n)$, with the universal set being $\mathbb{P}$ (the set of all positive integers):

$$1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$$

1. Remember that $S(n)$ is a predicate, which means it does not have a truth value until you plug a number in for $n$. Is $S(1)$ true? Explain how you know. 
2. By hand, and not to be turned in, determine whether $S(2), S(3), \dots, S(10)$ are true. What do you think is the truth set for $S(n)$? Explain briefly. 
3. If we were to prove that $1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$ for all positive integers $n$, we might use induction. The first step is to prove the base case. What exactly do we need to show, in order to prove the base case? Be specific. 
4. If we were to prove that $1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$ for all positive integers $n$ using induction, what would be the induction hypothesis? Give a _precise_ statement of this induction hypothesis, including an important quantifier. 
5. If we were to prove that $1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$ for all positive integers $n$ using induction, once we've proven the base case and assumed the induction hypothesis, what do we now need to show? Give a _precise_ statement. 

## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1VFyfXr](http://bit.ly/1VFyfXr)