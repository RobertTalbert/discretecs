# Problem Set 2

Submit solutions on or before **11:59pm Eastern time on Wednesday, February 18** in order to be eligible for engagement credits. 

## Instructions

Please remember the basic rules for Problem Sets: 

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 


---


## Problem 1: Boolean refactoring

In software engineering, "clean code" often means simplifying complex if statements. Suppose a developer is writing a permissions check for a cloud storage app. They have written a very messy conditional:

```python
if (!( (!isAdmin && isOwner) || (!isAdmin && !isPaidSubscriber) ))
```

1. Let $p$ be `isAdmin`, $q$ be `isOwner`, and $r$ be `isPaidSubscriber`. Write the logic as a formal proposition, using those variables and correct symbols for logical connectives. 
2. Use logical equivalences to simplify this expression to its shortest possible form. Show every step and name the law used.
3. Looking at your simplified version, explain in plain English: Under what specific conditions does a user actually get access? Is it possible for a non-admin to get access?

## Problem 2: System monitoring 

Let the domain $S$ be the set of all servers in a data center, and $P$ be the set of all possible processes. Define the following predicates:

- $R(s, p)$: "Server $s$ is running process $p$."
- $O(s)$: "Server $s$ is overloaded."
- $H(p)$: "Process $p$ is high-priority."

Translate these three system requirements into formal predicate logic:

1. "Every server is running at least one process."
2. "There is a process that is running on every server."
3. "If a server is running any high-priority process, that server is overloaded."
4. Suppose we know that $\forall s \exists p (H(p) \wedge R(s, p))$ is true. Based on your answer to statement #3, can we conclude that every server in the data center is overloaded? Explain your logical derivation.Pro