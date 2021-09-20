---
tags: mth225, weekly-challenge
---

# MTH 225: Weekly Challenge 3

**Due on Blackboard by 11:59pm Eastern on Saturday 9/25.** See "Submission Instructions" at the end of this document for details. 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* You may type up your work or write it by hand on paper, whiteboard, or in a notes app. **Typewritten work is preferred** because it makes revisions easier for you.
* If you handwrite your work on paper or a whiteboard, your work needs to be **scanned to a legible, black-and-white PDF**. 
* All your work is to be submitted as a **single PDF** at the appropriate assignment area on Blackboard in the *Weekly Challenges* folder. Please do not submit multiple PDFs, or files that are not in PDF format. 
:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

**Predicates and quantifiers:** 

1. Let $P(x)$ be the statement, $x^2 = x$. The domain is the set of all integers. State the truth values of the following: 
   - $P(0)$
   - $P(1)$
   - $P(2)$
   - $P(-1)$
   - $\exists x P(x)$
   - $\forall x P(x)$
2. Let $M(x)$ be the predicate "$x$ has visited Michigan's Adventure" where the domain is the set of all students at GVSU. State each of the following in English, then give their truth values (or at least, what you *think* their truth values are): 
   - $\exists x M(x)$
   - $\forall x M(x)$
   - $\neg \exists x M(x)$
   - $\neg \forall x M(x)$ 


**Sets and set notation:** 

1. Use set-builder notation to give a description of each of these sets. There's more than one way to do each one. 
   - $\{0, 3, 6, 9, 12\}$
   - $\{-3, -2, -1, 0, 1, 2, 3\}$
2. Write each of these sets in roster notation: 
   - $\{ x \in \mathbb{R} \, : \, x^2 = 1\}$
   - $\{ x \in \mathbb{N} \, : \, x < 12\}$
   - $\{ x \, \% \, 10 \, : \, x \in \mathbb{N}\}$
3. Determine whether the number $2$ is an element of each of the following sets: 
   - $\{x \in \mathbb{R} \, : \, x > 1\}$ 
   - $\{x \in \mathbb{R} \, : \, x^2 \ \text{is an integer}\}$
   - $\{2 ,\{2\}\}$
   - $\{\{2\}, \{2, \{2\}\}\}$
5. Determine whether these statements are true, or whether they are false: 
   - $0 \in \emptyset$ 
   - $\emptyset \in \{0\}$ 
   - $\{0\} \subseteq \emptyset$
   - $\emptyset \subseteq \{0\}$
   - $\{0\} \subseteq \{0\}$


## Application/Extension Problems 


1. We mentioned in the videos and in class that a predicate can be thought of as a tiny computer program, that accepts input of a certain type from the user and outputs only Boolean values --- that is, only `TRUE` or `FALSE`. That means we can use Python to study predicates and quantifiers, by writing them as Python functions. Some examples were given in the videos. Here are some more. Each one is called `P`, and the domain of each is the set of all integers (positive, negative, and zero). For each, determine if $\exists x P(x)$ is true or whether it is false; then give a valid explanation why. Then, do the same for $\forall x P(x)$. **Remember that the main focus of your work is the explanation.** Give an explanation on each answer that fully explains your reasoning. 

```python=
# Refer to this as Problem 1(a). 
def P(x): 
    return x**2 >= 0
```

```python=
# Refer to this as Problem 1(b). 
def P(x):
    return x**2 = 2
```

```python=
# Refer to this as Problem 1(c). 
def P(x):
    return (x**2 + 2) > 1
```


2. Now it's your turn to **write** some Python. Write Python code for predicates, like the ones above, that do the following. 
   - A predicate `P` that accepts integers as input and returns `TRUE` for all odd integers but `FALSE` for evens. 
   - A predicate `Q` that accepts integers as input returns `TRUE` if the input is an integer that is equal to 0 mod 2 but not equal to 0 mod 8; and returns `FALSE` otherwise. 
   - A predicate `R` that accepts strings as input and returns `TRUE` if the string has an odd number of characters. 

3. Write a predicate `S`, as a Python function, that accepts a string as input, and then returns a Boolean based on some condition of your choice that involves the string. The predicate `R` in the previous question is an example; it looks at the length of the string and returns a Boolean based on the results. You can create any similar condition you want; but *you may not use the length of the string* this time because the previous question already did something like that. [This website](https://www.w3schools.com/python/python_ref_string.asp) contains a huge list of Python string methods that you can select from. Play with them, then write a predicate that involves one or more of them. **Then**: determine which of the following are true statements and give an explanation: 
   - $\forall x S(x)$ 
   - $\exists x S(x)$
   - $\forall x \neg S(x)$ 
   - $\exists x \neg S(x)$ 


:::warning

**Rule for Python:** Whenever you submit Python code for grading, **it must execute without syntax errors. Code that throws a syntax error upon evaluation will result in an "Incomplete" mark *for the entire assignment.* It is your responsibility to run your code before submitting it and catch/debug all syntax errors.** 

For example this code would produce a syntax error. Why? 

```python=
def P(x)
    return x = x**2
```
---


**How to submit Python code:** You can do this in several different ways for now. Eventually we'll narrow these down, but this time you can do any of these: 

- Write up your code in a Jupyter notebook and submit it on Blackboard. *This is the preferred method* since the Jupyter notebook actually allows me to execute your code right in the document to check for errors. Some instructions for accessing Jupyter notebooks will be posted to Campuswire this week. 
- Write up your code in a Jupyter notebook on Google Colab and submit the link to it, as you would a Google Doc. Instructions on this will be in the aforementioned Campuswire post. 
- Write up your code in a text file and submit it on Blackboard. 
- Write up your code in a single [GitHub Gist](https://gist.github.com/) and submit the link on Blackboard. 

:::




## Feedback and Reflection 

**From now on, you'll be getting the same questions every week for Weekly Challenges.** So you can be collecting your thoughts on these, all week. 

1. What's at least one thing you did as a learner this week --- a study hack, a habit you started to build, a decision about when/where/how to study, etc. --- that you felt was particularly effective in helping you learn? (This doesn't have to be specifically for MTH 225 --- any example will do.)
2. What's at least one thing that happened this week, either something you did or something that happened to you, that kept you from learning as well as you could have? And, how will you try to remove or deal with that "blocker" this week? 
3. State at least one particularly interesting thing you learned in the class this week, or one particularly sticky question you have from the class this week.