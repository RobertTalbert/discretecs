---
tags: mth325-f22
---

# MTH 325 Fall 2022 Proof Problems 

:::info
Selected solutions for this Proof Problems can be found here: https://hackmd.io/@rtalbert235/H1HOeX1Bi 
:::


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

## Proof Problems 


### Problem 1

*Initial deadline: Sunday, October 2 11:59pm ET* 

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

Recall from MTH 225 that the **binomial coefficient** $\binom{n}{k}$ is the number of ways to select $k$ elements from an $n$-element set (irrespective of ordering). It can also be interpreted as the number of $k$-element subsets of an $n$-element set; or as the number of bitstrings of length $n$ that have exactly $k$ `1` bits. 

A fundamental identity for the binomial coefficient is this, which you also learned in MTH 225: 
$$\binom{n}{k} = \binom{n-1}{k} + \binom{n-1}{k-1}$$
For an explanation why this recurrence relation holds, [click here](https://vimeo.com/714228899).

Prove that, for all positive integers $n$, the following equality holds for the binomial coefficient: 

$$\binom{n}{0}2^0 + \binom{n}{1}2^1 + \binom{n}{2}2^2 + \cdots + \binom{n}{n}2^n = 3^n$$

*Pro tip*: There is a closed formula for the binomial coefficient, namely $\binom{n}{k} = \frac{n!}{(n-k)! k!}$. You are highly advised *not* to use that formula in this problem -- the algebra that results is truly awful. 


### Problem 2

*Initial deadline: Sunday, October 2 11:59pm ET* 

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

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

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

See Problem 2 for a definition of the **logarithm base 2** of a number. Prove that, for all positive integers $n$, the number of bits needed to represent $n$ in binary (base 2) is $1 + \lfloor \log_2(n) \rfloor$, that is, the logarithm base 2 of $n$ rounded down to the next lowest integer, plus 1. 

*Example:* According to this proposition, the number of bits needed to represent the number 99 in binary is 
$$1 + \lfloor \log_2(99) \rfloor = 1 + \lfloor 6.6294 \rfloor = 1+6 = 7 $$
And indeed, if we convert 99 to binary we get `1100011` which contains 7 bits. 


### Problem 4 

*Initial deadline: Sunday, October 2 11:59pm ET* 

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

>Definition: If $a$ and $b$ are integers then we say that **$a$ divides $b$** if there is an integer $k$ such that $b = ak$. For example, $3$ divides $21$ because there is an integer ($k=7$) such that $21 = 3k$. If $a$ divides $b$ then we write $a | b$. 

Here are some statements about divisibility. Not all of them are true! For the ones that are *not* true, give a specific counterexample and explain why the counterexample works. For those that *are* true, give a completed proof. 

1. If $a|b$ and $b|c$ then $a|c$
2. If $a|c$ and $b|c$ then $(ab)|c$ 
3. If $a|c$ and $b|c$ then $(a+b)|c$ 
4. If $(ab) | c$ then either $a|c$ or $b | c$ 
5. If $(a+b)| c$ then either $a|c$ or $b|c$ 
6. If $a|b$ and $a|c$ then $a|(bc)$ 
7. If $a|b$ and $a|c$ then $a | (b+c)$ 


### Problem 5

*Initial deadline: Sunday, October 2 11:59pm ET* 

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

Prove that the number of edges in the complete bipartite graph $K_{n,m}$ is $nm$. 

### Problem 6

*Initial deadline: Sunday, October 16 11:59pm ET* 

:::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
:::

The *hypercube graph* $Q_n$ is the graph formed as follows: 

* The vertices of $Q_n$ are the integers $0,1,2,\dots, 2^n - 1$ written in binary form as an $n$-bit string. 
* Two vertices of $Q_n$ are connected by an edge if their binary strings differ in exactly one place. 

For example, the hypercube graph $Q_3$ has eight vertices: `000`, `001`, `010`, `011`, `100`, `101`, `110`, and `111` (the numbers 0 through 7, in binary as 3-bit strings). The vertices `000` and `001` are connected by an edge, as are `000` and `010`; but `001` and `010` are not connected by an edge. The graph itself looks like this: 

![](https://i.imgur.com/wK4adQh.png)

This was generated by the following Python code: 
```python=
import networkx as nx
G = nx.hypercube_graph(3)
nx.draw(G, with_labels = True, node_color = "lime")
```

How many *edges* are in $Q_n$, for any positive integer $n$? Make and prove a conjecture about it. (You will only turn in the conjecture and its proof; you don't need to submit any investigation work you do in coming up with the conjecture.) 

:::

### Problem 7

*Initial deadline: Sunday, October 16 11:59pm ET* 

<!-- :::warning
**The initial deadline on this problem has now passed.** If you turned in a first draft prior to that deadline, you are free to continue revisions if needed. If you *did not* turn in a first draft before the deadline, submissions for this one are now closed.
::: -->

Prove that for all real numbers $a$ and $b$, if $a > 0$ and $b > 0$, then $\dfrac{2}{a} + \dfrac{2}{b} \neq \dfrac{4}{a+b}$. 

(Note: We looked at a *flawed* proof of this proposition in the Daily Prep for 9/19.) 

### Problem 8

*Initial deadline: Sunday, October 16 11:59pm ET* 



This one has two parts: 

1. Prove or disprove: If $G$ and $H$ are isomorphic graphs, then $G$ and $H$ have the same degree sequence. 
2. Prove or disprove: If $G$ and $H$ have the same degree sequence, then they are isomorphic graphs. 

If you believe a statement is false, disprove it by giving a *specific* counterexample and an explanation for why your counterexample disproves the statement. (Counterexamples here would be specific examples of graphs, not general conceptual explanations.) If you believe a statement is true, give a complete, clear, and correct proof. 

### Problem 9 

*Initial deadline: Sunday, October 30 11:59pm ET* 

This one has two parts (and the second one is an extension of the first): 

1. Prove that having a cycle of length 3 is an isomorphism invariant. That is, if $G$ and $H$ are isomorphic graphs and $G$ has a cycle of length 3, then $H$ has a cycle of length 3. 
2. Let $n$ be an integer with $n > 2$. Prove that having a cycle of length $n$ is an isomorphism invariant. That is, if $G$ and $H$ are isomorphic graphs and $G$ has a cycle of length $n$, then $H$ has a cycle of length 3. 

:::info
**Terminology note:** Recall that a *cycle* is a path that starts and ends at the same vertex but otherwise contains no repeated vertices. We represent cycles as sequences of vertices. A *cycle of length $n$* is a cycle that has $n$ distinct vertices in its sequence. (We count the start/end vertex only once.) For example, in the graph below, the sequence $C,G,L,C$ is a cycle of length 3; and $G,H,I,K,L,G$ is a cycle of length 5. (So a cycle of length $n$ has $n$ edges and $n+1$ vertices, the first and last of which are the same.)

![](https://i.imgur.com/QZJgzMX.png)
:::


### Problem 10

*Initial deadline: Sunday, October 30 11:59pm ET* 


Prove that if $G$ and $H$ are isomorphic graphs and $G$ is bipartite, then $H$ is bipartite. (That is, the property of "being bipartite" is an isomorphism invariant.)

Note: We are not assuming that either graph is the *complete* bipartite graph $K_{m,n}$. 

### Problem 11 

*Initial deadline: Sunday, October 30 11:59pm ET* 


Prove that if $G$ and $H$ are isomorphic and $G$ is connected, then $H$ is connected. (That is, the property of "being connected" is an isomorphism invariant.)

:::info
**Terminology note:** The concept of connectedness appears briefly in the textbook in Section 4.1. Here is a more complete definition you can use:

*Definition:* A graph $G$ is *connected* if, given any two vertices $v$ and $w$ in $G$, there exists a path starting at $v$ and ending at $w$.  
:::

### Problem 12

*Initial deadline: Sunday, October 30 11:59pm ET* 


The **hypercube graph** is a special graph defined in [Problem 6](https://hackmd.io/QTmHZqZgTiSbSzKO2Vwbfg?both#Problem-6). What is the chromatic number of the hypercube graph? Make a conjecture and prove it. 

### Problem 13

*Initial deadline: Sunday, October 30 11:59pm ET* 


(*A throwback problem not about graphs*) Prove that 
$$2^{n+2} + 3^{2n+1}$$ 
is divisible by $7$ for all positive integers $n$. 

*Note:* An integer $k$ is "divisible by $7$" if there exists an integer $q$ such that $k = 7q$. For example $35$ is divisible by $7$ by taking $q = 5$. 

###  Problem 14

*Initial deadline: Sunday, October 30 11:59pm ET*

The **hypercube graph** is a special graph defined in [Problem 6](https://hackmd.io/QTmHZqZgTiSbSzKO2Vwbfg?both#Problem-6). The second proof of Problem 6, shown above, looks at the subgraph of $Q_k$ whose vertices are the bitstrings whose leftmost bit is `0` and whose edges are all the pre-existing edges between those vertices. Call this subgraph $H$. It is claimed that the function from $H$ to $Q_{k-1}$ that takes a node in $H$ and simply removes the leftmost bit, is a graph isomorphism. **Prove that this is the case.**  You'll need to show that: (1) the function is injective, (2) the function is surjective, (3) if $(a,b)$ is an edge in $H$ then $(f(a),f(b))$ is an edge in $Q_{k-1}$, and (4) if $(c,d)$ is an edge in $Q_{k-1}$, then $(a,b)$ is an edge in $H$ where $a$ and $b$ are the unique nodes such that $f(a) = c$ and $f(b) = d$. 

This is one where you will greatly benefit from playing with examples first! 

###  Problem 15

*Initial deadline: Sunday, October 30 11:59pm ET*

This one has two parts: 

1. Prove that if a graph $G$ is bipartite, then $G$ does not have a cycle of length 3. 
2. Prove or disprove the converse of part 1: If a graph does not have a cycle of length 3, then the graph is bipartite. 

*Reminder*: "Length 3" means there are three edges. 

###  Problem 16

*Initial deadline: Sunday, October 30 11:59pm ET*

Prove this mini-theorem that made an appearance in the solution for [Problem 2](https://hackmd.io/QTmHZqZgTiSbSzKO2Vwbfg?view#Problem-2): 

For all real numbers $x$, $\lfloor x - 1 \rfloor = \lfloor x \rfloor - 1$. (Here, $\lfloor x \rfloor$ is the "floor function".)

### Problem 17

*Initial deadline: Sunday, November 20 11:59pm ET*


:::info
This problem is specifically intended to be proven by mathematical induction. 
:::

Prove that for all integers $n > 1$, 
$$1 + \frac{1}{4} + \frac{1}{9} + \cdots + \frac{1}{n^2} < 2 - \frac{1}{n}$$

### Problem 18

*Initial deadline: Sunday, November 20 11:59pm ET*


:::info
This problem is specifically intended to be proven by mathematical induction. 
:::

Prove that for all positive integers $n$, 
$$1^2 - 2^2 + 3^2 - \cdots + (-1)^{n-1}n^2 = (-1)^{n-1} \frac{n(n+1)}{2}$$


### Problem 19

*Initial deadline: Sunday, November 27 11:59pm ET*

Let $n$ be any integer greater than or equal to 2. We say that two integers $a$ and $b$ are **congruent modulo $n$** if their difference, $a-b$ is a multiple of $n$. That is, $a$ is congruent to $b$ modulo $n$ if there exists an integer $q$ such that $a-b = nq$. If $a$ and $b$ are congruent modulo $n$, we write this as $a \equiv b \pmod n$. 

Example: $57 \equiv 1 \pmod 4$ because $57-1 = 56$ and this is a multiple of $4$. Specifically, $57-1 = 4(14)$. (The "$q$" in the definition is $14$.) 

In this problem, let $n \geq 2$ and recall that  $\mathbb{Z}$ is the entire set of integers (including zero and negative integers). Place a relation on $\mathbb{Z}$ by saying $a \sim b$ if $a \equiv b \pmod n$. **Prove that this relation is an equivalence relation.** (Remember you will need to prove three things.)

### :new: Problem 20

Let $S$ be any set with an equivalence relation $\sim$ and let $x,y \in S$. Prove that either $[x] = [y]$ or $[x] \cap [y] = \emptyset$. 

### :new: Problem 21

Let $P$ be a partially ordered set with the partial ordering denoted by $\leq$. (As always this does not literally mean "less than or equal to".) 

1. Prove that if $P$ is finite, then it must have at least one minimal element. 
2. Give a concrete example that shows that if $P$ is *infinite*, it doesn't necessarily have any minimal elements. 

**Note:** If you are also working [Application Problem 5](https://hackmd.io/I5JNc8uxQjiLUocxeLqHAQ?view#-Problem-5-A-sorting-algorithm-for-posets) (topological sorting of posets), you can use your work here for Part 3 of that problem. 

### :new: Problem 22

A vertex of a tree is called an **internal vertex** if it is not a leaf. And a rooted tree is called a **full binary tree** if every internal vertex has exactly two children. Here is an example: 

![](https://i.imgur.com/hTPRNF6.png)

Prove that every full binary tree with $n \geq 3$ vertices has $\dfrac{n-1}{2}$ internal vertices and $\dfrac{n+1}{2}$ leaves. 

(For example, the full binary tree above has $n=7$ vertices in all. The proposition here would predict it would have $\frac{7-1}{2} = 3$ internal vertices and $\frac{7+1}{2} = 4$ leaves. Visually you can check that this is the case.)


### :new: Problem 23

In a rooted tree, the **level** of a vertex is the length of the (unique) path from the root to that vertex. The **height** of the tree is the maximum of the levels of its vertices. For example: 
![](https://i.imgur.com/XqeimdD.png)

In this tree, 11 is the root. Vertex 13 has a level of 2; vertex 27 has a level of 4. And the height of the tree is 7. 

A tree is said to be **binary** if every internal vertex has 2 or fewer children. (Refer to Problem 22 for the definition of "internal vertex".)

Prove that if $T$ is a binary tree of height $h$, then it has at most $2^h$ leaves.  