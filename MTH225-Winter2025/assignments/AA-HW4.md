# Application/Analysis Homework 4

MTH 225, Winter 2025

See the course calendar for due date

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 2**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

Application/Analysis Exam 1, scheduled for Friday February 21, will consist of problems taken verbatim from all the Application/Analysis Homework sets up to that point, including this one. So it is to your strong advantage to maximize your understanding of the problems and questions you find below --- you will see these on a test later.  


---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. State the negation of these quantified predicates: 
   - (a): Every day of the week ends in "y". 
   - (b): Some months in the year have 15 days. 

2. Use the following recurrence relations to generate $a(0)$ through $a(9)$. 
   - (a): $a(0) = 3$, and for $n > 0$, $a(n) = 3a(n-1) + n^2$. 
   - (b): $a(0) = 2$, $a(1) = 5$, and for $n > 1$, $a(n) = 3a(n-1) - 2a(n-2)$. 

3. A list of binary strings is constructed using the following recursive rule: The bitstring `10` and `11` are in the list. And, for any two strings $x$ and $y$ in the list, their sum $x+y$ is also in the list. Give ten elements of the list. 

 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 


1. Consider the predicate P(x,y): "x is a proper divisor of y". (This means that $x$ divides $y$ evenly, but $x$ is not equal to $y$.) The domain is all positive integers. Which of the following correctly expresses "Every number greater than 1 has at least one proper divisor"?

   a) ∀x > 1, ∃y(P(y,x))
   b) ∀x∀y(x > 1 → P(y,x))
   c) ∃x > 1, ∀y(P(y,x))
   d) ∀x∃y(x > 1 ∧ P(x,y))

2. Given the recursive function defined as:
   ```
   f(n) = 2         if n = 0
   f(n) = f(n-1)²   if n > 0
   ```
   What is the value of f(3)?

   a) 4
   b) 16
   c) 256
   d) 65536

3. What is the negation of the statement "For all real numbers x, x > 0"?

   a) For all real numbers x, x ≤ 0. 
   b) For all real numbers x, x = 0. 
   c) There exists a real number x such that x ≤ 0. 
   d) There exists a real number x such that x > 0. 

4. Consider the following Python function whose input `lst` is a nonempty list of numbers:
 
```python
def Q(lst): 
   if len(lst) == 1: return lst[0]
   else:
      y = lst[0]
      z = Q(lst[1:])
      if y < z: return y
      else: return z
```

In the Python syntax, `len` gives the length of a list; `lst[0]` returns the first element of `lst`; and `lst[1:]` is `lst` with its first element removed. 

This function returns: 

   a) The minimum element of `lst`
   b) The maximum element of `lst`
   c) The sum of the elements of `lst`
   d) The first element of `lst`


5. If P(x): "x is a programmer" and Q(x): "x knows Python", which of the following statements is logically equivalent to ∀x(P(x) → Q(x))?

   a) ∀x(¬P(x) ∨ Q(x))
   b) ∀x(¬Q(x) → ¬P(x))
   c) ∃x(P(x) ∧ ¬Q(x))
   d) Both a and b are correct





## Problems to solve 

Both of the problems this week involve looking at recursive algorithms that do some of the computations you have seen in the course. 

1. Remember that the *greatest common divisor* of two integers is the largest integer that divides both integers. The [Euclidean Algorithm](https://publish.obsidian.md/discretecs/Computer+Arithmetic/Euclidean+Algorithm) is what we used to find $\gcd(a,b)$. Here is a recursive Python function that implements the Euclidean Algorithm: 

```python
def gcd(a,b):
   if a == 0: return b
   else: 
      return gcd(b % a, a)
```
As you can see, the function calls itself in line 4 using numbers that are smaller than the original inputs, which is the essence of recursion. Please note, the `%` indicates the [modulus operator](https://publish.obsidian.md/discretecs/Computer+Arithmetic/Modulus+operator) as usual. If you are unfamiliar with Python, please ask a question or use the web for tutorials. 

**In this problem:** Randomly generate two 3-digit positive integers and call them $a$ and $b$ (it doesn't matter which is which). Then **manually work through the code** above to find $\gcd(a,b)$. [This video has been made](https://shottr.cc/s/1GiM/SCR-20250204-o23.png) to explain what I mean by "manually work through the code". Show all your steps and give simple, brief English explanations on each step as if you were teaching this algorithm to a CIS 162 class. 




2. In Application/Analysis Homework 3, you explored the **repeated squaring** algorithm for finding the value of $b^n \\% m$. As you saw, this algorithm avoids finding $b^n$, resulting in huge savings of time and memory. Here is a recursive Python function that implements this algorithm: 

```python
def mpower(b,n,m): 
  if n == 0: 
    return 1
  elif n % 2 == 0: 
    return mpower((b * b) % m, n / 2, m)
  else:
    return mpower((b * b) % m, n // 2, m) * b % m
```

The inputs are the base $b$, the exponent $n$, and the modulus $m$. We assume that all of these are integers. We also assume $b > 0$ and $n \geq 0$ (because a negative base or a negative exponent don't work in this algorithm) and that $m \geq 2$ (because if $m=1$ or $m=0$, reducing mod $m$ wouldn't make sense). For example, in the solution guide for Application/Analysis Homework 3 I did the computation for finding the last two digits of $7^{19700710}$. To find it with this function, you would enter `mpower(7, 19700710, 100)`. 

For those unfamiliar with Python or who need a refresher: The `%` is the [modulus operator](https://publish.obsidian.md/discretecs/Computer+Arithmetic/Modulus+operator). And the double-slash `//` means integer division or floor division: It's like regular division except we only keep the quotient, and throw away the remainder. For example, `15//4` equals `3` and `100//7` equals `14`. And, the `if-elif-else` structure is a chain of if/then statements; [see this page for a tutorial](https://www.datacamp.com/tutorial/python-if-elif-else) if you need it.

**In this problem:** Generate a random three-digit integer and call it $m$. Then **manually** work through the code above to find $7^n \\% 100$. [This video has been made](https://shottr.cc/s/1GiM/SCR-20250204-o23.png) to explain what I mean by "manually work through the code". Show all your steps and give simple, brief English explanations on each step as if you were teaching this algorithm to a CIS 162 class. 