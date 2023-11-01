# AEP 6: Counting Is Fun

## Overview and Background

Counting problems are awesome! :fire: So let's do some. 

## Tasks for this AEP

Here are three counting problems. Pick any two, and do them. (Don't turn in work on all three! It will be marked *Incomplete* and returned back to you without further comment.)

### Problem 1

This problem has three parts: 

1. How many positive integers less than 100,000,000 have exactly one digit equal to 9? (Once such integer would be 1212309. But 1212399 would *not* be an example because there are two 9's, not exactly one. Nor would 1212388 because this has no 9's.)
2. How many positive integers less than 100,000,000 have exactly *three* digits equal to 9? 
3. How many positive integers less than 100,000,000 have exactly one digit equal to 9, *and* have a sum of digits equal to 42? (An example of such a number is 8945682. A non-example would be 8990682 because although the digits add to 42, there's two 9's instead of one. Another non-example would be 798 because although there's only one 9, the digits don't add up to 42.) 

:::warning
Make sure to read the **Expectations and Grading Criteria** for allowable and non-allowable ways to solve this problem. 
:::

### Problem 2

You're hungry from a long day of doing Discrete Structures, so you head to your favorite donut shop to get a half-dozen (that is, six) donuts. The donut shop sells five different kinds of donuts: glazed, chocolate, blueberry, jelly-filled, and cake. The shop carries an unlimited supply of each of these kinds of donuts. You can get as many of each kind as you want, as long as you get only six of them in all. For example, you can get six jelly donuts; or two jelly donuts, two chocolate, and two glazed; or two cake donuts and one of each of the remaining kinds.  

How many different selections of six donuts can you make? 

:::warning
Make sure to read the **Expectations and Grading Criteria** for allowable and non-allowable ways to solve this problem. 
:::

### Problem 3

One of our original counting problems was finding out the number of ways to assign professors to offices. Let's return to that situation: 


1. How many ways are there to put six professors into four identical offices? Assume that you can leave some offices empty, and it's OK to put more than one professor in the same office. (In fact, note that it's impossible in this situation to avoid putting more than one professor in the same office because of the Pigeonhole Principle.
2. How many ways are there to put six professors into four identical offices so that none of the offices is empty? 

:::warning
Make sure to read the **Expectations and Grading Criteria** for allowable and non-allowable ways to solve this problem. 
:::

## Expectations and Grading Criteria 

Remember the general expectations and grading standards for AEPs are in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Fall2023/course-docs/standards-mth225-f23.md#standards-for-aeps) document. Make sure to review this before submitting anything and use those guidelines as a checklist to save yourself time and energy later from having to revise work that doesn't meet those standards. 

**Special requirements for this AEP:** In addition to the general expectations, this AEP has some special rules for how you may and may not approach solutions: 

- A solution that's obtained by **brute force** (using a computer, or a lot of patience, to simply list all the possible things you are counting and then manually counting them up) is *not* allowed. However, it's a very good idea to do this to *check* your work. 
- Your solution must explain **how you approached the setup of your problem**. For example, if you use the binomial coefficient -- why? If you use dots and dividers -- why? It's not enough just to have a right answer and correct computations. Explain to the reader how you got from the statement of the problem, to the selection of your tools, to the computation and then to the answer. [Review this video](https://vimeo.com/630075618) for an example of how the explanation should be done.

Solutions that are either of these will result in a mark of *Incomplete*, and your work will be returned without further comment.

When it comes to **explanations**: 

- **Keep it simple and clear.** Do not assume that the reader is a genius, has lots of experience shared with you, or wants to fill in any gaps you leave. Use plain language and make your explanations as clear as possible. 
- **General statements are not explained by examples.** For example if you think a function is injective, it means that there are no collisions from the input to the output. Explaining this, requires that you explain why collisions **never** happen with this function; a single, specific example of a collision not happening isn't convincing. However, remember that if a function **is not** injective, or is not surjective, then this *can* be explained with a single example where the property fails, so you can give that example and explain why it works. 
- **Remember the audience**. The audience is **your classmates** --- people who are smart and have all the background knowledge that a regular person in the class would have, but none of the specialized knowledge that *you* have, and no experience with your particular problem. At regular intervals, stop and ask yourself if, honestly, your explanation would be clear and convincing for that audience. If not, keep working on it. 

And remember: **The main criteria used for evaluating your work on this and most other AEPs is the *quality of your explanations, not the correctness of your answers***. It's pretty easy to get right answers; but it takes real understanding to explain why they are right. 




## Submitting your work 

**AEP submissions must be typewritten and saved as either a PDF or MS Word file. No part of your submission may involve handwriting; work that is submitted that contains handwriting will be graded N and returned without feedback.** This includes electronic handwritten docments, for example using a stylus and a note-taking app. To type up your work, you can use MS Word or Google Docs (both of which have equation editors for mathematical notation) or any other computer-based math typesetting tool. Just make sure you save your work as a Word document or PDF (no `.odt`, `.rtf`, or other file extensions are allowed).

When you have your work typed up, double-check it for neatness, correctness, and clarity. Then simply submit your document on Blackboard, in the **AEP** area, in the **AEP 6** assignment. 

There are no special additional criteria for this AEP. Although there is code to analyze in this AEP, you do not need to *write* any code for it, so a Jupyter notebook isn't necessary. If you choose to use a Jupyter notebook anyway, that's OK, just remember to set permissions on your document correctly ("Everyone with the link can comment") and turn in the link, not a PDF. 


## Getting Help

You **may** ask me (Talbert) for help on this assignment in the form of **specific mathematical or technical questions, or clarifying questions about the instructions**. If I cannot answer a question because it would give too much away, I'll tell you so. However please note: **I will not "look over your work" before you submit it to give you feedback on the overall submission**. I have made the expectations clear, so just follow those directions and submit your best work, and you'll be allowed to revise it if needed. 

For AEPs, the syllabus policy on collaboration is: 

>On AEPs, you are allowed to engage in general discussions of strategy only with others, but no collaboration on the details of a problem are allowed..
 
**You can ask technology related questions to anyone at any time**. For example if you need help figuring out how to type up your work, there are no restrictions on that. 