---
tags: mth225, weekly-practice
---

# MTH 225: Weekly Challege 6

**Due on Blackboard by 11:59pm Eastern on Sunday 10/24.** *Note the new due date.* 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* You may type up your work or write it by hand on paper, whiteboard, or in a notes app. **Typewritten work is preferred** because it makes revisions easier for you.
* If you handwrite your work on paper or a whiteboard, your work needs to be **scanned to a legible, black-and-white PDF**. 
* **If you submit code that needs to be executed, it must be submitted as a Jupyter notebook along with a PDF copy of that notebook.** Instructions are in the tutorials [here](https://campuswire.com/c/GB1A69E25/feed/35). 
* All your work is to be submitted as a **single PDF** at the appropriate assignment area on Blackboard in the *Weekly Challenges* folder. Please do not submit multiple PDFs, or files that are not in PDF format. 


:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

**Binomial coefficient:**

- Calculate the following using the closed formula: $\binom{7}{3}$, $\binom{9}{5}$, $\binom{12}{2}$, $\binom{50}{45}$. (You can check these with a calculator, or on [Wolfram|Alpha](http://wolframalpha.com) by entering, for example, `7 choose 3`.)
- How many bit strings of length 16 have exactly seven "1" bits? 
- If you expand $(x+1)^{20}$, what is the coefficient on the $x^{15}$ term? Answer this without actually expanding $(x+1)^{20}$. 

**Permutations:**

- Calculate the following: $5!$, $10!$, $0!$, $P(10,4)$, $P(5,5)$, $P(50,45)$. (You can check these with a calculator, or on [Wolfram|Alpha](http://wolframalpha.com) -- the factorial can be typed in directly, and $P(n,k)$ can be entered using the formula.) 
- In the game of basketball, five people play for each team at any given time. Three of the positions are *center*, *forward*, and *guard*. If a basketball team has 12 players, how many ways are there to choose three players and assign them to these three positions? 

**Stars and bars:**

- After gym class you are tasked with putting 13 identical dodgeballs away into 5 bins. How many ways can you do this if there are no restrictions on how you put the balls away? 
- How many *natural number* solutions are there to the equation $x_1 + x_2 + x_3 + x_4 + x_5 = 13$? Remember $0$ is considered to be one of the natural numbers. 

## Application/Extension Problems 

For this Weekly Challenge, **choose exactly three (3) of the following problems and work them**. *Do not attempt work on all five of the problems given.* Submissions that have more than three problems attempted will be marked Incomplete (IC) and returned to you for correction without feedback. 

:::info
**What does a complete and correct solution to a counting problem look like?**   In order to earn a *Satisfactory* mark on work that involves solutions to mathematical problems like the ones below, each solution should: 

- Have a **single correct answer that is clearly indicated** in the work. 
- But not only that: **All significant steps that lead to the answers must be correct and clearly shown in the writeup.** The reader should not have to do any extra work to fill in missing steps other than basic arithmetic. 
- But not only that: **The solution must have an English narrative explanation** that sets up the problem strategy, explains the choices made during the solution, and explains why the mathematical work that's done is correct. 
- And finally: **The entire package must look professional**. Handwritten work, while technically acceptable, has to be neat and organized as if you were submitting it as a formal report to your employer for an important project. It's much better if you can type it rather than handwrite it; typed up solutions are also *much* easier to revise. 


Your solutions in other words **cannot just be calculations or answers**. They must be complete solutions that **not only produce right answers but explain the reasoning process clearly**. Your audience for this explanation is **your classmates** --- someone at your level of understanding of discrete mathematics but who may not be familiar with the specific problem you are explaining. 


To see what a good solution looks like and also what bad solutions look like, I've prepared an example of each for a single counting problem from the textbook. :fire:  [Click here to view those solutions.](/jW0h25STTW6LoTz1qvHzmg)  :fire:
:::

1. A coin is flipped twelve times and each flip comes up heads or tails.
   a) How many possible outcomes are there in all? 
   b) How many possible outcomes contain exactly four "heads"? 
   c) How many possible outcomes contain at least four "heads"? 
   d) How many possible outcomes contain the same number of "heads" as "tails"? 
2. When the numbers 1 through 100000 are written out, how many times is the number 3 used? (*Example: If you wrote the numbers 1 throuh 30 out, you would use the number 3 four times*.)
4. A *chord* of a polygon is a line segment that connects two vertices that are not adjacent. If a polygon has $100$ vertices, how many chords are possible? (Note, we are assuming that the polygon is *convex*, i.e. every chord is contained in the interior. [Here's more on what that means](http://www.differencebetween.info/difference-between-convex-and-non-convex). )  *To approach this problem, try starting with something simpler --- like a polygon with 5 vertices, or 8, or 10. Look for patterns in how you are counting the chords.* 
5. *(For those interested in writing some code)* Let $L(a,b)$ be the number of lattice paths from $(0,0)$ to $(a,b)$ where $a,b$ are natural numbers. For example $L(5,0) = 1$ and $L(1,1) = 2$. In class, you came up with a recurrence relation for $L$ that related $L(a,b)$ to previously-calculated values of $L$. You also found two initial conditions on $L$: $L(a,0) = 1$ and $L(0,b) = 1$ for any $a,b$. Write a *recursive* Python function `L` that accepts two natural numbers `a,b`; the function should use recursion with the recurrence relation here, to produce the correct value of $L(a,b)$. **Do not** use the closed formula that involved the binomial coefficient in your Python code --- use only the recurrence relation from class. You can use the closed formula to check that your code is computing the right values if you want (in fact that is a smart idea). **If you choose this option, put your code in a Jupyter notebook and submit it and a PDF version of it along with any other work you have.** (You can type up your other problems in the Jupyter notebook to save on files.) 
6. Here's a mysterious Python function called `Q` that accepts two natural numbers `a,b` as input and then does... something. What is this function computing? Study the function and its output. Then make a conjecture about what it does --- then give a clear, correct, and convincing argument for why your conjecture is always right. Remember **examples are necessary to understand the problem, but your explanation must work apart from those examples.** 
```python=
def Q(a,b):
   Q = 1
   for i in range(2, a+1):
      Q = Q * i
   for j in range(2, a-b+1):
      Q = Q // j  # Remember // means integer division
   return Q
```


## Feedback and Reflection 

1. What's at least one thing you did as a learner this week --- a study hack, a habit you started to build, a decision about when/where/how to study, etc. --- that you felt was particularly effective in helping you learn? (This doesn't have to be specifically for MTH 225 --- any example will do.)
2. What's at least one thing that happened this week, either something you did or something that happened to you, that kept you from learning as well as you could have? And, how will you try to remove or deal with that "blocker" this week? 
3. State at least one particularly interesting thing you learned in the class this week, or one particularly sticky question you have from the class this week.
4. *(Optional)* Ask me any question, about the class or the material or anything else. 