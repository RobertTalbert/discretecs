# MTH 325 Application/Analysis Exam 1 -- Solution Guide and Notes 

## Part A

1. B
2. E
3. C
4. B
5. A
6. A
7. B
8. B
9. C
10. E

## Part B

### Option 1

Results vary according to which proof technique is used. Here is a proof using the contrapositive: 

Assume that $n$ is odd. We will show that $n^3$ is odd. Since $n$ is odd, there exists an integer $k$ such that $n = 2k+1$. In that case, $n^3 = (2k+1)^3 = 8k^3 + 12k^2 + 6k + 1$. Factoring $2$ from the first three terms gives $2(4k^3 + 6k^2 + 3k) + 1$. Since $k$ is an integer, $q = 4k^3 + 6k^2 + 3k$ is also an integer. Therefore there $n^3 = 2q+1$ where $q$ is an integer, so $n^3$ is odd. 

### Option 2

Results vary according to which proof technique is used. Here is a direct proof: 

Assume that $a$ and $b$ are odd. We want to show that $a+b$ is even. Since $a$ and $b$ are odd, there exist integers $m$ and $n$ such that $a = 2m+1$ and $b = 2n+1$. Then $a+b = 2m + 2n + 2 = 2(m+n+1)$. Since $m$ and $n$ are integers, $m+n+1$ is also an integer and therefore $a+b$ (being $2$ times an integer) is even. 


## Part C

### Option 1

This proof uses weak induction. 

The base case is when $n = 0$. In this case the left side of the equation is just the single term $F_0$ (not an actual sum of multiple numbers), which is equal to $1$ by definition. On the right side we have $F_2 - 1$. Now $F_2 = F_1 + F_0 = 1 + 1 = 2$, so $F_2 - 1 =1$. The left and right sides are now equal, so the base case has been verified. 

Now assume that $F_0 + F_1 + F_2 + \cdots + F_k = F_{k+2} -1$ for some $k$. We want to show that $F_0 + F_1 + F_2 + \cdots + F_{k+1} = F_{k+3} -1$. 

Looking at the left side, we have $F_0 + F_1 + F_2 + \cdots + F_{k+1}$. Grouping the all but the last term gives $(F_0 + F_1 + F_2 + \cdots + F_k) + F_{k+1}$, and by the inductive hypothesis, we can substitute the sum in parentheses to get $(F_{k+2} - 1) + F_{k+1}$. Rearranging terms gives $F_{k+2} + F_{k+1} - 1$ and then by the Fibonacci recurrence relation we have $F_{k+3} - 1$. This is what we wanted to prove. 

### Option 2

The proposition is equivalent to saying: For all $n \geq 1$, the Fibonacci number $F_{3n-1}$ is even. This proof uses weak induction. 

The base case in this form is $n=1$. This gives the number $F_2$ which is equal to $2$, which is even. 

Now assume that $F_{3k-1}$ is even for some $k$. We want to prove that $F_{3(k+1)-1}$ is even. In the subscript, $3(k+1) - 1 = 3k + 2$. So we want to show that $F_{3k+2}$ is even. Using the Fibonacci identity gives us: $F_{3k+2} = F_{3k+1} + F_{3k}$. We also know from the Fibonacci identity that $F_{3k+1} = F_{3k} + F_{3k-1}$. 

Substituting this last expression into the first term of the first expression gives: 

$$F_{3k+2} = F_{3k+1} + F_{3k} = (F_{3k} + F_{3k-1}) +F_{3k}$$

Adding like terms gives  $F_{3k+2} = 2 F_{3k} + F_{3k-1}$

Now, $2 F_{3k}$ is even because it is an integer multiple of $2$; and $F_{3k-1}$ is even by the inductive hypothesis. Therefore $F_{3k+2}$ is the sum of two even numbers, which is even. 



## Part D 

### Option 1

### Option 2