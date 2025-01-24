# Answers/Solutions for Application/Analysis Homework 1

## Practice Exercises

To check your work on these exercises, please use the technological tools we've introduced in class and contact me (Talbert) with any questions you have. If you submitted work, I will look at it and give feedback on the PDF you submitted (check Blackboard for this). 

## Multiple Choice items 

1. A
2. B
3. C
4. D
5. C
6. D

## Problems to Solve

1. Answers/solutions below: 
- (a) Here $q = -5$ and $r=0$, because $-150 = 30(-5) + 0$. 
- (b) Here $q = -169$ and $r=3$, because $-2025 = 30(-169) + 3$. 
- (c) The main problem here is that according to the Division Algorithm, the remainder $r$ has to satisfy the inequalities $0 \leq r < b$ where $b$ is the number we are dividing by. But since $b = -3$ here, it's not possible to find a value for $r$ that works, because if $0 \leq r$ and $r < b$ then this would imply that $0 < b$, which is fine except when $b$ is negative --- which it is here. So our version of the Division Algorithm does not even allow negative divisors in the first place. To get around this, Alex can just notice that dividing $500$ by $-3$ is the same thing as dividing $-500$ by $+3$. This would give a quotient of $-167$ and a remainder of $1$. 

Notice this quotient/remainder pair does not make the equation $500 = -3q + r$ work. But it does make the equation $-500 = 3q + r$ work, and now $0 \leq r < b$ is also satisfied. 

- (d) We get $-1999 = 6(-334) + 5$. Therefore $-1999  \\%  6 = 5$. 


1. To find the number of hours to add on to the time of 2:00pm after any number of hours has passed, let's say $n$ hours, compute $n \\% 24$. To see why, notice that every 24 hours we are at the same4 time of the day. So if $n$ is the total number of hours has passed, the quotient of $n$ divided by $24$ gives the number of *days* that have passed, and the remainder gives the number of "partial days" or hours. So, if 100000 hours have passed since 2:00pm, divide 100000 by 24. The quotient is 4166 and the remainder is 16. This means that 4166 complete days have passed, plus 16 extra hours. Moving ahead 16 hours from 2:00pm puts us at **6:00am**.  

2. Answers will vary on this one based on the integer you generated. Here is a sample solution for the integer $3881$. 

We will use the base conversion algorithm and divide by $60$. 

- Divide $3881$ by $60$ to get a quotient of $64$ and a remainder of $41$. 
- Divide $64$ by $60$ to get a quotient of $1$ and a remainder of $4$. 
- Divide $4$ by $60$ to get a quotient of $0$ and a remainder of $4$. 

The quotient is zero, so the algorithm stops and now the number in base 60 is the remainders in reverse order. In our version of this system, the number $41$ is represented by $F$ (upper case!). So in base 60, $3881$ is $44F$. 