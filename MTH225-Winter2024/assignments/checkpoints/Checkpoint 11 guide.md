# Checkpoint 11 guide 

## C1


## C2



## C3

## C4 


## C5 




## C6



---

[Remember it's now our policy](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 

## S4

 
## S5



## S6


## S7



## S8


## S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 



## S10

The characteristic equation for the recurrence relation is
$$r^2 = 3r + 4$$
Getting all the terms on the left gives $r^2 - 3r - 4 = 0$. This factors into $(r-4)(r+1) = 0$ on the left, so the characteristic roots are $r = 4$ and $r=-1$. 

The framework for the solution using those roots is: 
$$a(n) = c_1 (4)^n + c_2 (-1)^n$$

Plugging in $n=0$ gives the equation $5 = c_1 (4)^0 + c_2(-1)^0$ which simplifies to $c_1 + c_2 = 5$. 

Plugging in $n=1$ gives the equation $8 = c_1 (4)^1 + c_2(-1)^1$ which simplifies to $4c_1 - c_2 = 8$. 

Using the "elimination" method for solving the system of equations, we add the left and right sides of the first equation to the left and right sides of the second. The $c_2$ term cancels, leaving us with $5c_1 = 13$. Therefore $c_1 = 13/5$. 

To find $c_2$, plug $c_1 = 13/5$ in to $c_1 + c_2 = 5$ to get $13/5 + c_2 = 5$. Now solve for $c_2$ to get $c_2 = 5 - 13/5 = 12/5$. 

So the final solution is
$$a(n) = \frac{13}{5} (4)^n + \frac{12}{5} (-1)^n$$

(Note: Using decimals, $13/5 = 2.6$ and $12/5 = 2.4$. These are OK to use here.)