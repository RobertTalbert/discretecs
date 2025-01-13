# Application/Analysis Homework 1

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Welcome to your first Application/Analysis Homework set. Each Application/Analysis homework set has three parts: 

- *Optional practice exercises*, for you to use in getting practice with the Learning Targets involved in the homework; 
- *Multiple choice questions*, which ask you to think about underlying concepts; and 
- *Problems to solve*, where you are asked to apply or extend the basic ideas from class to new situations or questions. 

You are to **work all problems on your own paper or on a whiteboard**. You can also type them up if you want to, or use a tablet and stylus to make a handwritten electronic submission. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 1**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

Application/Analysis Exam 1, scheduled for Friday February 21, will consist of problems taken verbatim from all the Application/Analysis Homework sets up to that point, including this one. So it is to your strong advantage to maximize your understanding of the problems and questions you find below --- you will see these on a test later.  


---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. Use the Division Algorithm to find the values of $q$ and $r$ given by that algorithm, for these values of $a$ and $b$. (That is, write $a = bq+r$ and $0 \leq r < b$.)
- (a) $a = 220, b = 70$ 
- (b) $a = 855, b = 395$ 
- (c) $a = 872, b = 77$ 

2. Find the values of the following. (Note, the ones with negative numbers involved are explained in the vault and also in problem 1 below.)
- (a) `127 % 5`
- (b) `181130 % 2`
- (c) `100000 % 24` 
- (d) `(-100) % 6`

3. Use the Euclidean Algorithm to compute the following. 
- (a) $\gcd(100,88)$
- (b) $\gcd(1000000, 880)$
- (c) $\gcd(12347, 67891)$

4. Convert each integer below from the given base to the other base. 
- (a) 181130 from base 10 to base 8
- (b) 6621 from base 8 to base 10 
- (c) 3ABC from base 16 to base 10 
- (d) 11001101 from base 2 to base 16 (without going to base 10 first) 


 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

**1. Which of the following represents the Division Algorithm?**  
- A. $a = bq + r$, where $0 \leq r < b$  
- B. $a = bq + r$, where $0 \leq r \leq b$  
- C. $a = bq - r$, where $0 \leq r < b$  
- D. $a = b + q \times r$  

**2. If $a = 27$, $b = 5$, what are the quotient $q$ and remainder $r$ based on the Division Algorithm?**  
- A. $q = 6, r = 1$  
- B. $q = 5, r = 2$  
- C. $q = 5, r = 0$  
- D. $q = 6, r = 2$  

**3. What is the primary purpose of the Euclidean Algorithm?**  
- A. To find the product of two integers  
- B. To determine the least common multiple (LCM)  
- C. To compute the greatest common divisor (GCD)  
- D. To solve linear equations  

**4. In the Euclidean Algorithm, if $a = 196$ and $b = 28$, what is the first step?**  
- A. Compute $196 - 28$  
- B. Compute $196 \% 28$  
- C. Compute $28 \% 196$  
- D. Compute the quotient of 196 divided by 28 

**5. What does $a \% b$ represent?**  
- A. The division of $a$ by $b$  
- B. The product of $a$ and $b$  
- C. The remainder when $a$ is divided by $b$  
- D. The sum of $a$ and $b$  

**6. When converting the base 10 integer 2025 to octal, what is the first step?**
- A. Compute $2025 \% 2$
- B. Compute $2025 \% 8$ 
- C. Compute the quotient of 2025 divided by 8
- D. Find both the quotient and remainder of 2025 divided by 8



## Problems to solve 

1. The statement of the [Division Algorithm](https://publish.obsidian.md/discretecs/Computer+Arithmetic/Division+algorithm) and the [modulus operator](https://publish.obsidian.md/discretecs/Computer+Arithmetic/Modulus+operator) in the course vault says that the two numbers involved in the division must be positive. But this is not strictly necessary: One, or even both of them could be negative. These exercises get you to explore this possibility. 
   - (a) Suppose $a = -150$ and $b = 30$. The Division Algorithm would state that you can find integers $q$ and $r$ such that $-150 = 30q + r$ and $0 \leq r < 30$. What are the values of $q$ and $r$ that make this happen here? There will be only one possible right answer. 
   - (b) Similarly, find the values of $q$ and $r$ that the Division Algorithm would give you if you were dividing $-2025$ by $12$. 
   - (c) Suppose that Alex is doing a similar calculation and trying to find the values of $q$ and $r$ given by the Division Algorithm when $a = 500$ and $b = -3$ --- that is, when dividing $500$ by $-3$. Alex comes up with $q = -166$ and $r = 2$. Alex shows you that this is right by computing $(-3)(-166) + 2 = 500$. However, these values are incorrect! Find and explain Alex's mistake, find the correct values of $q$ and $r$, and explain your reasoning. (*Hint*: Look at the *entire* Division Algorithm, especially the very end.)
   - (d) The modulus operator can be used with negative integers, since we now see that the Division Algorithm can be used with negative integers. Consider $a = -1999$ and $b = 6$. Find the values of $q$ and $r$ given by the Division Algorithm so that $a = bq + r$. Then state the value of `a % b` and explain how this result can be obtained from the Division Algorithm. 

2. If it's 2:00pm right now, what time of the day will it be 100,000 hours from now? State your answer clearly and show all your work. *Hint*: The modulus operator comes in handy. 

<!-- 3. The **Extended Euclidean Algorithm** is a modification of the Euclidean Algorithm that takes in two positive integers $a$ and $b$, and expresses their greatest common divisor as a "combination" of $a$ and $b$, which means we can multiply $a$ by some integer and $b$ by some integer and add the results to get $\bcd(a,b)$. For example, if $a = 10$ and $b = 25$, their GCD is $5$, and we can write $5$ as a combination of $10$ and $25$ like this: $25 = 10(-2) + 25(1)$. This video shows how the Euclidean Algorithm can be "extended" to do this. Watch the video; then do the following. 
   (a) Generate two random positive integers $a$ and $b$ that are either 4 or 5 digits long. Then use the (ordinary) Euclidean Algorithm to find $\gcd(a,b)$. Show all your steps, like the examples in class. 
   (b) Then use the Extended Euclidean Algorithm to find integers $x$ and $y$ such that $\gcd(a,b) = ax + by$. Use the example in the video as your guide.  -->

4. In class we have worked with integers in bases 2, 8, 10, and 16. But other bases are possible. The ancient Babylonians used base 60 or **sexagesimal** for their numbers --- it's where we got 60 minutes in an hour, 360 degrees in a circle, and more. [The Wikipedia article goes into some detail on this](https://en.wikipedia.org/wiki/Sexagesimal), including the symbols used for digits. Generate a random integer with four or five digits, then convert it by hand to base 60 using the base conversion algorithm. Show all your steps. For the symbols, use the following: 
   - Ordinary 0-9 for zero through nine
   - Lower-case letters of the alphabet for 10-35; that is, a = 10, b = 11, ..., z = 35
   - Upper-case letters of the alphabet for the rest; so A = 36, B = 37, ..., X = 59. (You would not need to represent "60".)

Unfortunately some of these symbols look like others; for example lower and upper case "X" look similar, and capital "O" looks like a zero. If you encounter this problem, leave a note telling what the ambiguous symbols mean. 
