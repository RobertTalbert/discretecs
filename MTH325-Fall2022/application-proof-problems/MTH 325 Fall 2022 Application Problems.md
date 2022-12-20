---
tags: mth325-f22
---

# MTH 325 Fall 2022 Application Problems 

## Instructions 

First of all please note: **You do not have to do all of the problems below.** The Applications badge instructions in the syllabus only require that you complete **three different Application problems** at least one of which is a "Programming Focused" problem. We will add more problems through the semester, eventually totalling between 4 and 10 (probably 6-8). 

Some of these problems focus on writing Python code to accomplish some task. These are specifically labelled as **Programming Focused** and have a computer emoji :desktop_computer: under the problem number. 


Your job is to **find a problem that looks interesting to you and then solve it**. "Solve" here can look like different things, depending on the problem. However, *all* Application Problem solutions must be **complete, correct, and professionally presented solutions that explain why the work you did actually solves the problem**. [Please see the Specifications for Students Work in MTH 325 document](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) for precise details of what this involves. 

Among the criteria for acceptable work are these important points:

- Your work must constitute a **good-faith effort at a completed solution**. You may not write up part of a solution and leave other parts of it incomplete or blank. 
- Your work must be **free from serious errors** in computation, logic, factual knowledge, and semantics. (See the [Specifications document](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) for descriptions of those.)
- Your work must **look professional** and **explain your reasoning clearly**. Solutions that are just computations (a "wall of math" or nothing but computer code) will need to be revised. 

Some problems may have additional requirements unique to the problem. Be sure to read the problem statement carefully for any special items your solution must include. 

### Additional criteria for Programming Focused problems

