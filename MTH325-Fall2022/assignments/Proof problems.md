# Proof Problems 

## Instructions for all Proof Problems 

First of all please note: **You do not have to do all of the problems below.** The Proofs badge instructions in the syllabus only requires that you complete **three different Proof problems** --- one that uses mathematical induction in the proof, one that does *not* use induction, and a third one that you can prove any way you want. Proof problems will be added continuously to this list through the semester, and there may be dozens of problems from which to choose by the end. Please note that problems can be solved in many different ways, and it's possible that some Proof problems could be done both with induction and without it. 

Your job is to **find a problem that looks interesting to you and then solve it**. "Solve" here means **write a complete, correct, and polished proof** for the statement that's given in the problem. [Please see the Specifications for Students Work in MTH 325 document](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) for precise details of what this involves. Among the criteria for acceptable work are these important points: 

- Your work must constitute a **good-faith effort at a completed proof**. You may not write up part of a proof and leave other parts of it incomplete or blank. 
- Your work must be **free from serious errors** in computation, logic, factual knowledge, and semantics. (See the [Specifications document](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) for descriptions of those.)
- Your work must **look professional** and **explain your reasoning clearly**. Proofs that are just computations (a "wall of math") will need to be revised. 

Remember that **proofs are highly personalized, and the same statement can be proven many different ways**. A proof is just a clear, correct, and convincing explanation why a statement is always true. It does not have to conform to any particular method like induction, contradiction, etc. If you feel you can give an argument for why a statement below is true that is clear, correct, and convincing and it doesn't look like one of the basic arguments we explored in class, give it a try. 


Here are specific instructions on how to submit your work: 

- All Proof problems must be **typed** using a word processor or other computer program that allows for entry of mathematical notation. Microsoft Word, Google Docs, and Open Office Writer all have built-in equation editors you can use to insert mathematical notation. You can also use LaTeX if you know how. But, **no handwritten work is accepted** -- any submission that is handwritten will be marked "Revise" and returned without any feedback on the work itself. 
- Your work must be **saved as a PDF file**. Microsoft Word documents are also OK, but *no other file format is accepted* because I can't leave feedback on the submission if it's not PDF or Word. 
- Put **one problem per PDF**. If you have proofs for 2-3 different problems, submit them separately in separate files. 
- When you are ready to submit your work, save it in a PDF (one problem per PDF) and **upload the PDF to Blackboard** in the *Proof Problems Submission* assignment folder. **All work on Proof Problems goes in this one folder** which means this one Blackboard item might have your past work on several different proofs. I leave it up to you to know which ones you have submitted. 


Once your work is submitted, I will be notified, and then I will evaluate it using our "Critical Analysis" process. If your work meets the specifications laid out in the [Specifications](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document, it will be marked *Successful* on Blackboard, and you are done with that problem. If not, it will be marked *Revise* and you will be given feedback on both the good and the not-as-good on your work, and then you can revise and resubmit again later. Note that feedback will be given regardless of the mark. 


**Deadlines:** Each Proof Problem has an **initial deadline** listed. If you intend to submit any work at all on a problem, the first attempt must be submitted before this deadline. Once you have made that initial lsubmission, there is no further deadline on revisions other than the final deadline of **Sunday December 11**. Only attempts that represent good-faith efforts at complete and correct proofs are counted as "initial submissions. For example, if you submit a partial proof just before the deadline, a "revision" of that proof that is submitted after the deadline, in which you complete the partial work, will not be accepted. 



---



### Problem 1

*Initial deadline: Sunday, October 2 11:59pm ET* 

Recall from MTH 225 that the **binomial coefficient** $\binom{n}{k}$ is the number of ways to select $k$ elements from an $n$-element set (irrespective of ordering). It can also be interpreted as the number of $k$-element subsets of an $n$-element set; or as the number of bitstrings of length $n$ that have exactly $k$ `1` bits. 

A fundamental identity for the binomial coefficient is this, which you also learned in MTH 225: 
$$\binom{n}{k} = \binom{n-1}{k} + \binom{n-1}{k-1}$$
For an explanation why this recurrence relation holds, [click here](https://vimeo.com/714228899).

Prove that, for all positive integers $n$, the following equality holds for the binomial coefficient: 

$$\binom{n}{0}2^0 + \binom{n}{1}2^1 + \binom{n}{2}2^2 + \cdots + \binom{n}{n}2^n = 3^n$$

*Pro tip*: There is a closed formula for the binomial coefficient, namely $\binom{n}{k} = \frac{n!}{(n-k)! k!}$. You are highly advised *not* to use that formula in this problem -- the algebra that results is truly awful. 


### Problem 2

*Initial deadline: Sunday, October 2 11:59pm ET* 


The **logarithm base 2** of a number $x$, written $\log_2(x)$, is the power to which you would raise $2$ in order to get $x$. That is, if $\log_2(x) = a$ then $2^a = x$. For example, $\log_2(8) = 3$, $\log_2(1024) = 10$, and (using a calculator) $\log_2(100)$ is around $6.644$. 

Consider the following recursive function, given here as Python code: 

```python
def r(n):
	if n == 1: 
		return 0
	else:
		L = r(n//2)
	return L+1
```
Although you might not know Python, you can still read this like pseudocode. The first line defines the function `r(n)`. If the input is `1` then the output is simply declared to be `0`. Otherwise, the function calls itself on an input that is half the size of the original. Here, the `//` sign means **integer division**, that is, regular division but drop the remainder. For example `19//2` equals `9`.

With this information, prove that for all integers $n \geq 1$, the value that is output by this algorithm for `r(n)` is $\lfloor \log_2(n) \rfloor$, that is, the logarithm base 2 of $n$ rounded down to the next lowest integer. 

### Problem 3

*Initial deadline: Sunday, October 2 11:59pm ET* 


See Problem 2 for a definition of the **logarithm base 2** of a number. Prove that, for all positive integers $n$, the number of bits needed to represent $n$ in binary (base 2) is $1 + \lfloor \log_2(n) \rfloor$, that is, the logarithm base 2 of $n$ rounded down to the next lowest integer, plus 1. 

*Example:* According to this proposition, the number of bits needed to represent the number 99 in binary is 
$$1 + \lfloor \log_2(99) \rfloor = 1 + \lfloor 6.6294 \rfloor = 1+6 = 7 $$
And indeed, if we convert 99 to binary we get `1100011` which contains 7 bits. 

### Problem 4 

*Initial deadline: Sunday, October 2 11:59pm ET* 


>Definition: If $a$ and $b$ are integers then we say that **$a$ divides $b$** if there is an integer $k$ such that $b = ak$. For example, $3$ divides $21$ because there is an integer ($k=7$) such that $21 = 3k$. If $a$ divides $b$ then we write $a | b$. 

Here are some statements about divisibility. Not all of them are true! For the ones that are *not* true, give a specific counterexample and explain why the counterexample works. For those that *are* true, give a completed proof. 

1. If $a|b$ and $b|c$ then $a|c$
2. If $a|c$ and $b|c$ then $(ab)|c$ 
3. If $a|c$ and $b|c$ then $(a+b)|c$ 
4. If $(ab) | c$ then either $a|c$ or $b | c$ 
5. If $(a+b)| c$ then either $a|c$ or $b|c$ 
6. If $a|b$ and $a|c$ then $a|(bc)$ 
7. If $a|b$ and $a|c$ then $a | (b+c)$ 

