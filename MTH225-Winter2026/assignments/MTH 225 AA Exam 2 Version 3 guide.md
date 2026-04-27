# Solution guide for Application/Analysis Exam 2 Version 3

## Part B (Induction) 

### Option 1

The proposition is: For every integer $n \geq 0$ $5$ divides $6^n - 1$. 

**Framework:**

- The predicate $P(n)$ is the statement that $5$ divides $6^n - 1$. 
- The base case is when $n = 0$. In this case, $6^0 - 1 = 1 - 1 = 0$. Since $5$ does in fact divide $0$, the base case holds. 
- The inductive hypothesis is: Assume for some $k$ that $5$ divides $6^k - 1$. 
- The inductive step is: We want to prove that $5$ divides $6^{k+1} - 1$. 

**Proposed proof:** This time the proposed proof is fully correct. 


### Option 2

The proposition is: For every integer $n \geq 1$, $1 + 4 + 7 + \cdots + (3n-2) = \frac{n(3n-1)}{2}$. 

**Framework:**

- The predicate $P(n)$ is the equation $1 + 4 + 7 + \cdots + (3n-2) = \frac{n(3n-1)}{2}$. 
- The base case is when $n = 1$. In this case the left side of the equation is just the single term, $1$. The right side is $\frac{1(3(1)-1)}{2} = \frac{2}{2} = 1$. Since the left and right sides are equal, the base case holds. 
- The inductive hypothesis is: Assume that for some $k$, $1 + 4 + 7 + \cdots + (3k-2) = \frac{k(3k-1)}{2}$
- The inductive step is: Prove that $1 + 4 + 7 + \cdots + (3k+1) = \frac{(k+1)(3(k+1)-1)}{2}$. 

**Outline:** (There are multiple approaches here; this is just a sample.) Start with the left side of the proposed equation, $1 + 4 + 7 + \cdots + (3k+1)$. Use the inductive hypothesis to replace all but the last term with $\frac{k(3k-1)}{2}$, which would give us $\frac{k(3k-1)}{2} + (3k+1)$. Then expand and simplify to show that this equals $frac{(k+1)(3(k+1)-1)}{2}$. 

#### Grading notes on these

- On Option 2 a number of submissions had correct frameworks followed by outlines that had significant flaws. For example, some stated that we were going to prove that $(3k+1) = \frac{(k+1)(3(k+1)-1)}{2}$ which does not have a sum on the left side, even though there was a sum in the left side when stating the inductive step. Other outlines were not coherent plans for proof. Some omitted the outline altogether. 

## Part D (Counting problems)

### Option 1



### Option 2

Since the project director must be on the committee, this leaves 5 slots to fill. At least two slots must be filled by scientists. This means we could have two scientists, or three, or four, or five. Let's count each of those situations separately: 

- Exactly two scientists: There are $\binom{5}{2}$ to choose the scientists. Then there are three slots left to be filled with engineers, and $\binom{8}{3}$ ways to choose those. (Remember one engineer, the project director, has already been selected.) We choose the scientists then choose the engineers, so use the Multiplicative Principle: $\binom{5}{2} \cdot \binom{8}{3} = 10 \cdot 56 = 560$ ways to have exactly two scientists. 
- Exactly three scientists: Using similar reasoning there are $\binom{5}{3} \cdot \binom{8}{2} = 10 \cdot 28 = 280$ ways to do this. 
- Exactly four scientists: Using similar reasoning there are $\binom{5}{4} \cdot \binom{8}{1} = 5 \cdot 8 = 40$ ways to do this. 
- Exactly five scientists: Using similar reasoning there are $\binom{5}{5} \cdot \binom{8}{0} = 1$ way to do this. 

These are all disjoint outcomes so the total number of ways to get at least two scientists is $560 + 280 + 40 + 1 = 881$. 

Having formed the committee, assign the roles (from the non-project director members): There are five eligible members, so 5 ways to select the spokesperson and 4 ways to select the record for a total of 20. 

Therefore the total number of outcomes is $881 \cdot 20 = 17620$. 