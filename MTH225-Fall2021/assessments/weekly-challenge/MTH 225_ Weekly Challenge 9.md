---
tags: mth225, weekly-practice
---

# MTH 225: Weekly Challenge 9

:::info
**Weekly Challenges 8, 9, and 10 are deadline-free.** This means that you may submit your work whenever you believe it is ready to be assessed. However, remember there is one final deadline: *11:59pm Eastern on Sunday, December 12* which is the final deadline for all submissions and revisions of Weekly Challenge work. No submissions or revisions of Weekly Challenges will be accepted past this point. In order to give yourself enough time and space to revise your work on Weekly Challenges 8, 9, and 10, make every effort to submit a completed draft as soon as possible. 
:::




:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* You may type up your work or write it by hand on paper, whiteboard, or in a notes app. **Typewritten work is preferred** because it makes revisions easier for you.
* If you handwrite your work on paper or a whiteboard, your work needs to be **scanned to a legible, black-and-white PDF**. 
* All your work is to be submitted as a **single PDF** at the appropriate assignment area on Blackboard in the *Weekly Challenges* folder. Please do not submit multiple PDFs, or files that are not in PDF format. 


:::


** You do not need to turn in work or answers unless you want feedback on your work. 


## Application/Extension Problems 

Choose **ANY TWO (2)** of the following four problems and provide complete, clearly-written, and correct solutions for both of the ones you choose. *Do not submit work on more than two of these.* 


1. The characteristic root method we learned in class was formulated for *second*-order linear homogeneous recurrence relations. However, we can extend the technique for *third*-order linear homogeneous recurrence relations. These are linear homogeneous recurrence relations (where "linear homogeneous" means the same thing it meant for second-order recurrence relations) but where the recursion goes back three steps instead of two. An example would be: 
$$a_n = 2a_{n-1} + a_{n-2} - 2a_{n-3}$$
   The characteristic root method can be modified as follows: 
   - Convert the recurrence relation into the characteristic equation, which will now involve a *cubic* (degree 3) polynomial instead of a quadratic. 
   - Solve the characteristic equation to get the characteristic roots, which this time will be up to *three* roots. 
   - If the roots are all real numbers and are all distinct, set up a solution framework similar to the second-order case, but with three terms and three undetermined coefficients. 
   - A third-order recurrence relation requires three initial conditions; use those to create a system of *three* equations in three unknowns, and solve this system to get the final solution. 
   
   [Here is a sample solution for how this would work.](/8nMdEu1rQHGQn_Ui0dM5Ww) Following this example, solve the third-order linear homogeneous recurrence relation: 
   $$a_n = 9a_{n-1} + 4a_{n-2} - 36a_{n-3} \ \text{and} \ a_0 = 5, a_1 = 7, a_2 = 10$$
   **You may use a computer to solve the characteristic equation.** All other work must be done by hand, and all work that's perinent to the solution must be shown and clearly explained. (*Both* shown, *and* explained --- not just "shown".)  **UPDATE 2021-11-19:** If you do work on a computer, you *must* include a link to the work or a screenshot (link preferred). 

2. Recall that the Fibonacci numbers are the elements of the sequence $1,1,2,3,5,8,13,21,\dots$ where the first two terms are $1$ and $1$, and then every other term is the sum of the previous two. A recurrence relation for the Fibonacci numbers is $a_0 = 1, a_1 = 1$, and then for all $n > 1$: 
$$a_n = a_{n-1} + a_{n-2}$$
You'll notice this is a second-order, linear homogeneous recurrence relation. Use the characteristic root method to find a closed formula for the Fibonacci numbers. **You may use a computer to solve any system of linear equations.** All other work must be done by hand, and all work that's perinent to the solution must be shown and clearly explained. (*Both* shown, *and* explained --- not just "shown".)  **UPDATE 2021-11-19:** If you do work on a computer, you *must* include a link to the work or a screenshot (link preferred).

**UPDATE 2021-12-01:** You *may not* use decimals in the answer -- the closed formulas must use exact values, like $\sqrt{2}$ and not $1.41421356$. 

