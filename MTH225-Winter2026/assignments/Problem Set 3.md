# Problem Set 3

Submit solutions on or before **11:59pm Eastern time on Friday, March 6** in order to be eligible for engagement credits. 

## Instructions

Please remember the basic rules for Problem Sets: 

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 


---


## Problem 1: Combinatorial proof

We're currently looking at mathematical proofs using induction, but this is only one of a huge variety of methods of proof. Another important method of proof is called *combinatorial proof*. It is a used when you want to show that two sets have the same cardinality (i.e. the same "size"). The approach is to **create a bijective function from one of the sets to the other**. Since a bijection is a one-to-one correspondence between the elements of the domain and range, having a bijection lets us conclude that the domain and range have the same cardinality (size) even when those sets are infinite. 

This problem runs through an important example that will reappear soon. 

Let $B_4$ be the set of all binary strings of length $4$. For example `0111` and `1101` are both elements of $B_4$. Let $P(\\{1,2,3,4\\})$ be the power set of $\\{1,2,3,4\\}$ (the set of all subsets of $\\{1,2,3,4\\}$ as discussed in class earlier). 

1. Write out all the elements of $B_4$. There should 16 of these because they are just the decimal numbers 0 through 15 written in binary. 
2. Now look at the following function $f: B_4 \rightarrow P(\\{1,2,3,4\\})$. Given a binary string, create a subset of $\\{1,2,3,4\\}$ as follows: If the bit in position $n$ is 1, include the number $n$ in the subset. Otherwise do not include it. For example $f(0111) = \\{2,3,4\\}$ and $f(1101) = \\{1,2,4\\}$. Make a table of values for $f$ showing the outputs of all 16 possible inputs. Then use the table to explain why $f$ is a bijection. 
3. Based on question 3, how many subsets does $\\{1,2,3,4\\}$ have? 
4. Extend this idea to explain why the number of subsets of $\\{1,2,3,\dots, n\\}$ is $2^n$. (This is a fact we will prove in class with induction; here, you're proving it a different way.)

## Problem 2: Cardinalities of infinite sets

If $S$ is a set then its [cardinality](https://publish.obsidian.md/discretecs/Sets+and+Functions/Cardinality), $|S|$, refers to the "size" of the set. For finite sets this is just the number of elements in the set. But it's a mistake to say the same thing about infinite sets, because "the number of" elements in such a set is hard to pin down. That's what this problem will illustrate. 

1. Look at the sets $\mathbb{N}$ (natural numbers) and $\mathbb{Z}$ (integers). These are both infinite. Is $\mathbb{N}$ a subset of $\mathbb{Z}$? Or is it the other way around? Or is it neither? Also, are these sets equal? Explain everything. 
2. Consider the following function $f: \mathbb{N} \rightarrow \mathbb{Z}$ defined this way: 
   - If the input $n$ is an even natural number, then $f(n) = 2n$. 
   - If the input $n$ is an odd natural number, then $f(n) = -\frac{n+1}{2}$.

  For example $f(10) = 20$ and $f(21) = -11$. Make a table of values for this function from $n=0$ to $n=10$. (Watch your arithmetic when the input is odd.)
  
3. Based on the table values, is $f$ injective, surjective, bijective, or neither injective nor surjective? Explain. (You don't have to give a rigorous proof, just a convincing explanation.)
4. Based on the results of the second question, how does the cardinality of $\mathbb{N}$ compare to the cardinality of $\mathbb{Z}$? Be sure to explain your reasoning fully. Don't rely on intuition -- use the answer from question 3; also the ideas from Problem 1 above can be useful. 
5. Why is the answer to question 4 weird or counterintuitive in light of your answer to question 1?   

## Problem 3: Symmetric difference 

If $A$ and $B$ are sets then their [symmetric difference](https://publish.obsidian.md/discretecs/Sets+and+Functions/Symmetric+difference), written $A \Delta B$, is the set 

$$A \Delta B = (A-B) \cup (B-A)$$ 

1. Write a Python function `symm_diff` that takes in two sets $A$ and $B$ as input and produces their symmetric difference as output. See "Python Notes" below for tips. 
2. For any set $A$, what is the result of $A \Delta \emptyset$? Explain your reasoning fully and without diagrams or examples. 
3. For any set $A$, is it possible to find another set $B$ such that $A \Delta B = \emptyset$? If you believe this can be done for every set, give a rigorous and convincing explanation. If you believe this cannot be done for every set, give a specific, concrete example where it fails. 

**Python notes:** As mentioned in class, Python has native `set` objects and your function needs to use those (not lists, etc.). Working with sets is a little different than how you do it with lists. You might find some of these notes useful: 

- To initialize an empty set object in Python, use the `set()` constructor, like this: `empty_set = set()`. Do not just use empty curly braces `{}` because Python thinks this is an empty dictionary. (You could use `set({})` to create an empty set, but this is more work than just `set()`.) 
- To add an element `x` to an existing set `S`, use the `.add` method, like this: `S.add(x)`
- The operator `in` works for sets like it does for lists. For example `3 in {1,2,3}` returns `True` and `5 in {1,2,3}` returns `False`. 
- Set comprehensions are a thing in Python, just like list comprehensions and other kinds of comprehensions. For example `{x for x in A for x in B if x in A and x in B}` gives $A \cap B$.  