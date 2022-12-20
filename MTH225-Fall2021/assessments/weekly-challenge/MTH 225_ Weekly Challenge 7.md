---
tags: mth225, weekly-challenge
---

# MTH 225: Weekly Challenge 7

**Due on Blackboard by 11:59pm Eastern on Sunday 11/7.** 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* You may type up your work or write it by hand on paper, whiteboard, or in a notes app. **Typewritten work is preferred** because it makes revisions easier for you.
* If you handwrite your work on paper or a whiteboard, your work needs to be **scanned to a legible, black-and-white PDF**. 
* **If you do problem 4, it must go in a Jupyter notebook** so the code can be tested without copy/pasting. 
* All your work is to be submitted as a **single PDF** at the appropriate assignment area on Blackboard in the *Weekly Challenges* folder. Please do not submit multiple PDFs, or files that are not in PDF format. 


:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

:::info
This week, since we've covered no new material in the last few days, instead of giving you new Practice Exercises **please go back and look at earlier Weekly Challenges and their practice exercises.** Start with [MTH 225: Weekly Challege 6](/OK7bar-SSTauVp4JU-oW5A) and work your way backwards. **I will give feedback on any practice exercise from an earlier Weekly Challenge that you submit.** Just be sure to indicate where it's coming from. 
:::

## Application/Extension Problems 

Choose **any two (2) of the following four problems** to work. *Do not submit work on more than two of these.* 

1. This problem returns to an idea we started discussing in class two weeks ago but never got around to finishing: How to count the number of anagrams of a word that contains duplicate letters. Remember an "anagram" of a word is just a rearrangement of the letters in the word. 
   a) How many anagrams are there of the word "grand"? Show your work and answer, and explain your reasoning. **Attain your answer by using a counting argument, not by just listing the anagrams out using brute force.**
   b) How many anagrams are there of the word "valley"? Show your work and answer, and explain your reasoning. Again, use a counting argument and not brute force. 
   c) How many anagrams are there of the word "anagram"? Show your work and answer, and explain your reasoning. Again, use a counting argument and not brute force. 
   d) How many anagrams are there of the word "tattooist"? Show your work and answer, and explain your reasoning. Again, use a counting argument and not brute force. 
   e) Now it's time to generalize. If you are given a word that is $n$ letters long, with some of the letters repeated, how would you go about finding the number of anagrams of that word? Give a **precise, complete, and correct** algorithm for doing so. By "algorithm" we mean a detailed set of instructions on how to take the input (in this case, the word) and produce the output (in this case, the number of anagrams). Your algorithm should be a complete set of instructions that a reader can use to make this calculation given any word whatsoever. **Don't be vague.** Your algorithm should almost be computer code in its precision and specificity --- think of it as computer code for humans. *Your work will be evaluated by me (Talbert) taking a random word and seeing if I can follow your algorithm step by step and attain a correct result*. 
   
2. a) How many positive integers less than 1000000 have exactly one digit equal to 9? (Once such integer would be 109. But 199 would *not* be an example because there are two 9's, not exactly one.)
   b) How many positive integers less than 1000000 have exactly one digit equal to 9, *and* have a sum of digits equal to 13? (For example, the sum of the digits of the number 793 is 19, so this would *not* be counted even though it has exactly one 9.)
   
3. a) How many ways are there to put six professors into four identical offices? Assume that you can leave some offices empty, and it's OK to put more than one professor in the same office. (In fact, note that it's impossible in this situation to avoid putting more than one professor in the same office because of the Pigeonhole Principle.)
   b) How many ways are there to put six professors into four identical offices so that none of the offices is empty? 

4. Write a Python function called `distribute` that accepts two natural numbers `a` and `b` as input, and returns the number of ways to distribute $a$ identical objects to $b$ different bins. Here are some sample inputs and outputs, to show you two correct computations as well as to demonstrate what the function should look like when used: 

```
> distribute(5,5)
> 126   

> distribute(10,8)
> 19448
```

For this problem: You may assume that the user always inputs natural numbers. (So you don't need to include code that checks for correct input types.) If your function returns floating point numbers instead of integers (for example 126.0 instead of 126) that's OK. **Here are some requirements for your work:**

- Your function must be an actual Python function, with a `def` statement in the first line and not just a block of code. And it must be called `distribute` -- you may not name it something else. 
- As always, your function must compile properly when run --- no syntax errors should happen when you run it. **Test your code out first** to avoid this. 
- Your function must use `return`, not `print`, to return the result. 
- You may not use libraries outside the standard library; the function must execute and produce results without having to load anything extra. In particular, you may not use any function from `math`, `scipy`, or `numpy`. 
- You must include *not only* code, **but also an explanation** that explains what your code does and why it will always produce the correct result. *Do not put this explanation in your code as comments* but instead **put the code in a code block in a Jupyter notebook and the explanation in a Markdown cell separate from the code.** 


## Feedback and Reflection 

This week instead of doing the usual questions, please answer the questions on this survey: 

https://docs.google.com/forms/d/e/1FAIpQLSdUVPIZSGFtIJJ52LvEtkK78mTqLp6aj3jkhWlOrUe6wsOXlQ/viewform