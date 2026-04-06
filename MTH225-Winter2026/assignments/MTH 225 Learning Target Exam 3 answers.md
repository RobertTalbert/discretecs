# MTH 225 Learning Target Exam 3 answers and notes 

## Learning Target 9

1. The value of the variable for the base case is $n=0$. In this case, we have $4^0 - 1$ which equals $1-1$ or $0$. The integer $3$ divides $0$ because `0 % 3 = 0`. So the base case holds. 
2. Assume that for some $k$, $3$ divides $4^k - 1$. 
3. Prove that $3$ divides $4^{k+1} - 1$. 

## Learning Target 10 

1. This is a situation where we are selecting one object from disjoint bins, so we use the Additive Principle. The count is $4 + 7 + 3 = 14$. 
2. This is literally a license plate problem. There are $26$ letter choices for the first letter, then $25$ for the second one, then $24$ for the third, followed by $10$ choices for each of the digits. So the count is $26 \cdot 25 \cdot 24 \cdot 10^3 = 15,600,000$. 
3. The number of integers in this range divisible by $3$ is $33$ and the number divisible by $5$ is $20$. There are $6$ integers in this range that are divisible by both $3$ and $5$ (that is, divisible by $15$). So we need to use the Principle of Inclusion and Exclusion, and the count is $33 + 20 - 6 = 47$. 

## Learning Target 11

1. $\binom{12}{9} = \frac{12!}{9! 3!} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220$. 
2. Order doesn't count when forming a committee, so the count is $\binom{20}{5} = 15504$. 
3. All the letters in the word are distinct, so the count is $8! = 40320$. 
4. It's best to think of this as a license plate problem. We have three slots to fill and no repetitions (since once we select a letter, it can't be selected again). This gives $8$ choices for the first character, $7$ for the second, and $6$ for the third giving a count of $8 \cdot 7 \cdot 6 = 336$. This is the same as $P(8,3)$. 

## Learning Target 12 

1. Geometric. Closed formula: $a(n) = 3 \cdot 2^n$. Recurrence relation: $a(0) = 3$ and $a(n) = 2 \cdot a(n-1)$ for $n > 0$. 
2. Aritmetic. Closed formula: $a(n) = 3n+3$. Recurrence relation: $a(0) = 3$ and $a(n) = 3+ a(n-1)$ for $n > 0$.  
3. Neither. 
4. Arithmetic. Closed formula: $a(n) = 3 - 2n$. Recurrence relation: $a(0) = 3$ and $a(n) = a(n-1) - 2$ for $n > 0$. 