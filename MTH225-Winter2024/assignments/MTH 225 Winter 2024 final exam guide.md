# MTH 225 Winter 2024 final exam guide

## Part A

### Section 1: Multiple Choice

1. A
2. C (B is also correct but C is the most correct.)
3. B
4. C
5. B
6. B
7. E
8. E
9. B
10. A
11. A
12. A
13. A
14. E
15. B

### Section 2: Computation

1. $\displaystyle{\binom{350}{347} = \frac{350!}{347! \cdot 3!} = \frac{350 \cdot 349 \cdot 348}{3 \cdot 2 \cdot 1} = 7084700}$
2. The sequence is geometric with a common ratio of $2$. So the closed formula is $a(n) = 3(2)^n$ and a recursive definition is $a_0 = 3$ and $a_n = 2a_{n-1}$ for $n > 0$. 
3. 
| $p$ | $q$ | $r$ | $\neg p$ | $q \wedge r$ | $(\neg p) \rightarrow (q \wedge r)$ |
| --- | --- | --- | -------- | ------------ | ----------------------------------- |
| T   | T   | T   | F        | T            | T                                   |
| T   | T   | F   | F        | F            | T                                   |
| T   | F   | T   | F        | F            | T                                   |
| T   | F   | F   | F        | F            | T                                   |
| F   | T   | T   | T        | T            | T                                   |
| F   | T   | F   | T        | F            | F                                   |
| F   | F   | T   | T        | F            | F                                   |
| F   | F   | F   | T        | F            | F                                   |

4. For base 2: 
   
| Input | Quotient | Remainder |
| :---: | -------- | --------- |
|  202  | 101      | 0         |
|  101  | 50       | 1         |
|  50   | 25       | 0         |
|  25   | 12       | 1         |
|  12   | 6        | 0         |
|   6   | 3        | 0         |
|   3   | 1        | 1         |
|   1   | 0        | 1         |

So $(202)_{10} = (11001010)_2$. For base 16: 

| Input | Quotient | Remainder |
| :---: | -------- | --------- |
|  202  | 12       | 10 = `A`        |
|  12   | 0        | 12 = `C`        |

So $(202)_{10} = (CA)_{16}$.

5. (a) $\lbrace \emptyset, \lbrace a \rbrace, \lbrace b \rbrace, \lbrace c \rbrace, \lbrace a,b \rbrace. \lbrace a,c \rbrace, \lbrace b,c \rbrace , \lbrace a,b,c \rbrace \rbrace$

   (b) $\lbrace (a,1), (a,2), (b,1), (b,2), (c,1), (c,2) \rbrace$

6. (a) Incorrect

   (b) $\lbrace 1 \rbrace$ 

### Section 3: Problem Solving