In addition to the general specifications above and in the [Specifications document](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document, programming problems have these requirements: 

- **All computer code must be written in Python**. You may not use any other language (simply because I (Talbert) do not know any other language, so I wouldn't able to evaluate your work). 
- **All code must execute properly without syntax errors.** If your code produce a syntax error when it's evaluated, your work will be marked *Revise* and returned to you with no further feedback other than a note about the error. **It is your responsibility to run your code before submitting it so you can debug all syntax errors.**
- **Your solution cannot just be code --- it must also contain an explanation of your work.** If you write a program, explain what you did, how your program works, and why it will always produce the correct results. I prefer you place this explanation in text, outside the code itself rather than as comments within the code. 

Most of the time, your code will be graded by running a number of test cases through it and checking the outputs against known results. If the code does not produce the correct results on 100% of the test cases, your work will be marked *Revise* and I'll give you feedback on which test cases were causing problems. However, the debugging process will be left up to you. 

### How to submit your work 


Here are specific instructions on how to submit your work: 

- All Application Problem solutions must be **typed** using a word processor or other computer program that allows for entry of mathematical notation. Microsoft Word, Google Docs, and Open Office Writer all have built-in equation editors you can use to insert mathematical notation. You can also use LaTeX if you know how. But, **no handwritten work is accepted** -- any submission that is handwritten will be marked "Revise" and returned without any feedback on the work itself. 
- You are highly encouraged to use **Jupyter notebooks** for writing up and submitting your Application Problem solutions, especialy on Programming Focused problems, since these allow you to combine text, math notation, and code. [Google Colab](https://colab.research.google.com) is what we have used in class and is a good basic platform. I welcome all questions about how to use these! 
- Your work must be **saved as a PDF file**. Microsoft Word documents are also OK, but *no other file format is accepted* because I can't leave feedback on the submission if it's not PDF or Word. To save a Jupyter notebook on [Google Colab](https://colab.research.google.com) as a PDF, click `File > Print` and then save as PDF. 
- Put **one problem per PDF**. If you have solutions for 2-3 different problems, submit them separately in separate files. 
- When you are ready to submit your work, save it in a PDF (one problem per PDF) and **upload the PDF to Blackboard** in the *Application Problems Submission* assignment folder. **All work on Application Problems goes in this one folder** which means this one Blackboard item might have your past work on several different proofs. I leave it up to you to know which ones you have submitted. 


Once your work is submitted, I will be notified, and then I will evaluate it using our "Critical Analysis" process. If your work meets the specifications laid out in the [Specifications](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document, it will be marked *Successful* on Blackboard, and you are done with that problem. If not, it will be marked *Revise* and you will be given feedback on both the good and the not-as-good on your work, and then you can revise and resubmit again later. Note that feedback will be given regardless of the mark. 


**Deadlines:** Each Proof Problem has an **initial deadline** listed. If you intend to submit any work at all on a problem, the first attempt must be submitted before this deadline. Once you have made that initial lsubmission, there is no further deadline on revisions other than the final deadline of **Sunday December 11**. Only attempts that represent good-faith efforts at complete and correct proofs are counted as "initial submissions. For example, if you submit a partial proof just before the deadline, a "revision" of that proof that is submitted after the deadline, in which you complete the partial work, will not be accepted. 



---

## Application Problems 

### Problem 1: Is it bipartite?

*Initial deadline: Sunday, October 30 11:59pm ET* 

:::info
:desktop_computer: This is a **Programming Focused** problem. 
:::


Write a Python function called `is_bipartite` that takes as its input Python dictionary that represents a graph; and returns `True` if the graph is bipartite and `False` if the graph is not bipartite. 

Here are some examples of inputs and outputs (use them, and any others that you can make, to test your work): 

- The following dictionaries will return `True`: 
```python!=
{0:[2,3], 1:[3,4]}
{0: [3, 5], 1: [4], 2: [3, 5], 3: [0, 2], 4: [1], 5: [0, 2]}
```

- These will return `False`. Note that the first one is $K_5$ which is definitely not bipartite (why?). 

```python!=
{0: [1, 2, 3, 4], 1: [0, 2, 3, 4], 2: [0, 1, 3, 4], 3: [0, 1, 2, 4], 4: [0, 1, 2, 3]}
{0: [3, 4, 5], 1: [], 2: [4], 3: [0], 4: [0, 2, 5], 5: [0, 4]}
```

Important notes and additional requirements on this problem: 

- **This Python function should *not* use the `networkX` package, and it should not use any function or method found in the networkX package.** It should be simply a plain Python function that takes in a dictionary and produces a Boolean. Do not do `import networkx as nx` like we normally do. 
- **The code should use `return`, not `print`, to return the result.** That is, your code is not printing the words "True" or "False" to the screen; it is  `return`ing a Boolean. If you are not clear on what `return` does, [click here](https://www.geeksforgeeks.org/python-return-statement/) or review the Codecademy tutorial. 
- **The code should not use any object-oriented methodologies.** That is, it should not construct or instantiate classes. Use basic "procedural" programming methods. 
- **The function needs to be named `is_bipartite`.** Do not give it another name because this will mess up the grading process using test cases. 

Finally, note that [`networkx` already has an `is_bipartite` function](https://networkx.org/documentation/networkx-1.10/reference/generated/networkx.algorithms.bipartite.basic.is_bipartite.html), and [here is its source code](https://networkx.org/documentation/stable/_modules/networkx/algorithms/bipartite/basic.html). This source code isn't very useful for you because as you can see, the first line imports `networkx` which is forbidden in this problem. Although you can't use `networkx` functions in this problem, you can certainly use `networkx` apart from your submission, to make sure your code is producing correct results: Make up a graph, convert it to a dictionary, then run the dictionary through your code and through `networkx`'s code and see if the results agree. 

---

### Problem 2: Don't touch that dial

*Initial deadline: Sunday, October 30 11:59pm ET* 

Suppose there are six radio stations (we'll just label them "A" through "F"), and because of government restrictions and technical constraints, they cannot use the same channel if they are within 150 miles of each other. The table below shows the distances between each radio station: 



| Station | A    | B    | C   | D   | E   | F   |
| ------- | ---- | ---- | --- | --- | --- | --- |
| A        |   --   | 85     | 175    | 200    | 50    | 100    |
| B        |  85    | --     | 125    | 175    | 100    | 160    |
| C        |  175    | 125     | --    | 100    | 200    | 250    |
| D        |  200    | 175     | 100    | --    | 210    | 220    |
| E        |  50    | 100     | 200    | 210    | --    | 100    |
| F    | 100 | 160 | 250    | 220    | 100    |  --   |

So for example, station "A" and station "C" can use the same channel on the radio dial; but not station "A" and station "B" because they are too close together. 

What is the minimum number of channels needed for these six stations, and which stations could be assigned to which channels? 

:::info
Remember:
- Don't just give an answer with some supporting work --- **explain why your answer is correct using a mix of math and English.** You are not being evaluated only on the correctness of your answer, but mainly on the quality of this explanation. 
- Your audience is your class, and you need to write not only for mathemaical correctness but also for clarity. **Your solution should not only be correct, but also complete and clear.** 
- Your explanation should lead the reader from the beginning of the problem to its conclusion, like a good textbook or lecture would. 
- This is not a "Programming Focused" problem but you can choose to use Python in a supporting role if you want. 
:::

---

### Problem 3: Determining relation properties

*Initial deadline: Sunday, November 20 11:59pm ET* 

:::info
:desktop_computer: This is a **Programming Focused** problem. 
:::

We've learned in class that we can represent a relation as a directed graph, and a directed graph can be represented as an edge list. So therefore we can represent relations as ordered pairs of elements from the set that the relation uses. For example, if $A = \{1, 2, \dots 10\}$ and the relation is $a \sim b$ if and only if $a$ divides $b$, then the edge list for that relation is: 

```
[(1, 1), (1, 2), (1, 3), (1, 4), (1, 5), (1, 6), (1, 7), 
(1, 8), (1, 9), (1, 10), (2, 2), (2, 4), (2, 6), (2, 8), 
(2, 10), (3, 3), (3, 6), (3, 9), (4, 4), (4, 8), (5, 5), 
(5, 10), (6, 6), (7, 7), (8, 8), (9, 9), (10, 10)]
```

We're primarily interested in relations that have particular properties. In this problem: **Write the following three Python functions:**

- `is_reflexive`: The input is a relation on a set, given as an edge list. The function returns `True` if the relation is reflexive and `False` otherwise. (**Clarification:** Assume in this problem that there are no vertices of degree 0 -- that is, "isolated" vertices that have no edges incident with them. These would not appear in an edge list for a graph.)
- `is_symmetric`: The input is a relation on a set, given as an edge list. The function returns `True` if the relation is symmetric and `False` otherwise.
- `is_transitive`: The input is a relation on a set, given as an edge list. The function returns `True` if the relation is transitive and `False` otherwise.

You can use the edge list above as a test case; you'll find that it is reflexive and transitive but not symmetric. In fact, working out the details for why this is true, is a useful first step in figuring out an algorithm for doing it in general. 

Important notes and additional requirements on this problem: 

- **This Python function should *not* use the `networkX` package, and it should not use any function or method found in the networkX package.** It should be simply a plain Python function that takes in a list of pairs ("tuples" in Python terminology) and produces a Boolean. Do not do `import networkx as nx` like we normally do. 
- **The code should use `return`, not `print`, to return the result.** That is, your code is not printing the words "True" or "False" to the screen; it is  `return`ing a Boolean. If you are not clear on what `return` does, [click here](https://www.geeksforgeeks.org/python-return-statement/) or review the Codecademy tutorial. 
- **The code should not use any object-oriented methodologies.** That is, it should not construct or instantiate classes. Use basic "procedural" programming methods. 
- **The functions need to be named as indicated above.** Do not give them different names because this will mess up the grading process using test cases. 

And remember: 

- Do not submit just code, but also a narrative that explains what your code does and why you expect it to work each time. Please *do not* put that text as comments within the Python itself -- separate it out. 
- When you submit your work, please do not put code inside a PDF since copy/pasting doesn't work well with PDFs. Instead: Do the entire problem in a Jupyter notebook and submit that; or do it in a Jupyter notebook in Colab and create a share link to give me; or do your narrative explanation in one file and submit the code either in a separate text file or as a GitHub link. 

### Problem 4: Implementing composition

*Initial deadline: Sunday, November 27 11:59pm ET* 

:::info
:desktop_computer: This is a **Programming Focused** problem. 
:::

Write a Python function  called `square_relation` that does the following: 

- The input is a relation $r$ on the set $\{0, 1,2,3,\dots,n-1\}$ for some $n > 1$, expressed as an edge list of a digraph. 
- The output is $r^2$, the square of the relation that was input, again given as an edge list of a digraph. 

Examples: 
```python=
r = [(0,1), (1,2), (2,3)]
square_relation(r)

# The > symbol isn't actually in the output, it's just 
# there to make this look like output
> [(0,2), (1,3)] 


r = [(0,1), (2,3), (4,5)]
square_relation(r)
> [ ] 
# Returns the empty list; Why? 

r = [(0,1), (1,0)]
square_relation(r)
> [(0,0), (1,1)]
```


Important notes and additional requirements on this problem: 

- **This Python function should *not* use the `networkX` package, and it should not use any function or method found in the networkX package.** The input and output are just lists of tuples, and all the code should use Python functions in the standard library and nothing else. 
- **The code should use `return`, not `print`, to return the result.** If you are not clear on what `return` does, [click here](https://www.geeksforgeeks.org/python-return-statement/) or review the Codecademy tutorial. 
- **The code should not use any object-oriented methodologies.** That is, it should not construct or instantiate classes. Use basic "procedural" programming methods. 
- **The function needs to be named as indicated above.** Do not give them different names because this will mess up the grading process using test cases. 

And remember: 

- Do not submit just code, but also a narrative that explains what your code does and why you expect it to work each time. Please *do not* put that text as comments within the Python itself -- separate it out. 
- When you submit your work, please do not put code inside a PDF since copy/pasting doesn't work well with PDFs. Instead: Do the entire problem in a Jupyter notebook and submit that; or do it in a Jupyter notebook in Colab and create a share link to give me; or do your narrative explanation in one file and submit the code either in a separate text file or as a GitHub link. 

---

### Problem 5: A sorting algorithm for posets

Imagine you are working on a project (a software engineering project, a class project, a home improvement project, etc.) that has 20 different tasks involved. Some of those tasks might have dependencies -- they can only be completed once *other* tasks have been completed. Some tasks might be done independently of each other. But we can only work on one task at a time. How might we put the tasks in the project into a linear order, like a to-do list, so that if task "A" has to be completed before task "B", then "A" will appear before "B" in the list? 

This problem answers this question by modeling a project as a partially ordered set, and then using a sorting algorithm called **topological sorting**. 


Here is how the algorithm works in general. 

Let $P$ with the relation $\leq$ (which may not be literally "less than or equal to") be a finite partially ordered set with $n$ elements. 

- Initialize an empty list for the output. 
- While $P$ is nonempty, do the following: 
    - Choose any minimal element of $P$ and call it $a$. 
    - Set $P$ equal to $P$ with the element $a$ removed. 
    - Append $a$ to the output list in progress. 
- Once $P$ is empty, return the output list. 

:::info
**Example:** Let $P = \{1,2,4,5,12,20\}$ with the relation of "divides". We've seen in class that this relation makes $P$ a poset, and $1$ is a least as well as a minimal element. A topological sort of $P$ would look like this: 

| $P$                 | Minimal element chosen | New $P$           | Current list |
| ------------------- |:----------------------:| ----------------- | ------------ |
| $\{1,2,4,5,12,20\}$ |          $1$           | $\{2,4,5,12,20\}$ | $[1]$        |
| $\{2,4,5,12,20\}$   |          $5$           | $\{2,4,12,20\}$   | $[1,5]$      |
| $\{2,4,12,20\}$     |          $2$           | $\{4,12,20\}$     | $[1,5,2]$    |
| $\{4,12,20\}$       |          $4$           | $\{12,20\}$       | $[1,5,2,4]$  |
| $\{12,20\}$       |          $12$           | $\{20\}$       | $[1,5,2,4,12]$  |
| $\{20\}$       |          $20$           | $\{ \}$       | $[1,5,2,4,12, 20]$  |

The algorithm then terminates because $P = \emptyset$, and we get the list $[1,5,2,4,12, 20]$ as the output. 

**Especially note:** The output list has the property that if $a$ divides $b$ in the original poset, then $a$ appears before $b$ in the list. 

**Also:** After removing $1$ in the first step there are two minimal elements in the poset that remains, $2$ and $5$. We could have picked either one in step 2. The same is true after removing $4$ in step $4$; both $12$ and $20$ are minimal in the remaining poset and we can choose either one to remove in step 5. 
::: 

In this example, we have "sorted" the poset $P$ because we've taken its elements and put them in a linear ordering --- and the algorithm does it in such a way that if $a \leq b$ in the original poset then $a$ appears before $b$ in the sorted version. 

**For this problem:**


1. Use the topological sort algorithm to "sort" the poset $P = \{1, 2, 3, 6, 8, 12, 24, 36\}$ with the "divides" relation. Show all the steps, similarly to the example above. 
2. Going back to projects: Every project can be thought of as a collection of individual tasks, some of which have to be done in order, while some others are independent of each other. We can therefore think of a project as a poset: A set $T$ of tasks with the relation that $A \leq B$ if either $A = B$ or if $A$ must be completed before $B$ can be completed. Here is the Hasse diagram for the project of building a house: 
![](https://i.imgur.com/Biu0Puf.jpg)

    Use the topological sort algorithm to create a linear to-do list of tasks in this project. Show all the steps in the algorithm. ("Completion" is actually a task --- this involves doing a final walkthrough of the house and other project close-out tasks.)
3. The algorithm makes the assumption that there are actually minimal elements in the poset that we can remove. But as we've seen, sometimes elements with certain properties in a poset may not exist --- for example we can have posets without *least* elements. But, *every finite poset must have at least one minimal element*. Give a clear explanation, without using concrete examples, for why this is the case. (Does the word "finite" matter?)

### Problem 6: Finding extreme elements in a poset 

:::info
:desktop_computer: This is a **Programming Focused** problem. 
:::

For this problem, write two Python functions, `maximal_elements` and `greatest_element`, that do the following: 

- Each function accepts a partially ordered set, given as an edge list of a directed graph. (That is, the input is a relation that is reflexive, transitive, and antisymmetric. You may assume that the user is smart enough to always enter such a relation; no need to check the input.)
- `maximal_elements` returns a list that contains the maximal elements of the poset. 
- `greatest_element` returns a list containing the greatest element of the poset, or an empty list if there is no such element. 

Important notes and additional requirements on this problem: 

- **This Python function should *not* use the `networkX` package, and it should not use any function or method found in the networkX package.** The input and output are just lists of tuples, and all the code should use Python functions in the standard library and nothing else. 
- **The code should use `return`, not `print`, to return the result.** If you are not clear on what `return` does, [click here](https://www.geeksforgeeks.org/python-return-statement/) or review the Codecademy tutorial. 
- **The code should not use any object-oriented methodologies.** That is, it should not construct or instantiate classes. Use basic "procedural" programming methods. 
- **The functions needs to be named as indicated above.** Do not give them different names because this will mess up the grading process using test cases. 

And remember: 

- Do not submit just code, but also a narrative that explains what your code does and why you expect it to work each time. Please *do not* put that text as comments within the Python itself -- separate it out. 
- When you submit your work, please do not put code inside a PDF since copy/pasting doesn't work well with PDFs. Instead: Do the entire problem in a Jupyter notebook and submit that; or do it in a Jupyter notebook in Colab and create a share link to give me; or do your narrative explanation in one file and submit the code either in a separate text file or as a GitHub link. 


### :new: Problem 7: Finding optimal encoding of text 

If we have information to transmit over a digital network, it has to be translated into binary first so the computer can process it, and then transmitted. **How might we encode a text message into binary so that it uses as few bits as possible, thereby reducing transmission time and the probability of an error?** That's the question addressed in Problem 7. For this problem, you'll learn about **prefix codes** and the **Huffman code algorithm**, which uses trees and a bit of probability to encode text to binary. 

First, watch this 28-minute video that explains and demonstrates the concepts: 

<iframe title="vimeo-player" src="https://player.vimeo.com/video/776182008?h=778742702d" width="640" height="374" frameborder="0" allowfullscreen></iframe>

Then, for your work in the problem: 

- Using [the random text generator at this website](https://www.gigacalculator.com/randomizers/random-string-generator.php), create a **240 character random string** using **8 consonants and 2 vowels** of your choice. (A "vowel" is one of the letters a, e, i, o, u; a "consonant" is any of the other 21 letters of the English alphabet. We will count "y" as a consonant for this problem.) In other words you are randomly generating a tweet using your restricted alphabet. (Although it will be a nonsense string; in that sense it's not totally unlike real Twitter.) In your writeup, include a list of the letters you used and the string that you generated. Here is a screenshot of what the website looks like when set up properly: 


![](https://i.imgur.com/CdbBbzy.png)


You can choose different characters to use, but you must set the string length to 240, number of strings equal to 1, and leave all  the boxes unchecked. 

- Take your random string and determine the relative frequencies of each letter. List those separately in your writeup. 
- Then work step-by-step through the algorithm described in the video to build the Huffman coding tree for your 10-character "alphabet". Be sure to briefly explain what you are doing at each stage. (Steps without explanations will need to be revised so that there are explanations present!)
- Finally, make a real word out of the 10 characters you used, of length between 5 and 8 characters. (In the example above, for instance, you might use the word `quart`, or `shall`. But not `mathematics` because `e` is not one of the characters used.) Use your tree to encode the word into binary. Then encode the same word into binary using standard 8-bit ASCII (this is explained in the video); compare the sizes of the two encodings and briefly discuss why the Huffman code is shorter. 
