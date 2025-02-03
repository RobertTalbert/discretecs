# Answers/Solutions for Application/Analysis Homework 2

## Practice Exercises

To check your work on these exercises, please use the technological tools we've introduced in class and contact me (Talbert) with any questions you have. If you submitted work, I will look at it and give feedback on the PDF you submitted (check Blackboard for this). 

## Multiple Choice items 

1. A
2. C
3. B
4. B
5. A

## Problems to Solve

1. Truth table is below. This shows the statement $P \leftrightarrow Q$ built up step by step with intermediate columns. The rightmost column is $(P \rightarrow Q) \wedge (Q \rightarrow P)$ which is the same as $P \leftrightarrow Q$ by definition. 

| $P$ | $Q$ | $P \rightarrow Q$ | $Q \rightarrow P$ |  $(P \rightarrow Q) \wedge (Q \rightarrow P)$ | 
| --- | ---- | ---- | ---  | ----- | 
| T | T | T | T | T |
| T | F | T | F | F |
| F | T | F | T | F |
| F | F | T | T | T |

(Aside, this truth table says $P \leftrightarrow Q$ is true whenever $P$ and $Q$ share the same truth value, and is false otherwise.)


2. The answers here will vary based on what your birthdate is. Here's a solution using Prof. Talbert's birthday of July 10, 1970 (yes, I am super old). 

Converting the birthday to the format we want here gives 19700710. In binary, this is `1001011001001101111100110`. (I used the [base conversion calculator](https://www.rapidtables.com/convert/number/base-converter.html).) 

We now want to find the last two digits of $7^{19700710}$. **Getting the last two digits of an integer $n$ involves finding $n \\% 100$**. (For example, `5538 % 100 = 38`). So we'll use the repeated squaring algorithm to compute $7^{19700710} \\% 100$. 

First, work on the exponent by itself to split it into a sum of powers of 2. We use the binary for that. Since $(19700710)_{10}$ in base 2 is `1001011001001101111100110`, it means: 

$$\begin{eqnarray*}
19700710 &= 2^1 + 2^2 + 2^5 + 2^6 + 2^7 + 2^8 + 2^9 + 2^{11} + 2^{12} \\
             &+ 2^{15} + 2^{18} + 2^{19} + 2^{21} + 2^{24} 
\end{eqnarray*}$$

Each of the powers of 2 can be computed separately: 

$$\begin{eqnarray*}
19700710 &= 2 + 4 + 32 + 64 + 128 + 256 + 512 + 2048 + 4096 \\
             &+ 32768 + 262144 + 524288 + 2097152 + 16777216 
\end{eqnarray*}$$

(It's a smart idea to double check this with a calculator before proceeding.) 

Now replace the $19700710$ in $7^{19700710}$ with this sum: 

$$7^{19700710} = 7^{2 + 4 + 32 + 64 + 128 + 256 + 512 + 2048 + 4096 + 32768 + 262144 + 524288 + 2097152 + 16777216}$$


Now split up the power into a product of smaller powers using high school algebra exponent rules:  


$$7^{19700710} = 7^2 7^4 7^{32} 7^{64} 7^{128} 7^{256} 7^{512} 7^{2048} 7^{4096} 
7^{32768} 7^{262144} 7^{524288} 7^{2097152} 7^{16777216}$$ 

We now just need to compute each of these powers of $7$ modulo 100, which we can do by repeated squaring: 

$$\begin{eqnarray*} 
7^2 \\% 100 &= 49 \\% 100 = 49 \\
7^4 \\% 100 = (7^2)^2 \\% 100 &= (49)^2 \\% 100 = 2401 \\% 100 = 1 \\
7^8 \\% 100 = (7^4)^2 \\% 100 &= 1^2 \\% 100 = 1 \\
7^{16} \\% 100 = (7^8)^2 \\% 100 &= 1^2 \\% 100 = 1 \\
7^{32} \\% 100 = (7^{16})^2 \\% 100 &= 1^2 \\% 100 = 1 
\end{eqnarray*}$$

In fact we can stop here, because it's clear that all other powers of 7 where the exponent is a power of 2, are just going to be 1 mod 100. 

Now putting all this back together gives: 

$$\begin{eqnarray*}
7^{19700710} \\% 100 &= (7^2 7^4 7^{32} 7^{64} \cdots  7^{16777216}) \\% 100 \\
           &= (49 \cdot 1 \cdot 1 \cdots 1) \\% 100 \\
           &= 49. 
\end{eqnarray*}$$

So the last two digits of $7^{19700710}$ are $49$. 

It's not easy to check work on this because the numbers are extremely, extremely large. (The number $7^{19700710}$ has $16,649,032$ digits.) But WolframAlpha has a "hidden" function called `PowerMod` that will do it. [Here is the calculation](https://www.wolframalpha.com/input?i=PowerMod%287%2C+19700710%2C+100%29). The function `PowerMod` takes three inputs: the base, the exponent, and the modulus and runs this repeated squaring algorithm to make the computation; try it out on your problem to check the answer. 

