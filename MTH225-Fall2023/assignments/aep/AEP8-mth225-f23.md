# AEP 8: Proof using mathematical induction 

## Overview and Background

The last two AEPs for this course have to do with **proving mathematical statements**, which is something that professional computer scientists do (especially if they go through any schooling past their undergraduate degrees). This AEP focuses on proof using **mathematical induction**, a method of reasoning that we introduced earlier in the course but only discussed the "framework" of a proof. Here, you'll have a chance to actually *write proofs* with this method. 

## Background

In mathematics, we observe phenomena that have quantitative patterns and then try to say in clear language what is going on with those phenomena. For example, in the first week of this course, we looked at a function and sequences of numbers created using that function and tried to understand the behavior of those sequences. We often phrase our observations as **conjectures**, which are formally-stated educated guesses; and then **prove** that the conjecture is true.

A **proof** of a conjecture is a clear, correct, and convincing argument that the conjecture is true. Just like any argument, there are logical strategies that we can use to build a proof. One of those is [mathematical induction](https://publish.obsidian.md/mth225/Recursion+and+Induction/Mathematical+induction), which is the subject of this AEP and Learning Target 7. 

The vault article linked above contains a complete description of mathematical induction, the framework for an induction proof, and three worked examples of proofs. There are many, many more worked examples of proofs online as well for you to study. 

As a reminder, mathematical induction is a particular form of argumentation that works well with conjectures about **predicates that are true "for all natural numbers"** (or some subset of the natural numbers) and in which **recursion has a significant role**. Induction proofs use the recursion that is involved to create the argument, using this framework: 

1. Identify the predicate involved and the value of the variable used in the **base case**, then show by direct computation or demonstration that the base case holds. 
2. State the **induction hypothesis** which is just an assumption that the predicate is true for some undisclosed but specific value of the variable. 
3. Then state the **inductive step** which is just a clear statement of what needs to be proven based on the induction hypothesis. This is nothing more than stating that you want to prove that the predicate is true in the step that follows the one in the inductive hypothesis. 

To actually carry out the proof indicated in the inductive step requires some ingenuity and creativity, as well as a strong grasp of the meaning of the predicate you are working with and the recursion that's involved. Induction proofs can look quite different, so again study the three that are in the vault as well as any others you can find. 


## Tasks for this AEP

Below are three propositions that can be proven with mathematical induction. **Choose exactly one** and give a complete, correct, clear proof using mathematical induction. 

Your proof must:

- **Be a proof by mathematical induction**. There could be other ways to prove the result, but yours should be a proof by induction. 
- **Have the three-step framework clearly stated somewhere in the proof.** A reader should be able to scan your writing and see the framework. 
- **Be clearly written**, so that the average reader can follow it from start to finish with no questions and no need to do extra work. 
- **Be free of mathematical and logical errors.** 



1. Prove that, for all positive integers $n$, the following equality holds for the binomial coefficient: 

$$\binom{n}{0}2^0 + \binom{n}{1}2^1 + \binom{n}{2}2^2 + \cdots + \binom{n}{n}2^n = 3^n$$

(Reminder, this is to be proven by mathematical induction. *Do not attempt to apply the closed formula for the binomial coefficient!* You won't get anywhere, because the algebra is off the rails.)

2. For all natural numbers $n$, 
$${n\choose 0} + {n \choose 1} + {n\choose 2} + \cdots + {n \choose n} = 2^n$$
(This property of the binomial coefficient also appeared in AEP 7 where you're asked to give a combinatorial proof. If you select this for AEP 8, you'll need to give a new proof that uses mathematical induction.)

3. The **logarithm base 2** of a number $x$, written $\log_2(x)$, is the power to which you would raise $2$ in order to get $x$. That is, if $\log_2(x) = a$ then $2^a = x$. For example, $\log_2(8) = 3$, $\log_2(1024) = 10$, $\log_2(1) = 0$, and (using a calculator) $\log_2(100)$ is around $6.644$. 

Prove that, for all positive integers $n$, the number of bits needed to represent $n$ in binary (base 2) is $1 + \lfloor \log_2(n) \rfloor$, that is, the logarithm base 2 of $n$ rounded down to the next lowest integer, plus 1. (The notation $\lfloor x \rfloor$ is the *floor function*.) 

For example, this result would say that the number of bits needed to represent the decimal integer 782 in binary is $\lfloor \log_2(782) \rfloor + 1$ which [according to a calculator](https://www.wolframalpha.com/input?i=floor%28log2%28782%29%29+%2B+1) is **10 bits**. And indeed we can check that this number in base 2 is `1100001110` which has 10 bits. 

You may use any fact about logarithms that you might have learned in the past, for example in high school or in MTH 122. The three most popular logarithm properties are: 

- For any nonnegative numbers $x$ and $y$, $\log_2(xy) = \log_2(x) + \log_2(y)$.
- For any nonnegative numbers $x$ and $y$, $\log_2(x/y) = \log_2(x) - \log_2(y)$.
- For any nonnegative numbers $x$ and $a$, $\log_2(x^a) = a \log_2(x)$. 



## Expectations and Grading Criteria 

Remember the general expectations and grading standards for AEPs are in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Fall2023/course-docs/standards-mth225-f23.md#standards-for-aeps) document. Make sure to review this before submitting anything and use those guidelines as a checklist to save yourself time and energy later from having to revise work that doesn't meet those standards. 

**Special requirements for this AEP:** As noted above: 

- **Your solution must be a  proof by induction**: Use of the closed formula for the binomial coefficient, or the recurrence relation that defines the binomial coefficient, or another form of proof is not allowed.
- **Your proof must have the three-step framework clearly stated somewhere in the proof.** A reader should be able to scan your writing and see the framework. 
- **Your proof must be clearly written**, so that the average reader can follow it from start to finish with no questions and no need to do extra work. 
- **Your proof must be free of mathematical and logical errors.** Note, some "simple" or trivial errors might not impact the proof and would be permitted -- you'd get feedback about it but these by themselves wouldn't trigger a revision. 

Just as a reminder, the closed formula for the binomial coefficient is 
$$\binom{n}{k} = \frac{n!}{k! \cdot (n-k)!}$$ 
And the recurrence relation that defines it is 
$$\binom{n}{k} = \binom{n-1}{k} + \binom{n-1}{k-1}$$

Whereas in AEP 7, these formulas were off-limits, here you are welcome to use either one of these since they are fundamental representations of the Binomial Coefficient. But be careful of the closed formula, as it often doesn't work well with an induction proof and tends to create more work than it alleviates. 


Submissions that don't follow these requirements will be marked *Incomplete* and returned to you without further comment. 



When it comes to **explanations**: 

- **Keep it simple and clear.** Do not assume that the reader is a genius, has lots of experience shared with you, or wants to fill in any gaps you leave. Use plain language and make your explanations as clear as possible. 
- **General statements are not explained by examples.** For example if you think a function is injective, it means that there are no collisions from the input to the output. Explaining this, requires that you explain why collisions **never** happen with this function; a single, specific example of a collision not happening isn't convincing. However, remember that if a function **is not** injective, or is not surjective, then this *can* be explained with a single example where the property fails, so you can give that example and explain why it works. 
- **Remember the audience**. The audience is **your classmates** --- people who are smart and have all the background knowledge that a regular person in the class would have, but none of the specialized knowledge that *you* have, and no experience with your particular problem. At regular intervals, stop and ask yourself if, honestly, your explanation would be clear and convincing for that audience. If not, keep working on it. 

And remember: **The main criteria used for evaluating your work on this and most other AEPs is the *quality of your explanations, not the correctness of your answers***. It's pretty easy to get right answers; but it takes real understanding to explain why they are right. 




## Submitting your work 

**AEP submissions must be typewritten and saved as either a PDF or MS Word file. No part of your submission may involve handwriting; work that is submitted that contains handwriting will be graded N and returned without feedback.** This includes electronic handwritten docments, for example using a stylus and a note-taking app. To type up your work, you can use MS Word or Google Docs (both of which have equation editors for mathematical notation) or any other computer-based math typesetting tool. Just make sure you save your work as a Word document or PDF (no `.odt`, `.rtf`, or other file extensions are allowed).

When you have your work typed up, double-check it for neatness, correctness, and clarity. Then simply submit your document on Blackboard, in the **AEP** area, in the **AEP 8** assignment. 

There are no special additional criteria for this AEP. Although there is code to analyze in this AEP, you do not need to *write* any code for it, so a Jupyter notebook isn't necessary. If you choose to use a Jupyter notebook anyway, that's OK, just remember to set permissions on your document correctly ("Everyone with the link can comment") and turn in the link, not a PDF. 


## Getting Help

You **may** ask me (Talbert) for help on this assignment in the form of **specific mathematical or technical questions, or clarifying questions about the instructions**. If I cannot answer a question because it would give too much away, I'll tell you so. However please note: **I will not "look over your work" before you submit it to give you feedback on the overall submission**. I have made the expectations clear, so just follow those directions and submit your best work, and you'll be allowed to revise it if needed. 

For AEPs, the syllabus policy on collaboration is: 

>On AEPs, you are allowed to engage in general discussions of strategy only with others, but no collaboration on the details of a problem are allowed..
 
**You can ask technology related questions to anyone at any time**. For example if you need help figuring out how to type up your work, there are no restrictions on that. 