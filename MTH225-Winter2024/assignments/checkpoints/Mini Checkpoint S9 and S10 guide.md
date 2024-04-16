# Mini Checkpoint S9 and S10 guide 

## S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 
| 1 | Arithmetic | $a(n) = 4n+3$ | $a_0 = 3, a_n = a_{n-1} + 4$ | 
| 2 | Geometric | $a(n) = 3 \cdot 4^n$ | $a_0 = 3, a_n = 4a_{n-1}$ | 
| 3 | Neither | n/a | n/a | 
| 4 | Geometric | $a(n) = 10 \cdot \left( \frac{1}{2} \right)^n$ | $a_0 = 10, a_n = \frac{1}{2}a_{n-1}$ | 


## S10 

The characteristic equation for the recurrence relation is
$$r^2 = -4r + 12$$
Getting all the terms on the left gives $r^2 +4r - 12 = 0$. This factors into $(r+6)(r-2) = 0$ on the left, so the characteristic roots are $r = -6$ and $r=2$. 

The framework for the solution using those roots is: 
$$a(n) = c_1 (-6)^n + c_2 (2)^n$$

Plugging in $n=0$ gives the equation $1 = c_1 (-6)^0 + c_2(2)^0$ which simplifies to $c_1 + c_2 = 1$. 

Plugging in $n=1$ gives the equation $3 = c_1 (-6)^1 + c_2(2)^1$ which simplifies to $-6c_1 + 2c_2 = 3$. 

Using the "substitution" method for solving the system of equations, solve the first one for $c_2$ to get $c_2 = 1 - c_1$. Put this in for $c_2$ in the second one to get $-6c_1 + 2(1-c_1) = 3$. Simplifying this gives $2 - 8c_1 = 3$, so $c_1 = -1/8$. 

If $c_1 = -1/8$, then $c_2 = 1 - (-1/8) = 9/8$. 

So the final solution is
$$a(n) = -\frac{1}{8} (-6)^n + \frac{9}{8} (2)^n$$

(Decimals instead of fractions is OK as well, as long as they are correct and you showed work on how you got them.)