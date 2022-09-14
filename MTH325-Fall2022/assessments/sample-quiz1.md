# SAMPLE Content Skill Standard Quiz 

**NOTE:** This is a SAMPLE Content Skill Standard Quiz very similar to what you will see in your first quiz. On the actual quiz, only the specifics of the questions will change; everything else will remain as you see it here. Please take note: 

- Each item on the quiz pertains to exactly one Content Skill Standard, and the standard itself is stated before the problem. 
- Each item has a particular task or set of tasks that you will complete to demonstrate your skill. 
- Each item is followed by **Success criteria** that explain what a "successful" demonstration of skill requires. 
- The **Instructions** below give more information about how to take quizzes. Note especially, *you do not have to attempt a problem if you aren't ready to do so*. If you need more practice, go ahead and take it; future quizzes will contain new versions of all previously-assessed problems, so you can try again later. 
- On this particular SAMPLE Quiz, solutions have been included at the end of the page. 

---

:::info
This quiz contains *new questions* for **Content Skill Standards P.1 and P.2**.

**Instructions**

* Work only the problems that you **need to work** and **feel ready to work**. 
* Do your work on separate pages with **each Content Skill Standard on its own separate page**. *Please do not put work for multiple Standards on the same page.* 
* Make sure to consult the [Specifications for Student Work in MTH 325](https://hackmd.io/lD6oyEN5RdiUi_wdg-rkZg) document before starting on your work, so you're clear on what is expected and what constitutes a "successful" attempt. 
* Also, make sure to carefully read the **Success Criteria** below each problem to know exactly what is expected from that problem. 
* When you are done: **Scan** each Learning Target to a clear, legible, black-and-white PDF and **upload the PDF** to the designated folder on Blackboard. Please  *do not just take a picture with your camera* --- use a scanning app to create a PDF, and upload the PDF. You can also type up your work and save to a PDF if you want; or use a notes app on a tablet to handwrite your work and save that to a PDF. 

:::


## Content Skill Standard P.1 

:::warning
★ P.1: Given a statement to prove with mathematical induction, I can identify the predicate, state and prove the base case, state the inductive hypothesis, and outline the rest of the proof. 
:::

Consider the statement: 

>For all positive integers $n$, $1 + 2 + 4 + 8 + \cdots + 2^n = 2^{n+1} - 1$. 

1. State the predicate involved in this statement. 
2. State and prove the base case for a proof by induction of this statement. 
3. State the inductive hypothesis for a proof by induction of this statement. 
4. Outline the remainder of a proof by induction for this statement by clearly stating what you would prove, and giving at least one plausible idea for proving it. 

**Success criteria:** The predicate must be clearly stated; the base case must be correctly stated and proven; and the inductive hypothesis must be correctly stated in the context of the problem. The outline for the remainder of the proof must clearly state what you are going to prove, and the "plausible idea" must be some specific step you might take that makes sense in the context of the problem. 



## Content Skill Standard P.2

:::warning
★ P.2: Given a conditional statement, I can state the assumptions and conclusions for a direct proof, proof by contrapositive, and proof by contradiction. 
:::

Consider the statement: 

>For every integer $n$, if $n$ is a multiple of $4$ then $n^2 - 1$ is a multiple of $4$. 

1. Clearly state what you would assume and what you would prove, if proving this statement with a *direct proof*. 
2. Clearly state what you would assume and what you would prove, if proving this statement with a *proof by contrapositive*.
3. Clearly state *all* the assumptions you would make, if proving this statement *by contradiction*. 

**Success criteria:** All parts of each of the three items here are correctly and clearly stated. 

---

### "Successful" solutions for these sample problems

#### P.1 solution

1. The predicate is $P(n): 1 + 2 + 4 + 8 + \cdots + 2^n = 2^{n+1} - 1$. 
2. We would need to show that $P(1)$ is true, that is, $1 + 2^1 = 2^{1+1} -1$. To prove this, note that the left side is $1 + 2$ or $3$; and note that the right side is $2^2 - 1$ which is also $3$. These two are equal, so the predicate is true when $n=1$. 
3. Assume that for some positive integer $k$, $1 + 2 + 4 + 8 + \cdots + 2^k = 2^{k+1} - 1$. 
4. We want to prove that $1 + 2 + 4 + 8 + \cdots + 2^{k+1} = 2^{k+1+1} - 1$. To do this, we might look at the left side and group together the first $k$ terms to get $(1 + 2 + 4 + \cdots + 2^k) + 2^{k+1}$. Then we could replace the stuff in the group with $2^{k+1} - 1$ since we assumed this in the inductive hypothesis. That makes the left side equal to $2^{k+1} -1 + 2^{k+1}$. Then we would want to do some algebra to simplify this and make it equal to $2^{k+2} - 1$ somehow. 


#### P.2 solution

1. Assume that $n$ is a multiple of $4$. Then prove that $n^2 - 1$ is a multiple of $4$. 
2. Assume that $n^2 - 1$ is *not* a multiple of $4$. Then prove that $n$ is *not* a multiple of $4$. 
3. Assume that $n$ is a multiple of $4$ but $n^2 - 1$ is not a multiple of $4$. 