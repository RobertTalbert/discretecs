# AEP 7: Combinatorial proofs

## Overview and Background

The last two AEPs for this course have to do with **proving mathematical statements**, which is something that professional computer scientists do (especially if they go through any schooling past their undergraduate degrees). This AEP focuses on a particular form of proof called a *combinatorial proof* that is useful and intuitive. 

## Background

In mathematics, we observe phenomena that have quantitative patterns and then try to say in clear language what is going on with those phenomena. For example, in the first week of this course, we looked at a function and sequences of numbers created using that function and tried to understand the behavior of those sequences. We often phrase our observations as **conjectures**, which are formally-stated educated guesses; and then **prove** that the conjecture is true.

A **proof** of a conjecture is a clear, correct, and convincing argument that the conjecture is true. Just like any argument, there are logical strategies that we can use to build a proof. One of those is [mathematical induction](https://publish.obsidian.md/mth225/Recursion+and+Induction/Mathematical+induction), which is the subject of AEP 8 and Learning Target 7. But there are many strategies available, including one that involves counting things. 

Here is an example. Let $x$ and $y$ be any two natural numbers. We make the conjecture that: 
$$\begin{equation*}
{x+y \choose 2} - {x \choose 2} - {y \choose 2} = xy
\end{equation*}$$

For example, if $x = 3$ and $y=2$, then the right hand side is $6$. The left hand side is 
$$\binom{5}{2} - \binom{3}{2} - \binom{2}{2}$$
The first binomial coefficient equals $10$, the second is $3$, and the third is $1$. So the left side is $10-3-1$ which is also $6$. 

But if we're trying to explain why an equation about binomial coefficients *always* works, one example alone isn't convincing. How might we *prove* it? We could try using the closed formula for the binomial coefficient on the left side, and attempt to show that 
$$\frac{(x+y)!}{2! (x+y-2)!} - \frac{x!}{2! (x-2)!} - \frac{y!}{2! (y-2)!} = xy$$
But the algebra involved seems like it would be insane. Fortunately there is a simpler approach: **interpret the left and right sides of the proposed equation as two different ways to express the solution to the same counting problem**. If we can convincingly do this, then since the two different expressions count the same set of things, they must be equal. 

Consider the following problem: You are making an outfit consisting of a shirt and pairs of pants. (A "pair of pants" is one thing, not two.) Suppose you have $x$ shirts and $y$ pairs of pants. How many outfits are possible? 

On the one hand, making an outfit means picking the shirt and then picking the pants. There are $x$ of one and $y$ of the other, and they are picked in sequence. So by the Multiplicative Principle there are $xy$ outfits possible. 

On the other hand, you can also think of picking an outfit like this: Put all your shirts and all your pants in a pile. There are $x+y$ things in that pile. Pick two of them to put on, but throw out any selection where you picked two shirts, or two pairs of pants because those aren't valid outfits. You will end up with an outfit. There are $\binom{x+y}{2}$ ways to pick two things from the combined pile. Of those, $\binom{x}{2}$ will be selections of two shirts, which have to be put back; and $\binom{y}{2}$ will be selections of two pairs of pants. Therefore the number of valid outfits is $\binom{x+y}{2} - \binom{x}{2} - \binom{y}{2}$. 

The punchline: Since $\binom{x+y}{2} - \binom{x}{2} - \binom{y}{2}$ and $xy$ both count the same set -- the set of all valid outfits -- they must be equal. 

This line of reasoning is called a **combinatorial proof**. It involves no algebra whatsoever, not really even any computation. It just involves logical reasoning two explain why two different expressions count the same set of things and therefore must be equal. 

Our (optional) textbook has more examples of combinatorial proofs in [Section 1.4](https://discrete.openmathbooks.org/dmoi3/sec_comb-proofs.html) (https://discrete.openmathbooks.org/dmoi3/sec_comb-proofs.html). If you need more examples, start there, particularly with Examples 1.4.3, 1.4.4, and 1.4.5 which all have complete proofs given. 


## Tasks for this AEP

Here are three identities, all true, that involve the binomial coefficient in some way. **Pick exactly one** and give a combinatorial proof of it. 

To do this, you will need to: 
- Devise a counting problem for which the left side and the right side of the identity are both the answer; and this counting problem must be clearly expressed and easy for an average person to grasp. 
- Explain very clearly why the left side is a solution to the counting problem. 
- Explain very clearly why the right side is also a solution to the counting problem. 

Doing these three things results in a proof. Notice **this is almost entirely verbal argumentations and explanations**. You will need mathematical notation, but your submission *will not* have a lot of computation in it, or any computation possibly. 

1. For all natural numbers $n$ and $k$ with $k \leq n$, 

$$k{n\choose k} = n{n-1 \choose k-1}$$
(This is Exercise 6 from [Section 1.4](https://discrete.openmathbooks.org/dmoi3/sec_comb-proofs.html), and there's a hint there.)

2. For all natural numbers $n$, 
$${n\choose 0} + {n \choose 1} + {n\choose 2} + \cdots + {n \choose n} = 2^n$$
(This is Exercise 14 from [Section 1.4](https://discrete.openmathbooks.org/dmoi3/sec_comb-proofs.html). In the text there are three different suggestions for how to think about this; one involves "lattice paths" which we haven't discussed in class but which is discussed in [Section 1.2 of the text](https://discrete.openmathbooks.org/dmoi3/sec_counting-binom.html). You may assume that a set with $n$ elements has $2^n$ subsets, a fact which has shown up in class a few times.)

3. For all positive integers $n$ and $k$ with $1 \leq k \leq n$, 
$$\dbinom n {k - 1} + \dbinom n k = \dbinom {n + 1} k$$


## Expectations and Grading Criteria 

Remember the general expectations and grading standards for AEPs are in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Fall2023/course-docs/standards-mth225-f23.md#standards-for-aeps) document. Make sure to review this before submitting anything and use those guidelines as a checklist to save yourself time and energy later from having to revise work that doesn't meet those standards. 

**Special requirements for this AEP:** As mentioned above, this AEP is all about **clear explanations**. There will probably not be much, if any computation done in your work here. Please note that the following criteria are in effect: 

- **Your explanation for your problem must be a combinatorial proof**: It must consist of devising a counting problem for which the left and right sides are both the correct answer. **Use of mathematical induction, the closed formula for the binomial coefficient, or the recurrence relation that defines the binomial coefficient is not allowed**. (Although if you want to try a proof using one of these tools simply as practice, please go ahead -- just don't turn it in.)
- **The counting problem you devise should be easy for the standard audience (= your classmates) to grasp**: Avoid abstract, weird, or highly technical counting situations. It's OK, in fact encouraged, to use practical everyday setups like choosing outfits from your closet. 
- **If you use another mathematical fact in your proof, you will need to explain why that fact is true or get permission from me (Talbert) to use it:** For example, in problem 2 above I mentioned that you can use the fact that a set with $n$ elements has $2^n$ subsets. If you can think of a way to use that fact in your proof, go ahead. But if you encounter some other similar mathematical fact that seems useful, either prove *that* fact as part of your explanation or ask me if it's OK to assume. (And remember you are not allowed to use the closed formula or the recurrence relation for the binomial coefficient.)

Just as a reminder, the closed formula for the binomial coefficient is 
$$\binom{n}{k} = \frac{n!}{k! \cdot (n-k)!}$$ 
And the recurrence relation that defines it is 
$$\binom{n}{k} = \binom{n-1}{k} + \binom{n-1}{k-1}$$
Again, **these are generally off limits** in this AEP. But if you believe you have a legitimate combinatorial proof of your problem but it involves one or both of these, check with me first. 


Submissions that don't follow these requirements will be marked *Incomplete* and returned to you without further comment. 



When it comes to **explanations**: 

- **Keep it simple and clear.** Do not assume that the reader is a genius, has lots of experience shared with you, or wants to fill in any gaps you leave. Use plain language and make your explanations as clear as possible. 
- **General statements are not explained by examples.** For example if you think a function is injective, it means that there are no collisions from the input to the output. Explaining this, requires that you explain why collisions **never** happen with this function; a single, specific example of a collision not happening isn't convincing. However, remember that if a function **is not** injective, or is not surjective, then this *can* be explained with a single example where the property fails, so you can give that example and explain why it works. 
- **Remember the audience**. The audience is **your classmates** --- people who are smart and have all the background knowledge that a regular person in the class would have, but none of the specialized knowledge that *you* have, and no experience with your particular problem. At regular intervals, stop and ask yourself if, honestly, your explanation would be clear and convincing for that audience. If not, keep working on it. 

And remember: **The main criteria used for evaluating your work on this and most other AEPs is the *quality of your explanations, not the correctness of your answers***. It's pretty easy to get right answers; but it takes real understanding to explain why they are right. 




## Submitting your work 

**AEP submissions must be typewritten and saved as either a PDF or MS Word file. No part of your submission may involve handwriting; work that is submitted that contains handwriting will be graded N and returned without feedback.** This includes electronic handwritten docments, for example using a stylus and a note-taking app. To type up your work, you can use MS Word or Google Docs (both of which have equation editors for mathematical notation) or any other computer-based math typesetting tool. Just make sure you save your work as a Word document or PDF (no `.odt`, `.rtf`, or other file extensions are allowed).

When you have your work typed up, double-check it for neatness, correctness, and clarity. Then simply submit your document on Blackboard, in the **AEP** area, in the **AEP 7** assignment. 

There are no special additional criteria for this AEP. Although there is code to analyze in this AEP, you do not need to *write* any code for it, so a Jupyter notebook isn't necessary. If you choose to use a Jupyter notebook anyway, that's OK, just remember to set permissions on your document correctly ("Everyone with the link can comment") and turn in the link, not a PDF. 


## Getting Help

You **may** ask me (Talbert) for help on this assignment in the form of **specific mathematical or technical questions, or clarifying questions about the instructions**. If I cannot answer a question because it would give too much away, I'll tell you so. However please note: **I will not "look over your work" before you submit it to give you feedback on the overall submission**. I have made the expectations clear, so just follow those directions and submit your best work, and you'll be allowed to revise it if needed. 

For AEPs, the syllabus policy on collaboration is: 

>On AEPs, you are allowed to engage in general discussions of strategy only with others, but no collaboration on the details of a problem are allowed..
 
**You can ask technology related questions to anyone at any time**. For example if you need help figuring out how to type up your work, there are no restrictions on that. 