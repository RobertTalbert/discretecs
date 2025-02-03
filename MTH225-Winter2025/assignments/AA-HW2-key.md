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

1001 01100 10011  01111100110


$$\begin{eqnarray*}
19700710 &= 2^1 + 2^2 + 2^5 + 2^6 + 2^7 + 2^8 + 2^9 + 2^{11} + 2^{12} \\
             &+ 2^{15} + 2^{18} + 2^{19} + 2^{21} + 2^{24} 
\end{eqnarray*}$$

Each of the powers of 2 can be computed separately: 
$$\begin{eqnarray*}
19700710 &= 2 + 4 + 32 + 64 + 128 + 256 + 512 + 2048 + 4096 \\
             &+ 32768 + 262144 + 524288 + 2097152 + 16777216 
\end{eqnarray*}$$

It's a smart idea to double check this with a calculator before proceeding. 

Now replace the $19700710$ in $7^{19700710}$ with this sum: 
$$
7^{19700710} &= 7^{2 + 4 + 32 + 64 + 128 + 256 + 512 + 2048 + 4096 + 32768 + 262144 + 524288 + 2097152 + 16777216}
$$


Now split up the power into a product of smaller powers using high school algebra exponent rules:  

We now just need to compute each of these powers of $7$ modulo 100, which we can do by repeated squaring: 


Now putting all this back together gives: 


It's not easy to check work on this because the numbers are extremely, extremely large. But WolframAlpha has a "hidden" function called `PowerMod` that will do it: 