2. **(Python focused)** Write a Python function named `char_roots` that accepts a two-element list that represents the coefficients on a linear, second-order, homogeneous recurrence relation; and the function determines whether the recurrence relation has two real characteristic roots, a single repeated characteristic root, or two imaginary characteristic roots and the prints the information to the screen. 

   For this function, assume that if the recurrence relation is $a_n = A \cdot a_{n-1} + B \cdot a_{n-2}$, the list given to `char_roots` is `[A,B]` --- the coefficient on $a_{n-1}$  comes first, then the coefficient on $a_{n-2}$ is second. You may assume the coefficient on $a_n$ is $1$. For example, to determine the information about $a_n = a_{n-1} + 6a_{n-2}$, we would compute `char_roots([1, 6])`. 
   
   Here are some examples of inputs and outputs: 
   
    ```python
    > char_roots([1,6])
    > The recurrence relation has two real roots. 
    
    > char_roots([4,-4])
    > The recurrence relation has a single repeated root. 
    
    > char_roots([2,-4])
    > The recurrence relation has imaginary roots. 
    ```
    
    **No functions outside the standard library are needed, or allowed, on this problem.** To get started, work through the math for each of the above samples by hand. You don't need to come up with the actual solutions or even the characteristic roots --- you just need to know how many there are, and whether they are real numbers or imaginary numbers. What math are you doing? How might you make Python do that math? 

2. **(Python focused)** Write a Python function called `rr_solve` that accepts a list of *four* numbers related to the linear second-order recurrence relation
$$a_n = A \cdot a_{n-1} + B \cdot a_{n-2}, \quad a_0 = C, a_1 = D$$
The list to input is `[A,B,C,D]`: the coefficient on $a_{n-1}$, then the coefficient on $a_{n-2}$, then the initial condition for $n=0$, then the initial condition for $n=1$. The function should then **determine whether the recurrence relation has real or imaginary roots**. That information is not returned or printed. Instead, if the roots are imaginary, stop and print out that information. If the roots are real --- distinct or repeated --- then **determine the closed-form solution and print it to the screen**. 

   For example, Example 2.4.6 in your text involves the recurrence relation $a_n = 7a_{n-1} - 10 a_{n-2}$ with $a_0 = 2$ and $a_1 = 3$. The solution (found in that example) is $f(n) = \frac{7}{3}2^n - \frac{1}{3} 5^n$. In your code, this should look like: 
   ```
   > rr_solve([7,-10,2,3])
   > The solution is f(n) = 2.3333*2^n - 0.3333*5^n. 
    ```
   The function printed here is just a string. Likewise, following Example 2.4.7 in your text, we should have: 
    ```
    > rr_solve([6, -9, 1, 4])
    > The solution is f(n) = 1*3^n + 0.3333*n*(0.3333)^n. 
    ```
   And for the recurrence relation $a_n = 2a_{n-1} - 4a_{n-2}$ with $a_0 = 1$ and $a_1 = 3$, we should get: 
   ```
   > rr_solve([2, -4, 1, 3])
   > The recurrence relation has imaginary roots.
    ```
   That is, if the roots are imaginary, just stop and say so. 
   
   **For this problem you will need to use two features of the Python package called `numpy` (Numerical Python) for doing some of the math.** Here is a tutorial for how to use those features: [Numpy tutorial for Weekly Challenge 9](/I7v3HC89SXCsEPwwZ8SiZA)
   
   However **no other functions outside the standard core library are needed, or allowed.** 
   
   Please note, some leeway is allowed here for the exact appearance of your output. For example, the samples above have four decimal places; if you have more than that, it's OK. Also the phrasing of the answer doesn't have to be exactly what you see there. 
   
   Finally, **if you do the other Python problem in this Weekly Challenge** (writing the function `char_roots`) **you may use it in this problem if it helps**. In fact these two problems are mostly intended to go together as a package. 

## Feedback and Reflection 

Nothing required this time, although you are free to share any thoughts or questions you may have. 