# MTH 325: Problem Set 4

Submit solutions on or before **11:59pm Eastern time on Friday March 27** in order to be eligible for engagement credits. 

## Instructions

Please remember the basic rules for Problem Sets: 

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 


---


## Problem 1: More induction

Pick ONE (1) of the following and give a complete, clearly written, and correct proof using either weak or strong induction. 

1. For every integer greater than $6$, $3^n  < n!$
2. For all nonnegative integers $n$, $1 + 2 + 2^2 + 2^3 + \cdots + 2^n = 2^{n+1} - 1$. 
3. Recall that the Fibonacci numbers are the integers given by the recurrence relation $F_1 = 1, F_2 = 1$ and for $n > 2$ we have $F_n = F_{n-1} + F_{n-2}$. Then, for all integers $n \geq 2$, $F_{2n} = \left( F_{n+1}  \right)^2 - \left( F_{n-1}  \right)^2$. 


## Problem 2: Application of graph coloring 

A small college is scheduling final exams for seven courses: Calculus (CA), Statistics (ST), Physics (PH), Chemistry (CH), Biology (BI), Computer Science (CS), and Economics (EC). This is a small college, so there is only one section of each course available, and no alternate time slots. The registrar has identified the following pairs of courses that share at least one student: CA–ST, CA–PH, CA–CS, ST–EC, ST–BI, PH–CH, PH–CS, CH–BI, CS–EC, BI–EC. (For example, “CA-ST” means that there’s at least one student enrolled in both Calculus and Statistics and therefore cannot have their final exams for those classes scheduled at the same time.) 

1. Draw the *conflict graph* for this situation. This is a graph where each course is a node, and there is an edge between two nodes if the classes are in conflict with each other (in terms of their final exams) and therefore their exams cannot be scheduled into the same slot. Again, no handwritten work; you can use networkX, for example, to produce a nice-looking computer-generated graph. 
2. Run the greedy coloring algorithm (by hand) on the conflict graph, using alphabetical order for the nodes, to come up with a valid vertex coloring. Organize your work using a table like we did in [the class activity on coloring](https://docs.google.com/document/d/1RB0xC9i_7TyhyDMLLAtZ5o_w4AlYlyphYO1WD_z-1cQ/edit?usp=sharing). Then use the results to create a final exam schedule that has no conflicts. 
3. Is your coloring from part 2 the smallest possible coloring (uses the smallest possible number of colors)? If so, explain why. If not, find a minimal coloring. 



## Problem 3: Proofs about coloring

Choose ONE (1) of the following and give a completed proof. Your proof should be a complete, clear, logical explanation for why the statement is true; it may or may not conform exactly to one of the techniques we've studied (induction, contradiction, etc.). 

Recall that $\chi(G)$ is the [chromatic number](https://publish.obsidian.md/discretecs/Graphs/Chromatic+number) of the graph $G$. 

1. Prove that if $T$ is a tree, then $\chi(T) = 2$. 
2. Let $Q_n$ is the hypercube graph from [Problem Set 3](https://github.com/RobertTalbert/discretecs/blob/master/MTH325-Winter2026/assignments/MTH%20325%20Problem%20Set%203.md). Prove that $\chi(Q_n) = 2$ for all $n$. 
3. Let $G$ be any graph. Prove that if $G$ contains a cycle of length 3, then $\chi(G) \geq 3$. Also give a counterexample that shows that this statement is false if you replace "3" with a larger integer. 