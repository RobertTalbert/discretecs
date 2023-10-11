
# AEP 2: Analyzing Python functions

## Overview 

In this AEP, you'll extend an activity we did in class where we took some functions and methods from Python and looked at them from the point of view of mathematical functions. Here, you'll do the same, except pick some Python functions that are off the beaten path. 


**Initial deadline**: **Sunday, October 29 at 11:59pm ET**. You are allowed to spend one token to extend this deadline by 48 hours. 


## Background

In a recent class meeting, we did an activity where we took some Python functions and thought of them like mathematical functions, and determined their domain, codomain, and range and what this information means on a practical level. (The activity, with answers, can be found [here](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Fall2023/activities/Class%20activity%20October%209%20Functions.ipynb).)

This way of analyzing computer functions by treating them like mathematical functions can really help us understand the details of how those functions work and what pitfalls we might wish to avoid. Since computer languages are basically nothing but thousands of functions, there's lots to analyze! And since that class activity, we've added [injectivity](https://publish.obsidian.md/mth225/Sets+and+Functions/Injective), [surjectivity](https://publish.obsidian.md/mth225/Sets+and+Functions/Surjective), and [bijectivity](https://publish.obsidian.md/mth225/Sets+and+Functions/Bijective) to the list of properties of functions that we might care about. 

So it's time for an expansion and update of that class activity. 

 
## Tasks for this AEP

In Python, find **four built-in functions from the either the standard library or from the `math` library** that interest you. A reference for all the built-in functions in the standard library can be found here: https://docs.python.org/3/library/functions.html The `math` library functions are here: https://docs.python.org/3/library/math.html The only functions off limits are `math.gcd` and `math.floor` since those were part of the in-class activity. 

**Note: You might need to do a little research on Python data structures and data types to understand what a function does.** (This is partly the purpose of this assignment.) For example the `map` function uses another function as input --- that seems weird, and if you don't understand what that means, either commit to learning about it or pick another function. Some of the functions might be too obscure to be worth the effort; for example the `exec()` function is quite mysterious and technical, and should probably be left alone. 

For each of these four: 

1. State the function and explain in everyday terms what it does. "Everyday terms" means that you should be using nontechnical, jargon-free language. It's OK to refer to names of Python or computing concepts like "list", "for loop", etc. but remember *your audience knows the math you know, but nothing else* so keep things simple; you'll be asked to revise your explanations if they are too complicated. **Do not just copy, or mildly rephrase the documentation on the function**. Put it in your own words, in simple language that someone needing to have the documentation explained to them would find useful. 
2. Determine the domain and codomain of your function, and explain your reasoning -- again, using simple language that is as non-technical as possible. 
3. Determine the range of your function, explain your reasoning -- again, using simple language that is as non-technical as possible. 
4. Determine whether the function is injective, surjective, both (i.e. bijective), or neither and explain your reasoning -- again, using simple language that is as non-technical as possible. 
5. Explain what your results from 2-4 might mean for a programmer trying to write code to solve a problem. For example, does a failure of being injective cause any potential issues with errors or security? Does having a particular domain or codomain open up possibilities of combining the function with something else, to do something cool? Use your imagination! 

Since you will be choosing four functions and doing five things with each, that's a total of 20 responses you'll be submitting on this AEP. 

**Important:** Although this AEP does not require writing any code, it's almost 100% certain **you will need to play around with your functions first by interacting with them in a Python environment, before you are able to give a clear and simple explanation of all of its properties**. It's very difficult to simply look at a Python function and thoroughly understand what it does and how it behaves. *Play with it for a while first.* 

## Expectations and Grading Criteria

Just to reiterate what was said above, when it comes to **explanations**: 

- **Keep it simple and clear.** Do not assume that the reader is a genius, has lots of experience shared with you, or wants to fill in any gaps you leave. Use plain language and make your explanations as clear as possible. 
- **General statements are not explained by examples.** For example if you think a function is injective, it means that there are no collisions from the input to the output. Explaining this, requires that you explain why collisions **never** happen with this function; a single, specific example of a collision not happening isn't convincing. However, remember that if a function **is not** injective, or is not surjective, then this *can* be explained with a single example where the property fails, so you can give that example and explain why it works. 
- **Remember the audience**. The audience is **your classmates** --- people who are smart and have all the background knowledge that a regular person in the class would have, but none of the specialized knowledge that *you* have, and no experience with your particular problem. At regular intervals, stop and ask yourself if, honestly, your explanation would be clear and convincing for that audience. If not, keep working on it. 

And remember: **The main criteria used for evaluating your work on this and most other AEPs is the *quality of your explanations, not the correctness of your answers***. It's pretty easy to get right answers; but it takes real understanding to explain why they are right. S

Remember the general expectations and grading standards for AEPs are in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Fall2023/course-docs/standards-mth225-f23.md#standards-for-aeps) document. Make sure to review this before submitting anything and use those guidelines as a checklist to save yourself time and energy later from having to revise work that doesn't meet those standards. 



## Submitting your work 

**AEP submissions must be typewritten and saved as either a PDF or MS Word file. No part of your submission may involve handwriting; work that is submitted that contains handwriting will be graded N and returned without feedback.** This includes electronic handwritten docments, for example using a stylus and a note-taking app. To type up your work, you can use MS Word or Google Docs (both of which have equation editors for mathematical notation) or any other computer-based math typesetting tool. Just make sure you save your work as a Word document or PDF (no `.odt`, `.rtf`, or other file extensions are allowed).

When you have your work typed up, double-check it for neatness, correctness, and clarity. Then simply submit your document on Blackboard, in the **AEP** area, in the **AEP 3** assignment. 

There are no special additional criteria for this AEP. Although there is code to analyze in this AEP, you do not need to *write* any code for it, so a Jupyter notebook isn't necessary. If you choose to use a Jupyter notebook anyway, that's OK, just remember to set permissions on your document correctly ("Everyone with the link can comment") and turn in the link, not a PDF. 


## Getting Help

You **may** ask me (Talbert) for help on this assignment in the form of **specific mathematical or technical questions, or clarifying questions about the instructions**. If I cannot answer a question because it would give too much away, I'll tell you so. However please note: **I will not "look over your work" before you submit it to give you feedback on the overall submission**. I have made the expectations clear, so just follow those directions and submit your best work, and you'll be allowed to revise it if needed. 

For AEPs, the syllabus policy on collaboration is: 

>On AEPs, you are allowed to engage in general discussions of strategy only with others, but no collaboration on the details of a problem are allowed..
 
**You can ask technology related questions to anyone at any time**. For example if you need help figuring out how to type up your work, there are no restrictions on that. 