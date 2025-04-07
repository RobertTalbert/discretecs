 # Application/Analysis Exam 2 Solution Guide

[Click here for the exam form](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/assignments/Application%20Analysis%20Exam%202.pdf). 

## Multiple Choice Answers

1. **A**: Not injective, because for example $f(12) = 2$ and $f(22) = 2$. Also not surjective because the only outputs are $0, 1, 2, 3, \dots, 9$. 
2. **D**: The cardinality of the set itself is 10, and so the cardinality of the power set is $2^{10} = 1024$.
3. **B**: $A \times B$ is the set of all ordered pairs $(a,b)$ where $a \in A$ and $b \in B$. There are 10 ways to choose $a$ and 3 ways to choose $b$, so there are $10 \times 3 = 30$ ordered pairs.
4. **D**: If the two sets were completely disjoint, we would just add the two cardinalities together to get the size of the union ($10 + 14 = 24$). But there may be points in common, so we have to subtract the size of the intersection. We don't know what that size is, but subtracting it off would give something at most 24. 
5. **E**: The first two responses are standard interpretations of the binomial coefficient. (We usually say we are counting bitstrings with a certain number of `1` bits, but this is equivalent to counting the number of `0` bits.) Response (C) is incorrect because the binomial coefficient does not take order into account. 
6. **B**: This is a standard fact about the binomial coefficient. 
7. **B**: Treat the problem as a license plate situation. 
8. **A**: Again think about license plates -- there are $k$ blanks and $n$ choices per blank. 
9.  **B**: This is a standard fact about the factorial function. 
10. **B**: This is standard set terminology. 


## Problem Group 1

1. .
   - (a) The approach that gives $10^5 = 100000$ is incorrect because this quantity counts the number of ways to fill in five different boxes with 10 choices per box, like a license plate. But this assumes that only five of the ten apples are being put into the boxes, and does not account for the fact we can put more than one apple in a box. 
   - (b) Instead we use the dots and dividers method. We can think of the apples as 10 dots in a row, and we need to put 4 dividers between them to separate them into 5 boxes. The number of ways to arrange 10 dots and 4 dividers is the number of ways to choose 4 positions from the total of 14 (10 dots + 4 dividers), which is $\binom{14}{4}$. This is equal to $1001$.

2. We will prove that for all natural numbers $n$ and $k$ with $n \geq k$, $\binom{n}{k} = \binom{n}{n-k}$, and do it without induction or using the closed formula. The binomial coefficient on the left counts the number of ways to choose $k$ objects from a set of $n$ objects. The binomial coefficient on the right counts the number of ways to choose $n-k$ objects from a set of $n$ objects. But if we choose $k$ objects to keep, then we are automatically choosing $n-k$ objects to leave out. So the two quantities are equal.

## Problem Group 2

