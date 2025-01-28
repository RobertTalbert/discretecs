# Answer key for Learning Target Exam 1

Please review the course announcement from 2025-01-28 for details. Please bring questions to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 

## Learning Target 1

1. Use long division to find the quotient and remainder obtained when dividing $78294$ by $22$.

**Answer**: Quotient = 3558, Remainder = 18. Note: Work is not shown on this one due to math formatting limitations. For questions about your work, please bring those to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 



2. Use the Euclidean Algorithm to find $\gcd(250, 8)$. 

**Solution**: 

$$\begin{eqnarray*}
250 &= 8(31) + 2 \\
8 &= 2(4) + 0
\end{eqnarray*}$$

The remainder is zero, so the algorithm halts and the GCD is the last nonzero remainder: $\gcd(250,8) = 2$. 


**Answer**: 2

3. State the values of each of the following: 

- (a) $1234  \\% 56$ 
- (b) $123098091235 \\% 2$
- (c) $7890 \\% 3$

**Answers**: 2, 1, 0. (Note, no work needs to be shown here because it asks you to "state" the values.) 

### Notes 

- **On the Euclidean Algorithm question, several responses mistakenly shifted the values in the second step to use the *quotient* from the previous step (31) instead of the divisor (8).** So the second step looked like: $31 = 2(15) + 1$ and then there was a third step, $15 = 1(15) + 0$. In this work, the algorithm terminates but the GCD it returns would be the last nonzero remainder which according to this work would be 1, not 2. So the answer was correct but it's inconsistent with the work, which is an incorrect implementation of the algorithm. This results in the Learning Target being marked *Proficient* or *Beginner* and this will need to be reattempted later. 
- Also on this problem, some responses made the above mistake and stated that the GCD is 1, which is consistent with the work but incorrect (and not a "simple" mistake, like a miscopied number). **A simple reality check can alert you to this error:** Notice that both 250 and 8 are even, so they are both divisible by 2; therefore the GCD can't possibly be 1 because the GCD is by definition the largest integer that divides both. This would have to be at least 2 this time. 
- Also on this problem, some responses made other mistakes and came up with GCDs of 4, or 7. **A simple reality check can alert you to this error:** Neither 4 nor 7 divides 250, so these cannot possibly be the GCD because by definition, the GCD has to divide both numbers. 
- On the third item, several responses gave the quotient of the two numbers being divided, or mistook the symbol `%` for the division symbol $\div$ and gave both the quotient and the remainder. Neither is correct, so make sure you know what `%` means. 
- Also on the third item, some responses gave answers that were not possible, for example $123098091235 \\% 2 = 3$. Again, make sure you know what `%` means and how this affects the size of the answer. 
- Also on the third item, not a mistake, but some responses did the full long division process to determine the answer, and this is not necessary. For example $123098091235 \\% 2$ can be determined to equal 1 by merely noticing that $123098091235$ is odd --- no long division needed and no calculator activities needed. 


## Learning Target 2

>I can convert a positive integer between bases 2, 8, 10, and 16; and I can represent a negative integer in binary using twos complement.

1. Convert the integer $42B$ from hexadecimal (base 16) to decimal (base 10). 

**Solution**: 
$$(42B)_{16} = 4 \times 16^2 + 2 \times 16^1 + 11 \times 16^0 = 1067$$


2. Convert the integer `11101111` from binary (base 2) to decimal (base 10). 

**Solution:** 
$$(11101111)_2 = 1 \times 2^7 + 1 \times 2^6 + 1 \times 2^5 + 0 \times 2^4 + 1 \times 2^3 1 \times 2^2 1 \times 2^1 + 1 \times 2^0 = 239$$

3. Convert the integer 445 from decimal (base 10) to binary (base 2). 

**Solution**: Using the base conversion algorithm: 

$$\begin{eqnarray*}
445 &= 2(222) + 1 \\
222 &= 2(111) + 0 \\
111 &= 2(55) + 1 \\ 
55 &= 2(27) + 1 \\
27 &= 2(13) + 1 \\
13 &= 2(6) + 1 \\
6 &= 2(3) + 0 \\
3 &= 2(1) + 1 \\
1 &= 2(0) + 1
\end{eqnarray*}$$

The algorithm halts here since the quotient is $0$ and we read the remainders off in reverse order: `110111101`. 


## Learning Target 3

Note: Work is not shown below due to math formatting limitations. For questions about your work, please bring those to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 

1. Compute `101111 + 101011`.
2. Compute `10101 - 10011`. 
3. Compute `11001` $\times$ `110`. 
4. Compute `1100111` $\div$ `11`. 

**Answers**: `1011010`; `10`; `10010110`; Quotient = `100010`, Remainder = `1`. 


## Learning Target 4

Consider the implication: **Classes will be cancelled if the roads are bad.** 

1. State the hypothesis and conclusion of this implication. Make sure to state which is which. 
2. State the converse. 
3. State the contrapositive. 
4. State the negation. 

**Answers**: 
1. Hypothesis: The roads are bad. Conclusion: Classes will be cancelled. 
2. If classes are cancelled, the roads are bad. 
3. If classes are not cancelled, the roads are not bad. 
4. The roads are bad, but class isn't cancelled. 

Note: There is no "work" to show because it asks you to "state" the answers. For questions about your work, please bring those to drop-in hours, an [appointment](http://calendly.com/robert-talbert), or email. 
