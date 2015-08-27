# MTH 325 Guided Practice: Matrices

## Overview

We've learned about relations, how to represent them, and their properties --- and the fact that sometimes the properties of relations are easier to discern if we change the representation. The next lesson in that series has to do with a very important form of representation using what is called a _matrix_. Matrices (that's the plural form of "matrix") are in themselves an extremely common and useful "discrete structure" and correspond to "arrays" that we sometimes use in computer programming. So this lesson is a side trip back to Chapter 5 of our textbook, where we will learn about matrices and specifically how to _add_ and _multiply_ matrices. We will need this information before we can talk about matrices for relations. 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ State the order of a matrix. 
+ State whether two matrices are equal. 
+ Add two matrices (that have the same order). 
+ Find the scalar multiple of a matrix. 
+ Multiply two $2 \times 2$ or $3 \times 3$ matrices. 
+ Write the identity matrix $I_n$. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Multiply any two matrices of compatible order. 
+ Compute a power of a matrix. 

## Learning resources 

To gain proficiency in the learning objectives, use the following resources. You may include other resources if you wish, in addition to or in replacement of the following. 

__Textbook__: In _Applied Discrete Structures_, read Sections 5.1, 5.2, and 5.3. Make sure to read actively, working through examples and activities as you go. 

__Video__: Watch the following videos: 

+ [Multiplying Matrices -- Example 1](https://youtu.be/sYlOjyPyX3g) (9:37)
+ [Multiplying Matrices -- Example 2](https://youtu.be/YtMYfvypgM4) (5:28) 

## Exercises

The following exercises are to be done _during_ and _following_ your reading and viewing of the resources. Work these out on paper and then enter the responses into the appropriate submission form (see Submission Instructions) by the deadline. You will receive a mark of __Pass__ if each item response shows a good-faith effort to be right and is submitted prior to the deadline. 

__NOTE:__ Since you can't enter in mathematical notation in the Google form, we will use the syntax that Sage uses for matrices. To enter a matrix into Sage, enter it as a list (with square brackets as the delimiters) whose elements are also lists, one list for each row of the matrix, all wrapped inside the command `Matrix( )`. For example, the matrix 
$$\left(\begin{array}{rrrrr}
-1 & 1 & 0 & 0 & 0 \\
0 & -1 & -3 & 8 & -4 \\
-1 & 0 & 1 & 17 & 1
\end{array}\right)$$
would be entered as `Matrix([[-1,1,0,0,0], [0,-1,-3,8,-4], [-1,0,1,17,1]])`. 

Consider the following matrices: 
$$A = \left(\begin{array}{rrr}
1 & 1 & 1 \\
-2 & -4 & -1 \\
3 & 0 & 1
\end{array}\right) \qquad 
B = \left(\begin{array}{rr}
-1 & -3 \\
1 & 1 \\
14 & 2
\end{array}\right) \qquad
C = \left(\begin{array}{rr}
0 & -12 \\
1 & 1
\end{array}\right) \qquad 
D = \left(\begin{array}{rrr}
0 & -1 & -6 \\
1 & 3 & -3 \\
0 & 7 & -1
\end{array}\right)$$

For each of the following, determine whether the operation that's presented can be computed. If it can be computed, do so, and enter the answer in the blank at the submission form using the Sage syntax described above. If not, then write "can't be computed" and be ready in class to explain why. 

1. $AD$
2. $DA$
3. $AB$
4. $BA$
5. $BC$
6. $C^2$

Note that you can use Sage to check your work here. Just open a Sage notebook in SageMath Cloud, enter each matrix using the syntax above, and use `+` to add matrices and `*` to multiply them. Watch your email for more details. 

---

There is a final item at the response form that solicits any specific mathematical questions or comments you may have about the material in the reading or viewing. If you have any specific mathematical questions, leave them in the blank. Frequently occurring questions will be addressed during the discussion time in class. Other questions (good but not frequently occurring) will be replied to in person on through email. If you have no questions, just leave that item blank.

---

## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1NH9b1T](http://bit.ly/1NH9b1T)