1. There are many possible examples for each of the four parts. Here are a few samples. 
    - (a) Injective, but not surjective: For each input $n$, let $f(n) = n + 1$. This is injective because if it were not injective, then there would be two different inputs $a$ and $b$ that both map to the same output, so $a+1 = b+1$. But if $a+1= b+1$ then $a=b$. It is not surjective because there is no input that gives an output of 0.
    - (b) Surjective, but not injective: For each input $n$, let $f(n) = n \\% 2$. This is surjective because the outputs are 0 and 1, and there are inputs that give both outputs. It is not injective because for example $f(0) = f(2) = 0$.
    - (c) Both injective and surjective but not the identity function: For each input $n$, if $n$ is even then map it to $n+1$; and if $n$ is odd then map it to $n-1$. This is injective because if $f(a) = f(b)$, then either both $a$ and $b$ are even or both are odd. In either case, we can show that $a = b$. It is surjective because for every output $m$, if $m$ is even then there is an input $m-1$ that maps to it; and if $m$ is odd then there is an input $m+1$ that maps to it. (A picture is more convincing, but it's hard to draw a picture on GitHub!)
    - (d) Neither injective nor surjective: For each input $n$, let $f(n) = n \\% 3$. This is not injective because for example $f(0) = f(3) = 0$. It is not surjective because there is no input that gives an output of 3.

2. .
   - (a) If letters cannot be repeated: Then it's a license plate problem with 8 blanks. Since letters can't be repeated, the first blank has 26 choices, the second blank has 25 choices, and so on. So the answer is $26 \times 25 \times 24 \times 23 \times 22 \times 21 \times 20 \times 19 = 26!/(26-8)! = 26!/18! = 62990928000$.
   - (b) Start or end in X, and letters can be repeated: There are two cases: (1) The string starts with X, and (2) the string ends with X. In the first case, the first letter is fixed as X, and the other 7 letters can be anything from A-Z. So there are $26^7$ strings that start with X. In the second case, the last letter is fixed as X, and the other 7 letters can be anything from A-Z. So there are $26^7$ strings that end with X. But we have double-counted the strings that both start and end with X, which is $26^6$. So the total number of strings is $26^7 + 26^7 - 26^6 = 2 \times 26^7 - 26^6 = 2 \times 8031810176 - 308915776 = 15728640$.
   - (c) Exactly one vowel, and letters cannot be repeated: There are 5 vowels (A, E, I, O, U) and 21 consonants. We can choose the position of the vowel in 8 ways. Then we can choose the vowel in 5 ways. Then we can choose the other 7 letters from the remaining 21 letters. So the answer is $8 \times 5 \times P(21,7) = 8 \times 5 \times (21!/14!) 8 \times 5 \times 586051200 = 23442048000$.


## Problem Group 3

1. We will find the number of strings that have exactly three a's, the number that have exactly 4 b's, then add these together -- and then subtract the number of strings that both three a's and 4 b's. 
    - Exactly 3 a's: We can choose the positions of the a's in $\binom{10}{3}$ ways. The other 7 letters can be either b or c, so there are $2^7$ ways to fill in the other letters. So the answer is $\binom{10}{3} \times 2^7 = 120 \times 128 = 15360$.
    - Exactly 4 b's: We can choose the positions of the b's in $\binom{10}{4}$ ways. The other 6 letters can be anything from a or c, so there are $2^6$ ways to fill in the other letters. So the answer is $\binom{10}{4} \times 2^6 = 210 \times 64 = 13440$.
    - Exactly 3 a's and 4 b's: We can choose the positions of the a's in $\binom{10}{3}$ ways. Then there are $\binom{7}{4}$ ways to choose the positions of the b's from the remaining 7 letters. The remaining three letters must be c's. So the answer is $\binom{10}{3} \times \binom{7}{4} = 120 \times 35 = 4200$.
    - So the total number of strings is $15360 + 13440 - 4200 = 24600$.
2. .
   - (a) Fewer than five elements: The number of subsets of a set with $n$ elements is $2^n$. The binomial coefficient $\binom{10}{k}$ counts the number of subsets of this set that have exactly $k$ elements. So the number of subsets with fewer than 5 elements is $2^{10} - \binom{10}{5} - \binom{10}{6} - \binom{10}{7} - \binom{10}{8} - \binom{10}{9} - \binom{10}{10} = 1024 - 252 - 210 - 120 - 45 - 10 - 1 = 386$. Or, you can add up binomial coefficients: $\binom{10}{0} + \binom{10}{1} + \binom{10}{2} + \binom{10}{3} + \binom{10}{4} = 1 + 10 + 45 + 120 + 210 = 386$.
   - (b) Even number of elements: The number of subsets with an even number of elements is $2^{10} - \binom{10}{1} - \binom{10}{3} - \binom{10}{5} - \binom{10}{7} - \binom{10}{9} = 1024 - 10 - 120 - 252 - 120 - 10 = 512$. Or just realize that there are $2^{10}$ subsets total, and half of them have an even number of elements and half have an odd number of elements. So the answer is $2^{10}/2 = 512$.


