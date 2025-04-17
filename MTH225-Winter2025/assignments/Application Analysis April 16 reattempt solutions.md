# Application/Analysis Exam reattempt solution guides 

This document has solutions for both of the Application/Analysis Exam reattempts from April 16. Links to the original exam forms, with the questions, are provided on the [Class Page](https://docs.google.com/document/d/1pCxYpwLsHa9ciZv4zrtCH2P3aEM6g6Za2onQsOJCung/edit?pli=1&tab=t.0) entry for April 16. 

## Exam 1 reattempt solutions

Click here for the exam form with the questions. 

### Multiple Choice 

1. C
2. C
3. C
4. B
5. A
6. B
7. C
8. D
9. C
10. A

### Problem Group 1

1. Here are the steps for the base conversion algorithm. We repeatedly divide by 36 and keep the remainder until the quotient is 0; then the final result is the remainders in reverse order. 

$$\begin{eqnarray*}
483726 &= 13436(36) + 30 \\
13436 &= 373(36) + 8 \\
373 &= 10(36) + 13 \\
10 &= 0(36) + 10
\end{eqnarray*}$$

The remainders are 30, 8, 13, 10. The final result is the remainders in reverse order, which is 10, 13, 8, and 30. In base 36, "10" is represented by the letter `a`, "13" is represented by the letter `d`, and "30" is represented by the letter `u`, so the final result is `ad8u`.

1. Since $89$ is `1011001` in binary, it means that 
$$89 = 1 \cdot 2^6 + 0 \cdot 2^5 + 1 \cdot 2^4 + 1 \cdot 2^3 + 0 \cdot 2^2 + 0 \cdot 2^1 + 1 \cdot 2^0$$
Use this fact to replace the 89 in the exponent with a sum of powers of 2: 
$$7^{89} = 7^{2^6 + 2^4 + 2^3 + 2^0} = 7^{64 + 16 + 8 + 1}$$
Now we can use the fact that $a^{b + c} = a^b \cdot a^c$ to rewrite this as
$$7^{89} = 7^{64} \cdot 7^{16} \cdot 7^{8} \cdot 7^{1}$$
Now we can calculate each of these powers of 7 using repeated squaring, modulo 100 since we want the last two digits. 

$$\begin{eqnarray*}
7^1 &= 7 \\
7^2 &= 49 \\
7^4 &= 49^2 = 2401 = 1 \mod 100 \\
7^8 &= 1^2 = 1 \mod 100 \\
7^{16} &= 1^2 = 1 \mod 100 \\
7^{32} &= 1^2 = 1 \mod 100 \\
7^{64} &= 1^2 = 1 \mod 100 \\
\end{eqnarray*}$$

Now we can multiply these together, modulo 100.

$$\begin{eqnarray*}
7^{89} &= 7^{64} \cdot 7^{16} \cdot 7^{8} \cdot 7^{1} \\
&= 1 \cdot 1 \cdot 1 \cdot 7 \\
&= 7 \mod 100 = 7 
\end{eqnarray*}$$

So the last two digits of $7^{89}$ are 07.

### Problem Group 2

1. The input to the function is the list `[3,5,2,8,1]`. Here are the steps given in order as a bullet list:

- The length of the input is not 1. So `sub_max` is set equal to  `recursive_max([5,2,8,1])` and the item returned is either 3 or the result of the recursive call, whichever is larger. We won't know this until the recursion is done. 
- The length of the input is not 1. So set `sub_max` equal to the function `recursive_max([2,8,1])`. The item returned is either 5 or the result of the next recursive call, whichever is larger. We won't know this until the recursion is done.
- The length of the input is not 1. So set `sub_max` equal to the function `recursive_max([8,1])`. The item returned is either 2 or the result of the next recursive call, whichever is larger. We won't know this until the recursion is done.
- The length of the input is not 1. So set `sub_max` equal to the function `recursive_max([1])`. The item returned is either 8 or the result of the next recursive call, whichever is larger. We won't know this until the recursion is done.
- The length of the input is 1. So return `1` and begin to work our way up through the pending calculations.
- The previous function call returns the larger of 8 and 1, which is 8. 
- The function call before that returns the larger of 2 and 8, which is 8. 
- The function call before that returns the larger of 5 and 8, which is 8. 
- The function call before that returns the larger of 3 and 8, which is 8. This is the top-most calculation in the stack, so the final result is 8. 


2. The proof has more than one significant error: 
   
   - The inductive step is incorrect. It says we need to show that $k^2 + 1 \leq 2^{k+1}$, but it should be $(k+1)^2 \leq 2^{k+1}$. Note, $k^2 + 1 \neq (k+1)^2$. (This is the main error and this one must be pointed out to have a successful solution.)
   - There is also an algebra error in the inductive step: It says $2^k + 2^1 = 2^{k+1}$ but this is not true. 

### Problem Group 3

1. Here is a truth table comtaining all the statements. The premises are indicated with a check mark; the conclusion has a star. 

| $p$ | $q$ | $r$ | $p \wedge q$ ✓ | $\neg p$     | $(\neg p) \wedge r$ ✓ | $q \vee r$ ☆     | |              
| --- | --- | --- | --------------- | --- | ---------------------- | --- | ------------- | 
| T   | T   | T   | T               |  F   | F                      | T   |       
| T   | F   | T   | F               |  F   | F                      | T   |        
| F   | T   | T   | F               |  T   | T                      | T   |      
| F   | F   | T   | F               |  T   | T                      | T   |     
| T   | T   | F   | T               |  F   | F                      | T   |       
| T   | F   | F   | F               |  F   | F                      | F   |      
| F   | T   | F   | F               |  T   | F                      | T   |  
| F   | F   | F   | F               |  T   | F                      | F   | 

In this argument, **the premises are never true simultaneously**. Therefore **this argument is considered valid** because the definition of a "valid" argument is based on the conditional statement that *if* the premises are true, *then* the conclusion is true; this conditional statement has a hypothesis that is always false, therefore the conditional statement is true. 

Put differently: An argument is *invalid* if there is a situation (row in the truth table) where the premises are true but the conclusion is false. That never happens here because the premises are never true in the same row. Therefore the argument fails to be invalid, i.e. the argument is valid. 

1. .
   - (a) Based on the descriptions above, he truth tables for NAND and NOT are: 
  
| p | q | p NAND q | p NOR q | 
|---|---|----------| ------ | 
| T | T | F        | F
| T | F | T        | F
| F | T | T        | F
| F | F | T        | T

   - (b) Here are the truth tables for $\neg (p \land q)$ and $\neg (p \lor q)$: 

| $p$ | $q$ | $p \land q$ | $\neg(p \land q)$ |  $p \lor q$   |  $\neg(p \lor q)$   |
| --- | --- | ----------- | ----------------- | --- | --- |
| T   | T   | T           | F                 |  T   |  F   |
| T   | F   | F           | T                 |  T   |   F  |
| F   | T   | F           | T                 |  T  |  F  |
| F   | F   | F           | T                 |   F  |  T   |

The results in column 4 are the same as for NAND; the results in column 6 are the same as for NOR. Therefore the logical equivalences hold. 



##  Exam 2 reattempt solutions


### Multiple choice 

1. C
2. B
3. B
4. B
5. A
6. A
7. A
8. E
9. B
10. B

### Problem Group 1

1. All three solutions are incorrect: 
   - Solution 1 is incorrect because it assumes the candies are all distinct from each other. This leads to counting the same arrangement multiple times. For example, call the children Alice, Bob, and Charlie and consider the labelling with Alice's name on the first candy, Bob's name on the second candy, and Charlie's name on the remaining 18. This is the same as labelling the first candy with Bob's name, the second with Alice's name, and the remaining 18 with Charlie's name because the candies are all the same; but the solution counts these as different arrangements.
   - Solution 2 is incorrect because there is nothing to guarantee that all 20 candies are given out or that the total number of candies given out is 20. For example one distribution counted by this method is to give each child 15 candies, so fill in each child's blank with 15. But this isn't possible because there are only 20 candies to give out. 
   - Solution 3 is incorrect because we are not, in fact, selecting 3 items from a group of 20. This would be correct if the candies were all different and we wanted to select 3 of them. But that's not what's happening here. 

2. The key is to remember that $\binom{n}{k}$ counts the number of bit strings of length $n$ that have weight $k$. (You can also take the approach that it counts the number of subsets of size $k$ of a set of size $n$, but the solution here will use bitstrings.) The sum on the left counts the number of $n$-bit strings that are weight 0, or weight 1, or weight 2, and so on up through weight $n$. But since every $n$-bit string has to have one of those weights and no bitstring can have two of them, that sum simply counts the total number of bitstrings of length $n$. On the other hand, we know that the total number of bitstrings of length $n$ is $2^n$. So the left side counts the number of bitstrings of length $n$ and the right side counts the number of bitstrings of length $n$. So they are equal.

### Problem Group 2

1. .
   - (a) `floor` is surjective but not injective. An example where it fails to be injective is `floor(3.5) = floor(3.9) = 3`. (The function is surjective because given any integer in the codomain, we can find an input that maps to it, namely that integer itself. For example if we pick $5$ then `floor(5)` equals this.) 
   - (b) `abs` is neither injective nor surjective. It it not injective because for example `abs(-3) = abs(3) = 3`. It is not surjective because there are numbers in the codomain that are not in the range. For example, `abs(x)` cannot equal `-1` for any real number $x$.
   - (c) `max` is surjective but not injective. An example where injectivity fails would be the two lists `[1,2]` and `[0,2]`; these are different lists but they have the same maximum value. (The `max` function is surjective because given any float in the codomain, we can input the list containing just that one float and it will return that float as the maximum value. For example if we pick $5$ then `max([5])` equals this.)

2.
    - (a) If repetitions are allowed, then we have eight positions with 26 choices for each position. So the answer is $26^8 = 208827064576$.
    - (b) If repetitions are not allowed, then we have 26 choices for the first position, 25 for the second, and so on down to 19 choices for the last position. So the answer is $26 \cdot 25 \cdot 24 \cdots 19 = \frac{26!}{18!} = 1562275$.
    - (c) There are eight different positions where the `X` could go. For each of those positions, there are seven positions remaining with 25 choices for the first of those (because you can't repeat the `X`), 24 choices for the second, 23 for the third, 22 for the fourth, 21 for the fifth, 20 for the sixth, and 19 for the seventh, So the answer is $8 \cdot 25 \cdot 24 \cdots 19 = 19381824000$. 

### Problem Group 3

1. It helps to note that a sequence of coin flips with each flip giving you heads or tails, is equivalent to a string of bits consisting of `0` or `1`. Think of `0` as representing tails and `1` as representing heads. 
   - (a) There are 10 positions and two choices for each position, so the answer is $2^{10} = 1024$.
   - (b) The number of ways to select 2 heads from 10 flips is $\binom{10}{2} = 45$, the same as the number of 10-bit strings with exactly two `1` bits. 
   - (c) Having "at most" three tails means having no tails, or just 1, or just 2, or just 3. The count for each of those is $\binom{10}{0}$, $\binom{10}{1}$, $\binom{10}{2}$, and $\binom{10}{3}$. So the answer is $\binom{10}{0} + \binom{10}{1} + \binom{10}{2} + \binom{10}{3} = 1 + 10 + 45 + 120 = 176$.

2. 
   - (a) The number of permutations of an 8-character string with all the letters different is $8! = 40320$.
   - (b) If the rightmost letter must be `H`, then we have 7 positions to fill with the remaining 7 letters. So the answer is $7! = 5040$.
   - (c) If the string must contain `BCD`, then we can treat `BCD` as a single "letter". This leaves six objects to permute: `BCD`, `A`, `E`, `F`, `G`, and `H`. So the answer is $6! = 720$.