1. This proof can be [found in the course vault](https://publish.obsidian.md/mth225/Recursion+and+Induction/Mathematical+induction). It's the last entry above "Resources". 
2. The base case is $n = 5$. In this case, the left side of the inequality is $4\cdot 5 = 20$ and the right side is $2^5 = 32$. Since $20 < 32$ the base case holds. Now assume that $4k < 2^k$ for some natural number $k > 5$. We want to prove that $4(k+1) < 2^{k+1}$. Start on the left side of this inequality: Algebra says that $4(k+1) = 4k + 4$. Since $k > 5$, we have $4 < 4k$, so therefore $4k+4 < 4k + 4k$. By the induction hypothesis we know that $4k < 2^k$. So $4k + 4k < 2^k + 2^k$. The right side here equals $2 \cdot 2^k$ which equals $2^{k+1}$. So, chaining all these inequalities and equations together we get: 

$$4(k+1) = 4k + 4 < 4k + 4k < 2^k + 2^k = 2^{k+1}$$

Therefore $4(k+1) < 2^{k+1}$ which is what we said we would prove. 

3. (a) The ordering of the toppings is irrelevant, so we are just choosing 3 items from a group of 11. So the total count is  $\displaystyle{\binom{11}{3} = 165}$. 

   (b) Same problem, only now there are just 10 toppings to choose from: $\displaystyle{\binom{10}{3} = 120}$. 

4. This is a dots-and-dividers problem, like the problem from class about putting copies of files into folders. Each type of donut is a "folder" and you have six "files" that you can put into each (think of a "file" as a choice to get that kind of donut). For example the diagram `**|*|***` would represent a choice of two plain, one chocolate, and three jelly donuts. Each such diagram corresponds to a bitstring of length 8 and weight 2, so there are $\displaystyle{\binom{8}{2} = 28}$ possible selections. 

5. (a) Use the Principle of Inclusion and Exclusion. The number of strings that start with `01` is $2^6$ because the first two bits are fixed but there's a free choice of two bits for the remaining 6. The number ending in a `0` is $2^7$ for similar reasons. The number that both start with `01` and end in `0` is $2^5$ again for similar reasons, and those are double counted so subtract this from the sum: $2^6 + 2^7 - 2^5 = 160$. 

   (b) The number of 8-bit strings with exactly three `1` bits is, by definition, the binomial coefficient $\displaystyle{\binom{8}{3} = 56}$. 

   (c) Having "at least" 3 bits means having exactly 3, or exactly 4, or exactly 5, or exactly 6, or exactly 7, or exactly 8. Those six conditions are disjoint, so we can use binomial coefficients to count each case and then the Additive Principle to get the total count: 

   $$\displaystyle{\binom{8}{3} + \binom{8}{4} + \binom{8}{5} + \binom{8}{6} + \binom{8}{7} + \binom{8}{8} = 56 +70 + 56 + 28 + 8 + 1 = 219}$$

   (*Alternate approach: Count the number of bit strings that have **fewer** than 3 `1` bits, and subtract this from the total number of all 8-bit strings.*)

6. (a) Treat this as a license plate problem where there are five slots to fill -- one for each point in the domain of the function. Each point in the domain has to be sent to one of seven possible destinations in the range of the function. So there are seven possible choices for each of the five blanks. Therefore the count is $7 \cdot 7 \cdot 7 \cdot 7 \cdot 7 = 7^5 = 16807$. 

   (b) If the functions are required to be injective, then no two points in the domain can map to the same point in the range. So again imagine a license plate problem with five blanks. The first blank can be filled in, in seven ways. The next blank can't have the same entry as the first one, so there are 6 ways to fill this in. The next blank after that has 5 possible entries, and so on. The total count is $7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 = 2520$. 

## Part B

### C1

1. The screen breaks
2. I will get a new phone
3. If I get a new phone, then the screen broke. 
4. If I don't get a new phone, then the screen was not broken.
5. If the screen doesn't break, I won't get a new phone. 
6. The screen on my phone broke but I did not get a new one. 

### C2 

1. The predicate $P(n)$ is the statement that $1 + 2 + \cdots + n = \frac{n(n+1)}{2}$. 
2. The base case is $n=1$. 
3. If $n=1$ then the left side of the predicate is just the one-term "sum" consisting of the number $1$. On the right, it's the fraction $\frac{1(1+1)}{2}$. This is $2/2$ which equals $1$. Since the left and right sides are equal, the base case holds.
4. Assume for some natural number $k$ that $1 + 2 + \cdots + k = \frac{k(k+1)}{2}$. 
5. Prove that $1 + 2 + \cdots + k + (k+1) = \frac{(k+1)(k+2)}{2}$. 

## C3

1. (a) True

   (b) True 

   (c) True

   (d) True 

   (e) False 

2. (a) Incorrect syntax 

   (b) $\lbrace 2, 4, 8 \rbrace$ 

   (c) $\lbrace 1, 3, 5, 7, 9 \rbrace$ 



### C4 

1. $\lbrace 2 \rbrace$
2. $\lbrace 2,3,4,5,6 \rbrace$
3. $\lbrace 4,5 \rbrace$
4. $\lbrace 2,3, 4,6 \rbrace$
5. $9$
6. $\lbrace \emptyset, \lbrace 2 \rbrace, \lbrace 4 \rbrace, \lbrace 6 \rbrace, \lbrace 2,4 \rbrace, \lbrace 2,6 \rbrace, \lbrace 4,6 \rbrace, \lbrace 2,4,6 \rbrace \rbrace$

### C5

1. $2^{19} = 524288$
2. $14 + 11 - 5 = 20$. 

### C6

1. (a) $6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720$. 

   (b) $\displaystyle{\binom{200}{198} = \frac{200!}{198! \cdot 2!} = \frac{200 \cdot 199}{2 \cdot 1} = 19900}$. 

2. Ordering is irrelevant so we are just choosing 4 items from a group of 16: $\binom{16}{4} = 1820$. 

---

Supplemental skills posted after 12:00pm ET on 2024-04-25. 

<!-- ### S1 and S2

Check your work using a [base converter](https://www.rapidtables.com/convert/number/base-converter.html) or [binary calculator](https://www.calculator.net/binary-calculator.html). 

### S3

Check your work using a [truth table tool](https://web.stanford.edu/class/cs103/tools/truth-table-tool/). 

### S4

1. (a) False

   (b) True 

   (c) False

   (d) True 

2. "All final exams are hard" 

### S5

- $a_2 = 3a_1 + a_0 = 3(1) + 2 = 5$
- $a_3 = 3a_2 + a_1 = 3(5) + 1 = 16$
- $a_4 = 3a_3 + a_2 = 3(16) + 5 = 53$
- $a_5 = 3a_4 + a_3 = 3(53) + 16 = 175$
- $a_6 = 3a_5 + a_4 = 3(175) + 53 = 578$

### S6

1. $R(1) = 3$, $R(2) = 5$, $R(3) = 8$. 
2. Each step of the pattern incorporates the previous figure  into the lower-left of the new figure and then adds a dot on the right of every previous row, plus a new dot on top in the second column. This means there are two dots added in step 2 and three dots added in step 3, and in general there will be $n$ dots added in step $n$. Therefore the recurrence relation will be $R(n) = R(n-1) + n$. 

### S7

1. Function. Domain = $\lbrace h,i \rbrace$. Codomain = $\lbrace 8,9,5 \rbrace$. Range = $\lbrace 8,9 \rbrace$. 
2. Not a function. 
3. Not a function. 
4. Function. Domain = $\lbrace f,n,v,i \rbrace$. Codomain and range = $\lbrace j,q \rbrace$. 
5. Function. Domain = $\lbrace 0,2,8,7,1 \rbrace$. Codomain = $\lbrace n,w,e,k \rbrace$. Range = $\lbrace n,w,k \rbrace$.
6. Function. Domain = $\lbrace 4,9,3 \rbrace$. Codomain and range = $\lbrace e,a \rbrace$. 

### S8

1. Bijective. 
2. Not injective since `1011` and `0011` map to `1011`. Not surjective because bitstrings like `0000` that have a leftmost bit equal to `0` will never be output. 
3. Injective, but not surjective because for example $0$ is never an output. (You would have to plug in $a = -2$ to hit it, but this is not in the domain.)

### S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 
| 1 | Neither | n/a | n/a |
| 2 | Geometric | $a(n) = 2(3)^n$ | $a_0 = 2$, $a_n = 3a_{n-1}$ |  
| 3 | Arithmetic | $a(n) = 11+n$ | $a_0 = 11$ and $a_n = a_{n-1} + 1$ | 
| 4 | Geometric | $a(n) = 100\left( \frac{1}{2}\right)^n$ | $a_0 = 100$, $a_n = \frac{1}{2}a_{n-1}$ | 


### S10 


The characteristic equation for the recurrence relation is
$$r^2 = 3r + 10$$
Getting all the terms on the left gives $r^2 - 3r - 10 = 0$. This factors into $(r-5)(r+2) = 0$ on the left, so the characteristic roots are $r = 5$ and $r=-2$. 

The framework for the solution using those roots is: 
$$a(n) = c_1 (5)^n + c_2 (-2)^n$$

Plugging in $n=0$ gives the equation $4 = c_1 (5)^0 + c_2(-2)^0$ which simplifies to $c_1 + c_2 = 4$. 

Plugging in $n=1$ gives the equation $1 = c_1 (5)^1 + c_2(-2)^1$ which simplifies to $5c_1 - 2c_2 = 1$. 

Let's use the "elimination" method for solving the system of equations. We first multiply both sides of the first equation by $2$ to get $2c_1 + 2c_2 = 8$. Now add both sides to the corresponding sides of the second equation to get $7c_1 = 9$, so $c_1 = \frac{9}{7}$. 

To find $c_2$, plug $c_1 = \frac{9}{7}$ in to $c_1 + c_2 = 4$ to get $\frac{9}{7} + c_2 = 4$. Now solve for $c_2$ to get $c_2 = \frac{19}{7}$. 

So the final solution is
$$a(n) = \frac{9}{7}(5)^n + \frac{19}{7} (-2)^n$$ -->
