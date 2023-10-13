# Detailed solution for Checkpoint 5 Learning Target 7

> (**CORE**) Given a statement to prove using mathematical induction, I can state the framework of a proof. (Identify the predicate, identify and prove the base case, state the inductive hypothesis, and state what needs to be proven in the inductive step)



Suppose we want to prove the following statement using mathematical induction: 

> For all natural numbers $n \geq 1$, $n <, 2^n$. 

## Solution with details

1. *Write out the predicate involved in this statement: $P(n)$ says…*

$P(n)$ is the statement that $n < 2^n$. 

It's incorrect to include the quantifier "For all natural numbers $n \geq 1$" here. Once you add the quantifier this is no longer a predicate, it is a proposition. We want only the predicate. 

---

2. *What value of $n$ corresponds to the base case?* 

The base case here is when $n = 1$. (Because that's what the quantifier says.)

---

3. *Prove that the base case holds, by direct computation or demonstration*. 

We need to demonstrate that the predicate from Part 1 is true when $n=1$. Since the predicate is an inequality, this means we need to find the value of the left hand side of that inequality when $n=1$; then find the value of the right hand side; then see if the left is less than the right. 

On the left, we just have $n$, which is $1$ for the base case. 

On the right, we have $2^n$ which is $2^1 = 2$. 

Since we get $1$ on the left and $2$ on the right, and $1 < 2$, the inequality is true and so is the predicate. 

---


4. *Clearly state the inductive hypothesis without using the notation "$P(n)$"*. 

Assume that $k < 2^k$ for some natural number $k$. 

Note the quantifier "for some". Saying "**for all** natural numbers" $k$ makes this incorrect. As we discussed in class, if we assume that the predicate is true *for all* natural numbers $k \geq 1$ then this is assuming that the original proposition itself is true, and so there would be no point in proving it. We are assuming that the process of verifying the predicate works *up to a point*, not "for all" numbers. 

Also note that we are not using the notation $P(n)$ but rather stating the inequality in the predicate explicitly. This makes it clearer to the reader what it is we are assuming. 

---

5. *Clearly state what needs to be proven in the inductive step. Do not use the notation "$P(n)$" . You do NOT have to actually prove this statement; just state it*. 

We want to prove that $(k+1) < 2^{k+1}$.  

## Bonus: A completed proof

*Here is what a complete and correct induction proof of this proposition would look like. See if you can identify the framework inside this argument*. 

**Proof:** First we prove the base case, when $n=1$. On the left side, we have $n = 1$. On the right, we have $2^n = 2^1 = 2$. Since $1 < 2$, the base case holds. 

Now assume that $k < 2^k$ for some natural number $k$. We want to prove that $k + 1 < 2^{k+1}$. We will start on the left side and build a chain of equations and inequalities resulting in the right side. 

First, note that since we proved the proposition to be true when $n=1$, we can assume that $k \geq 2$. Therefore, 
$$k + 1 < k + k$$
The right side here is $2k$. But we assumed in the inductive hypothesis that $k < 2^k$, so 
$$2k < 2 \cdot 2^k$$ 
The right side here is $2^{k+1}$ through basic algebra. Putting all this together, we have shown:
$$ k + 1 < k + k = 2k < 2 \cdot 2^k = 2^{k+1}$$
Therefore $k+1 < 2^{k+1}$. So by mathematical induction, $n < 2^n$ for all $n \geq 1$. 