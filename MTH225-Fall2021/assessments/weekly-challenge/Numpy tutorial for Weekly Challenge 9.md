---
tags: mth225, python
---


# Numpy tutorial for Weekly Challenge 9

NumPy is a package for doing numerical mathematics (as opposed to *symbolic* mathematics) in Python. You can learn all about NumPy [here](https://numpy.org/). It is pronounced NOOM-pie. NumPy is a treasure trove of mathematical methods that are highly optimized to run quickly on large sets of data. Chances are, you will be using NumPy again in the future. 

For now, for the `rr_solve` problem, you need two particular functions from NumPy. 

## `roots`

The function `roots` finds or approximates the roots of a polynomial. A "polynomial" is a mathematical expression that is a sum of multiples of powers of a variable $x$. For example $x^2 - 4x + 4$ is a polynomial and so is $r^2 - 6r + 9$. So, we have been dealing with polynomials quite a bit lately --- we have been changing recurrence relations into polynomials and then finding their roots. 

**NumPy works with polynomials by turning them into lists --- namely lists of coefficients**. For example, the polynomial $x^2 - 4x + 4$ would be, from NumPy's point of view, the list `[1, -4, 4]`. Likewise $r^2 - 6r + 9$ would be the list `[1, -6, 9]`. And going backwards, the list `[2,4,-5,7]` would correspond to the polynomial $2x^3 + 4x^2 - 5x + 7$. The variable name doesn't matter; the list tells you which power of the variable the number belongs to.[^1]

The `roots` function in NumPy takes in a list that represents a polynomial and returns a list that contains its roots. To use this function, you have first import the function into your workspace by typing `from numpy import roots`. Then you can just plug in the list to the function. 

**Example:** The polynomial $x^2 + x - 12$ has two roots, $x = 3$ and $x = -4$ which you can find by using algebra. Here's what that  looks like using the `roots` function: 

```python=
> from numpy import roots
> roots([1,1,-12])

# output
> array([-4.,  3.])
```
So, I lied a little above: The output is not really a *list* but something called an "array". This is a NumPy data structure. It's not exactly a list ([here's an in depth explanation of the differences](https://webcourses.ucf.edu/courses/1249560/pages/python-lists-vs-numpy-arrays-what-is-the-difference)) but it behaves very much like one. In particular, we can reference the elements of an array just like we can a list: 

```python=
from numpy import roots
solution = roots([1,1,-12])
print(solution[0]) # Grab the first element of the array and print it
print(solution[1]) # Grab the second element and print it

# output
-4.0
3.0
```

So, `roots` is very important for solving recurrence relations because they solve the characteristic equation that we convert the recurrence relation into. 

## `linalg.solve`

Another thing we do in solving recurrence relations is to solve *systems of linear equations*. For example, in Example 2.4.6 in your textbook, there's a solution for the recurrence relation $a_n = 7a_{n-1} - 10 a_{n-2}$ with $a_0 = 2$ and $a_1 = 3$. Eventually this requires solving the system of equations
$$\begin{align*}
a + b &= 2 \\
2a + 5b & = 3
\end{align*}$$
Although there's no details given in the example, methods you learned in high school algebra give $a = 7/3$ and $b = -1/3$. 

NumPy has tons of functions for solving linear systems. (Those in MTH 204 or MTH 205, take note!) The one to focus on here is `solve` found in the sub-library `linalg` ("linear algebra"). To load it into your workspace, enter: `from numpy.linalg import solve`. Then it's a three step process: 

1. Create a list, with two lists inside it. The first list is the coefficients of the first equation in the system, the second is the coefficients of the second equation. Call that `A` for now. 
2. Create a list with the right-hand sides of the two equations in the system. Call that `b` for now. 
3. Then enter `solve(A,b)`. The output is a NumPy array with the solution. The order matters: The first array entry goes with the variable represented by the first entry in the coefficient lists, similarly for the second. 

Here's an example that solves the system from Example 2.4.6: 

```python=
from numpy.linalg import solve
A = [[1,1], [2,5]]
b = [2,3]
solve(A,b)

# output
array([ 2.33333333, -0.33333333])  # This is a = 7/3, b = -1/3
```
As with the array that `roots` produces, we can pull out the individual elements. For example: 

```python=
A = [[1,1], [2,5]]
b = [2,3]
woot = solve(A,b)

woot[1]

# output
-0.3333333333333333
```
So this function is super useful for solving recurrence relations, because it solves the linear system that appears in the second half of the solution process once we are inputting the initial conditions. 


[^1]: NumPy does not handle symbolic variables at all. There's another big package called [SymPy](https://www.sympy.org/en/index.html) that does that, and we're not using that here.