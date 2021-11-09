---
tags: mth225, weekly-practice
---

# MTH 225: Weekly Challenge 8

**Due on Blackboard by 11:59pm Eastern on Sunday 11/21.** 

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


## Application/Extension Problems 

Choose **any two (2) of the following four problems** to work. *Do not submit work on more than two of these.* 

1. Work Exercise #12 in [Section 2.2](http://discrete.openmathbooks.org/dmoi3/sec_seq-arithgeom.html) of your textbook. 
2. Work Exercise #13 in [Section 2.2](http://discrete.openmathbooks.org/dmoi3/sec_seq-arithgeom.html) of your textbook. 
1. Work Exercise #14 in [Section 2.2](http://discrete.openmathbooks.org/dmoi3/sec_seq-arithgeom.html) of your textbook. 
4. Write a Python function called `sequence_info` that does the following: 
  - The function takes a list as input, that contains at least the first five elements of a sequence. Giving it more than five terms is OK. 
  - The function determines if the sequence --- as given by the list that the user inputs --- is arithmetic, geometric, or neither. 
  - If the sequence is *arithmetic*, the function  prints a message to the screen stating so, and also stating what the common amount between terms is. 
  - If the sequence is *geometric*, the function  prints a message to the screen stating so, and also stating what the common ratio between terms is.
  - If the sequence is *neither arithmetic nor geometric*, the function prints a message to the screen saying so. 

Here are some sample inputs and outputs, to show what calling the function should look like and to give you sample results to check your work against. 

```
> sequence_info([1,2,3,4,5,6])
> The sequence is arithmetic with common amount 1. 

> sequence_info([2,4,8,16,32])
> The sequence is geometric with common ratio 2. 

> sequence_info([1,1,2,3,5,8,13])
> The sequence is neither arithmetic nor geometric.
```

Some assumptions and requirements for this: 

- You may assume that the user never gives an input list shorter than 5 elements, and never gives input that is not a list. 
- Your function must be called `sequence_info`. You may not rename it. (Your code will be graded by running it on a large number of test cases, and this won't work unless the name is `sequence_info`.)
- Your code must use the `print` command, not `return`, to print the information to the screen. 
- Only functions from the standard library are allowed. You may not use functions from any other modules or libraries. 

## Feedback and Reflection 

