# Application/Analysis Exam 1 Solution Guide

## Multiple Choice Answers

1. C
2. C
3. A
4. C
5. C
6. D
7. C
8. A
9. C
10. C

## Problem Group 1 (Computation)

1. Convert the number 20259 from base 10 to base 60. 

**Solution:** Run the base conversion algorithm, dividing by 60 each time and recording the remainders: 

$$\begin{eqnarray*}
20259 &= 60(337) + 39 \\
337 &= 60(5) + 37 \\
5 &= 60(0) + 5
\end{eqnarray*}$$

Here the algorithm stops because the quotient is $0$. Since this is base 60, the remainders of $37$ and $39$ are represented by `B` and `D` respectively. Reading the remainders off in reverse order gives the base 60 representation: `5BD`. 

2. Find the last two digits of $7^{69}$. 

**Solution:** The binary for $69$ is `1000101` as stated. This means that 
$$69 = 1 + 4 + 64$$
So $7^{69} = 7^{1 + 4 + 64} = 7^1 \cdot 7^4 \cdot 7^{64}$. Now go through repeated squaring mod 100 to get these powers of $7$:

$$\begin{eqnarray*}
7^1 \\% 100 &= 7 \\
7^2 \\% 100 &= \left( 7^1 \right)^2 \\% 100 = 49 \\% 100 = 49 \\
7^4 \\% 100 &= \left( 7^2 \right)^2 \\% 100 = 49^2 \\% 100 = 2401 \\% 100 = 1 \\
7^8 \\% 100 &= \left( 7^4 \right)^2 \\% 100 = 1 \\% 100 = 1 
\end{eqnarray*}$$

From here we can see that $7^{16}, 7^{32}$, and $7^{64}$ will all be 1 mod 100 because we're just squaring $1$ over and over. 

Therefore: 

$$\begin{eqnarray*}
7^{69} \\% 100 &= \left(7^1 \cdot 7^4 \cdot 7^{64}\right) \\% 100 \\
    &= (7 \cdot 1 \cdot 1) \\% 100 \\
    &= (7) \\% 100 \\
    &= 7
\end{eqnarray*}$$

Side note: Double checking with a computer shows that this is right, because here is $7^{69}$: 

$$20500514515695490612229010908095867391439626248463723805607$$

## Problem Group 2 (Algorithms and proofs)

1. Manually work through the following recursive algorithm to find $\gcd(456, 789)$: 

```python
def gcd(a,b):
   if a == 0: return b
   else: 
      return gcd(b % a, a)
```

There are lots of ways to display the information when tracing through the code. Here is one way, using a table: 

| $a$ | $b$ | Is $a = 0$? | $b \\% a$ | Return:          |
| --- | --- | ----------- | ------- | ---------------- |
| 456 | 789 | No          | $333$   | $\gcd(333, 456)$ |
| 333 | 456 | No          | 123     | $\gcd(123,333)$  |
| 123 | 333 | No          | 87      | $\gcd(87,123)$   |
| 87  | 123 | No          | 36      | $\gcd(36,87)$    |
| 36  | 87  | No          | 15      | $\gcd(15,36)$    |
| 15  | 36  | No          | 6       | $\gcd(6,15)$     |
| 6   | 15  | No          | 3       | $\gcd(3,6)$      |
| 3   | 6   | No          | 0       | $\gcd(0,3)$      |
| 0   | 3   | YES -- STOP |         |          3        |


So $\gcd(456,789) = 3$. 

2. Critique the following proof of the proposition **For all positive integers $n$, $11^n - 6$ is a multiple of $5$. 

>**Proof:** We prove this with mathematical induction. So assume that for some positive integer $k$, $11^k - 6$ is a mulitple of $5$. We want to show that $11^{k+1} - 6$ is a multiple of $5$. Looking at $11^{k+1} - 6$, we can factor out an $11$ to get $11(11^k - 6)$. But, in the inductive hypothesis we assumed that $11^k-6$ is a multiple of $5$. Since $11^{k+1} - 6 = 11(11^k - 6)$ and the expression in parentheses is a multiple of $5$, it means that $11^{k+1} - 6$ is $11$ times a multiple of $5$, so therefore $11^{k+1} - 6$ is also a multiple of $5$. This is what we wanted to show, so the proposition is proven. 

Here is a list of the major errors in this proof: 

- **There is no base case**. This is a major error because without the base case, we have not established that the proposition is true in any case, so the inductive hypothesis might be false. 
- **The "factoring" step going from $11^{k+1} - 6$ to $11(11^k - 6)$ is incorrect.** There is no factor of $11$ on the second term, so an $11$ cannot be factored out. This is a major error because the rest of the proof is built on the idea that $11^k - 6$ is a multiple of $5$ and the expression $11^{k+1} - 6$ is $11$ times a multiple of $5$. 


## Problem Group 3 (Logic)