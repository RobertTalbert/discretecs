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
$7^{69} \\% 100 = \left(7^1 \cdot 7^4 \cdot 7^{64}\right) \\% 100 \\
    &= (7 \cdot 1 \cdot 1) \\& 100 \\
    &= (7) \\% 100 \\
    &= 7
\end{eqnarray*}$$