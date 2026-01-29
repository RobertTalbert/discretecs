# Problem Set 1

Submit solutions on or before **11:59pm Eastern time on Friday, February 6** in order to be eligible for engagement credits. 

## Instructions

Welcome to your first Problem Set. The purpose of this Problem Set is to apply and extend the basic ideas from our recent classes. 

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 


---


## Problem 1: Check digit algorithms

The **International Standard Book Number** (ISBN-10) is a 10-digit code used to identify books. You will find one on the back cover of any book you pick up. To prevent errors caused by manual data entry, the tenth digit ($x_{10}$) is a check digit, calculated using modular arithmetic.Let the 10 digits be represented as $x_1, x_2, x_3, \dots, x_{10}$. The ISBN-10 standard requires that the digits satisfy the following congruence:

$$\sum_{i=1}^{10} i \cdot x_i \equiv 0 \pmod{11}$$

The symbol on the left is [sigma notation](https://publish.obsidian.md/discretecs/Basic+math+concepts/Sigma+notation) or [summation notation](https://publish.obsidian.md/discretecs/Basic+math+concepts/Sigma+notation). Click the link to learn more in the vault. 

(Note: Since the modulus is 11, if the check digit $x_{10}$ needs to be 10, we use the character 'X'.)

1. Determine if the following is a valid ISBN-10 code: `0-306-40615-2`. Show your work. 
2. A new computer science textbook has the first 9 digits 1-107-05713. Calculate the correct check digit $x_{10}$ to complete this ISBN.
3. One of the most common entry errors is mistyping a single digit (e.g., typing a $5$ instead of an $8$). Suppose the correct digit at position $k$ is $x_k$, but it is entered as $x'_k$. Write an expression for the difference between the correct sum and the erroneous sum. Then explain why this error will always result in a sum that is not congruent to $0 \pmod{11}$.
<!-- 
## Problem 2: Modular hashing and collision logic

Imagine you have a small storage locker with 10 slots, numbered 0 through 9. You need to store "keys" (large ID numbers) in these slots. A **Hash Function** is a rule that tells you which slot a key belongs to. The most common rule is the Remainder Method:

$$\text{Slot} = \text{Key} \pmod{\text{Number of Slots}}$$

1. You need to store the following ID numbers: 22, 10, 47, and 52. If your storage locker has 10 slots, calculate which slot each ID number goes into.
2. A "collision" happens when two different IDs want the same slot. Which two IDs from the list above collide?
3. If the locker size is 10, what do all ID numbers that "collide" in slot #5 have in common regarding their last digit?
4. In computer memory, data is often stored at addresses that are "even" (multiples of 2). Suppose all your ID numbers are even (2, 4, 6, 8, 10...). If you choose a locker with 8 slots (numbered 0–7), list all the slot numbers that will stay empty forever. Based on your answer, why is it usually a better idea to pick a [prime number](https://publish.obsidian.md/discretecs/Basic+math+concepts/Prime+and+composite+numbers) (like 7 or 11) for the number of slots rather than an even number like 8? -->


## Problem 2: Solving linear congruence equations

In standard algebra, $2x = 6$ has only one answer: $x = 3$. But in modular arithmetic, equations can have multiple solutions or even no solution at all. These equations look like regular equations but involve integer congruence, like: $ax \equiv b \pmod n$. A *solution* for one of these is a value of $x$ that makes the relationship true. For example, a solution to $2x \equiv 6 \pmod{11}$ is $x=3$. But this is not the only solution! Another is $x=14$, because $2 \times 14 = 28$ and $28 \equiv 6 \pmod{11}$. 

1. Find all the integer values of $x$ between $0$ and $12$ that solve the equation $3x \equiv 6 \pmod{12}$ and show your work. If there are no such integers, say so, then explain why. 
2. Find all the integer values of $x$ between $0$ and $12$ that solve the equation $5x \equiv 6 \pmod{12}$ and show your work. If there are no such integers, say so, then explain why. 
3. In CS, we often need to "undo" a multiplication. To undo $ax \equiv b$, we look for a **Modular Inverse**. This is a number $a^{-1}$ such that $a \cdot a^{-1} \equiv 1 \pmod n$. The $-1$ is not an exponent, but just a flag that tells us it is the modular inverse of $a$. Find a number $x$ such that $3 \cdot x \equiv 1 \pmod 7$ and explain your reasoning. (This $x$ is the "inverse" of 3.) Now, use that inverse to solve $3x \equiv 5 \pmod 7$. (Hint: Multiply both sides by your inverse).
4. Now suppose your modulus is $n = 6$. Try to find an inverse for 3, that is, a solution to $3 \cdot x \equiv 1 \pmod 6$. What happens? 
5. Looking at your work in the last two parts, what is the relationship between the number $a$ and the modulus $n$ that allows an inverse to exist? (Hint: Think about their common factors).