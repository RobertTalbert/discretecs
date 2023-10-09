# Detailed solution for Checkpoint 4 Learning Target 7

> (**CORE**) Given a statement to prove using mathematical induction, I can state the framework of a proof. (Identify the predicate, identify and prove the base case, state the inductive hypothesis, and state what needs to be proven in the inductive step)



Suppose we want to prove the following statement using mathematical induction: 

> For all natural numbers $n \geq 1$, the sum $1 + 2 + 3 + \cdots + n$ is equal to $\dfrac{n(n+1)}{2}$. 

## Solution with details

1. *Write out the predicate involved in this statement: $P(n)$ says…*

$P(n)$ is the statement that $1 + 2 + 3 + \cdots + n$ is equal to $\dfrac{n(n+1)}{2}$. 

It's incorrect to include the quantifier "For all natural numbers $n \geq 1$" here. Once you add the quantifier this is no longer a predicate, it is a proposition. We want only the predicate. 

---

2. *What value of $n$ corresponds to the base case?* 

The base case here is when $n = 1$. (Because that's what the quantifier says.)

---

3. *Prove that the base case holds, by direct computation or demonstration*. 

We need to demonstrate that the predicate from Part 1 is true when $n=1$. Since the predicate is an equation, this means we need to find the value of the left hand side of that equation when $n=1$; then find the value of the right hand side; then see if these two are equal. 

On the left, the sum $1 + 2 + \cdots + n$ when $n=1$ would simply be the single term, $1$. 

On the right, the fraction $\frac{n(n+1)}{2}$ would be $\frac{1 \cdot 2}{2}$ which equals $1$. 

Since we get $1$ on the left and $1$ on the right, the equation is true and so is the predicate. 

---


4. *Clearly state the inductive hypothesis without using the notation "$P(n)$"*. 

Assume that $1 + 2 + 3 + \cdots + k$ equals $\dfrac{k(k+1)}{2}$ for some natural number $k$. 

Note the quantifier "for some". Saying "**for all** natural numbers" $k$ makes this incorrect. As we discussed in class, if we assume that the predicate is true *for all* natural numbers $k \geq 1$ then this is assuming that the original proposition itself is true, and so there would be no point in proving it. We are assuming that the process of verifying the predicate works *up to a point*, not "for all" numbers. 

Also note that we are not using the notation $P(n)$ but rather stating the equation in the predicate explicitly. This makes it clearer to the reader what it is we are assuming. 

---

5. *Clearly state what needs to be proven in the inductive step. Do not use the notation "$P(n)$" . You do NOT have to actually prove this statement; just state it*. 

We want to prove that $1 + 2 + 3 + \cdots + (k+1)$ equals $\dfrac{(k+1)(k+1+1)}{2}$. 

## Bonus: A completed proof

*Here is what a complete and correct induction proof of this proposition would look like. See if you can identify the framework inside this argument*. 

**Proof:** First we prove the base case, when $n=1$. On the left side, the sum is just the single number $1$. On the right, the fraction $\frac{n(n+1)}{2}$ would be $\frac{1 \cdot 2}{2}$ which equals $1$. Since the left and right sides are equal in this case, the base case holds. 

Now assume that $1 + 2 + 3 + \cdots + k$ equals $\dfrac{k(k+1)}{2}$ for some natural number $k$. We want to prove that $1 + 2 + 3 + \cdots + (k+1) = \dfrac{(k+1)(k+1+1)}{2}$. Starting on the left side, we have: 

$$1 + 2 + 3 + \cdots + (k+1)$$

The next-to-last term in this sum is $k$: 

$$1 + 2 + 3 + \cdots + k + (k+1)$$

If we group together all of the terms except the last one, we can use the inductive hypothesis: 

$$(1 + 2 + 3 + \cdots + k) + (k+1) = \frac{k(k+1)}{2} + (k+1)$$

Now we can get common denominators and add together: 

$$\frac{k(k+1)}{2} + (k+1) = \frac{k(k+1)}{2} + \frac{2(k+1)}{2} = \frac{k^2 + 3k + 2}{2}$$

The last fraction above, if you factor the numerator, is $\frac{(k+1)(k+2)}{2}$$. Therefore we have shown that $1 + 2 + 3 + \cdots + (k+1) = \dfrac{(k+1)(k+1+1)}{2}$ and so by mathematical induction, the original proposition is true for all $n \geq 1$. 
