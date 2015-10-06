# MTH 325 Guided Practice 8.3b: Solving Linear Recurrence Relations

## Overview

In the previous lesson, we learned about recurrence relations, what a solution to a recurrence relation looks like, and how to verify whether a given closed-form expression is or is not a solution to a recurrence relation. The next step is to __find__ a closed form solution to a recurrence relation. We will do so using a technique that involves converting a recurrence relation into a polynomial (the _characteristic polynomial_) then using algebra to find its roots. 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ Identify when a recurrence relation is homogenenous versus non-homogeneous.
+ Write the characteristic polynomial and characteristic equation for a linear recurrence relation. 
+ Find the roots of the characteristic polynomial: by hand in simple cases, and using a computer in more complicated cases. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Given a homogeneous linear recurrence relation, use Algorithm 8.3.1 to find a closed-form solution. 

## Learning resources 

To gain proficiency in the learning objectives, use the following resources. You may include other resources if you wish, in addition to or in replacement of the following. 

__Textbook__: In _Applied Discrete Structures_, read in Section 8.3 from the subsection ``Solving Recurrence Relations'' through Example 8.3.9. Make sure to read actively, working through examples and activities as you go. Warning: The book's exposition here is not clear! 

__Video__: Watch the following videos:

+ [Linear homogeneous recurrence relations](http://www.youtube.com/watch?v=bSBg9V2tZ3I)(8:32)
+ [Solving linear homogeneous recurrence relations](https://www.youtube.com/watch?v=_u4GzKH5e0U) (8:13)
+ [Solving linear recurrence relations part 2](https://www.youtube.com/watch?v=Dkd1BbIZ1Vg) (5:40)

## Exercises

The following exercises are to be done _during_ and _following_ your reading and viewing of the resources. Work these out on paper and then enter the responses into the appropriate submission form (see Submission Instructions) by the deadline. You will receive a mark of __Pass__ if each item response shows a good-faith effort to be right and is submitted prior to the deadline. 

1. Consider the recurrence relation $S(k) + S(k-1) - 12 S(k-2) = 0$ with initial conditions $S(0) = 0$ and $S(1) = 3$. Is this recurrence relation homogeneous? Explain why or why not. 
2. Again consider the recurrence relation $S(k) + S(k-1) - 12 S(k-2) = 0$ with initial conditions $S(0) = 0$ and $S(1) = 3$. Write the characteristic equation for this recurrence relation. (Use the caret symbol ^ for exponents in the submission form, for example 3^k.)
3. Again consider the recurrence relation $S(k) + S(k-1) - 12 S(k-2) = 0$ with initial conditions $S(0) = 0$ and $S(1) = 3$. Find the solutions to the characteristic equation. Are they distinct or repeated? 
4. Explain how you would proceed to find a closed-form solution to the original recurrence relation in question 1 given the information you have about the solutions to the characteristic equation. 


## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1JPpgfx](http://bit.ly/1JPpgfx)