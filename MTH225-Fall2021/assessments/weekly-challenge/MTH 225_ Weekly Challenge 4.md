---
tags: mth225, weekly-challenge
---

# MTH 225: Weekly Challenge 4

**Due on Blackboard by 11:59pm Eastern on Saturday 10/2.** See "Submission Instructions" at the end of this document for details. 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 

---

:fire: **NEW INSTRUCTIONS FOR SUBMITTING WORK**

See the bottom of the document for new instructions for submitting work in Jupyter notebooks. **Handwritten work is no longer accepted except on the practice exercises** (if you choose to do them). 

:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

**Set operations:** Let $A = \{1,2,3,4,5\}$ and $B = \{0,3,6\}$. Find: 
   * $A \cup B$
   * $A \cap B$
   * $A \setminus B$
   * $B \setminus A$ 
   * $A \triangle B$ 
   * $B \times \{10, 20\}$ 

**Function basics:**

1. Here are four mappings from $\mathbb{Z}$ to $\mathbb{R}$. Which ones are functions? If one is not a function, why not? 
   * $f(n) = \pm n$
   * $f(n) = \sqrt{n+1}$
   * $f(n) = \sqrt{n^2 + 1}$
   * $f(n) = 1/(n^2 - 4)$ 
2. Here is a function $g:\{1,2,3,4\} \rightarrow \{x,y,z\}$ given as a Python dictionary: `g = [1:'x', 2:'z', 3:'x', 4:'z']`. 
   * Draw an arrow diagram that represents the function, and represent the function as a "matrix". 
   * What are the domain, codomain, and range? 

**Injective/surjective/bijective:** Here are some functions. Determine whether each one is injective, surjective, or bijective. 

1. $f: \mathbb{Z} \rightarrow \mathbb{Z}$ given by $f(n) = n-1$
2. $f: \mathbb{Z} \rightarrow \mathbb{Z}$ given by $f(n) = n^3$
3. $f: \mathbb{Z} \rightarrow \mathbb{Z}$ given by $f(n) = (3n+1) \ \% \ 4$


## Application/Extension Problems 



1. A highly efficient way to construct a list in Python is using a **list comprehension**. It allows you to make a list using set builder like notation. That makes a good way to practice your Python and your set notation at the same time! To start this problem, first read through [this short introduction to list comprehensions and their syntax](https://colab.research.google.com/drive/1mLlqmfEExYUN_Rmdz3zXcNcZFdV9Zxq7?usp=sharing). (Bonus: That's a Jupyter notebook, so you can see how to combine code and formatted text. Consider doing this yourself on this assignment!) Then, **write list comprehensions that build the following lists.**


   a) Let $A = \{x \in \mathbb{N} \, : \, x \leq 1000 \, \text{and} \, x \ \text{is divisible by 9} \}$ and $B = \{x \in \mathbb{N} \, : \, x \leq 1000 \, \text{and} \, x \ \text{is divisible by 4} \}$. (Note: "$a$ is divisible by $b$" means $b$ divides $a$ with no remainder. For example $144$ is divisible by $4$.) Write a list comprehension that produces the set $A \cup B$. 
   
   b) Using the same $A$ and $B$ sets as above, write a list comprehension that produces the set $A \cap B$. 
   
   c) Using the same $A$ and $B$ sets as above, write a list comprehension that produces the set $A \setminus B$. 
   
   d) Using the same $A$ and $B$ sets as above, write a list comprehension that produces the set $A \triangle B$.



2. We're going to use list comprehensions in Module 4 to quickly check our answers in puzzle problems involving complex counting arrangements. We will use a list comprehension to build a large set whose elements have certain properties in common, and then see how many objects are in it. In Python, you can find the length of a list using the `len` function. For example `len([1,2,3,4,10])` produces `5`. You'll practice this now. 

   a) Write a list comprehension that produces the **Cartesian product** of the sets $\{0,1,2\}$ and $\{0,1\}$. Spoiler: The list itself should look like `[(0,0), (1,0), (2,0), (0,1), (1,1), (2,1)]`. That is, it should be a list whose elements are tuples, with the first coordinate in the first set and the second coordinate in the second. That's the result; you supply the code. 

b) Write a **single line of code** that finds the cardinality of the Cartesian product of the sets $\{0,1,2,\dots,9\}$ and $\{0,1, \dots, 5\}$. Spoiler: Use the `len` function on a list comprehension. 

c) Write a **single line of code** that finds the cardinality of the Cartesian product of the sets $\{0,1,2,\dots,999\}$ and $\{0,1, \dots, 49\}$. Note that the first set has 1000 elements and the second one has 50. 

   d) Based on the previous two items, what do you think is the relationship between $|A|$ and $|B|$, and $|A \times B|$, if $A$ and $B$ are finite sets? State your guess clearly as a conjecture. Then provide one more example that verifies your conjecture. Then, give a good-faith effort at a general, universal explanation (that does not depend on specific examples) for why your conjecture is always true. 




## Feedback and Reflection 

1. What's at least one thing you did as a learner this week --- a study hack, a habit you started to build, a decision about when/where/how to study, etc. --- that you felt was particularly effective in helping you learn? (This doesn't have to be specifically for MTH 225 --- any example will do.)
2. What's at least one thing that happened this week, either something you did or something that happened to you, that kept you from learning as well as you could have? And, how will you try to remove or deal with that "blocker" this week? 
3. State at least one particularly interesting thing you learned in the class this week, or one particularly sticky question you have from the class this week.
4. (**OPTIONAL**) Any other questions or things you need to know, or let me know about? 

## Submitting your work

Your work has a mix of math, English, and Python like last week, and this will continue to be the case in coming weeks. **The preferred method for writing up and submitting work is as a Jupyter notebook that combines the text, code, and math.** Please attempt this for this Weekly Challenge. You can use any of the methods for authoring Jupyter notebooks that we have discussed (the GVSU JupyterHub, Google Colab, etc.). Please see the tutorial videos posted previously for how to work with the different kinds of cells and ask questions on Campuswire if you need further help. 

We're still working on a simple-as-possible workflow for turning Jupyter notebooks in on Blackboard. So far, the best option has been to **download your notebook as .ipynb from the "Download" menu** and then **turn in the notebook on Blackboard**. I can then download your notebooks and run them locally. This is good because I can run your code directly to see if it works. 

**Exception:** If you are needing feedback on the Practice Exercises at the beginning, it's OK to hand-write those and submit a scanned PDF. 