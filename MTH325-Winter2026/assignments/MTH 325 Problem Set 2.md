# Problem Set 2

## Instructions

Recall the rules for problem sets:

- To submit your work on a Problem Set, please TYPE up your solutions and save them as a PDF, then upload the PDF to the designated area on Blackboard (in the Problem Sets folder). **Handwritten work is not accepted.**
- These Problem Sets are **not graded directly**. They are only given formative feedback that you can use to improve your work. You may resubmit a new draft of a Problem Set at any time, by making a new draft and uploading that to the same designated area on Blackboard where the first draft went. 
- **Application/Analysis Exam problems will be selected from among problems that appear on Problem Sets**. So it is to your advantage to submit Problem Sets and use the feedback to refine your solutions. 
- You will receive 8 engagement credits for turning in a **good-faith complete attempt at a Problem Set prior to its deadline**. This means: Every part of every problem must contain an attempt that represents an honest try at a full and complete solution. 

---


## Problem 1: Network redundancy

In a distributed computing network, every server (thought of as a node) must be connected to exactly 3 other servers to ensure redundant communication paths. When this happens, the resulting graph is called a **3-regular graph**.

1. Prove that it is impossible to build such a network if the total number of servers is 15. Do not draw any pictures for this problem! Prove it using facts we learned in class. 
2. If the network has 6 servers, draw the graph or provide the Python dictionary that represents a 3-regular structure.
3. Does the graph from part 2 contain a Hamiltonian cycle? Provide the sequence of vertices for the cycle or explain why one cannot exist.


## Problem 2: Memory vs. speed tradeoff

A social media startup is designing a feature to suggest "friends of friends": If Alice is friends with Bob and Bob is friends with Chuck, then the feature will suggest to Alice that she become friends with Chuck and vice versa.  The developers at the startup are debating how to store their graph of $n$ users and $m$ friendships.

1. Suppose a graph $G$ has 10,000 nodes but is very sparse (each user has only 20 friends on average). Calculate the number of entries required to represent this in an adjacency matrix versus a Python dictionary.2. Write the logic (or pseudocode) for a function `is_friend(user_a, user_b)` for both representations. This function would accept the names of two users and return `TRUE` if they are friends in the network and `FALSE` otherwise. 
3. If the network's graph is a complete graph ($K_n$), which representation is more efficient for checking if a specific edge exists? Explain using specific reasoning. 
4. To justify your answer to the previous question, prove that for any graph, the total number of elements stored across all adjacency lists in a dictionary representation of the graph is exactly $2|E|$. Use this to explain why the dictionary "bloats" when the graph becomes dense.
