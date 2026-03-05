# MTH 325 Application/Analysis Exam 1 -- Solution Guide and Notes 

## Part A

1. B
2. E
3. C
4. B
5. A
6. A
7. B
8. B
9. C
10. E

## Part B

### Option 1

Results vary according to which proof technique is used. Here is a proof using the contrapositive: 

Assume that $n$ is odd. We will show that $n^3$ is odd. Since $n$ is odd, there exists an integer $k$ such that $n = 2k+1$. In that case, $n^3 = (2k+1)^3 = 8k^3 + 12k^2 + 6k + 1$. Factoring $2$ from the first three terms gives $2(4k^3 + 6k^2 + 3k) + 1$. Since $k$ is an integer, $q = 4k^3 + 6k^2 + 3k$ is also an integer. Therefore there $n^3 = 2q+1$ where $q$ is an integer, so $n^3$ is odd. 

### Option 2

Results vary according to which proof technique is used. Here is a direct proof: 

Assume that $a$ and $b$ are odd. We want to show that $a+b$ is even. Since $a$ and $b$ are odd, there exist integers $m$ and $n$ such that $a = 2m+1$ and $b = 2n+1$. Then $a+b = 2m + 2n + 2 = 2(m+n+1)$. Since $m$ and $n$ are integers, $m+n+1$ is also an integer and therefore $a+b$ (being $2$ times an integer) is even. 

### Grading notes for Part B

- **A frequent mistake in Option 2**: If you prove this with a direct proof, you start by assuming $a$ and $b$ are odd. The frequent mistake was using the same variable to represent this, for example: "Since $a$ is odd then $a = 2k+1$ and since $b$ is odd then $b = 2k+1$." Using the same variable, $k$, for both $a$ and $b$ now means that $a$ and $b$ are equal **to each other** since they are both equal to $2k+1$. But that's an unwarranted assumption because we can't assume that $a$ and $b$ are equal. We are only assuming that they are both odd numbers. That's a significant enough mistake to derail the logic of the rest of the proof. So in this situation, as shown in the solution above, you have to use two different variables to represent the odd-ness of $a$ and $b$.  
- **Just say no to induction:** Some submissions for option one saw the letter $n$ as the variable and decided to try induction. Induction is a poor fit for either of these two options because there is no recursion involved in either of them. And these two propositions are also stated to be true for all integers, not just all positive integers. Induction does not handle negative integers particularly well. 

---

## Part C

### Option 1

This proof uses weak induction. 

The base case is when $n = 0$. In this case the left side of the equation is just the single term $F_0$ (not an actual sum of multiple numbers), which is equal to $1$ by definition. On the right side we have $F_2 - 1$. Now $F_2 = F_1 + F_0 = 1 + 1 = 2$, so $F_2 - 1 =1$. The left and right sides are now equal, so the base case has been verified. 

Now assume that $F_0 + F_1 + F_2 + \cdots + F_k = F_{k+2} -1$ for some $k$. We want to show that $F_0 + F_1 + F_2 + \cdots + F_{k+1} = F_{k+3} -1$. 

Looking at the left side, we have $F_0 + F_1 + F_2 + \cdots + F_{k+1}$. Grouping the all but the last term gives $(F_0 + F_1 + F_2 + \cdots + F_k) + F_{k+1}$, and by the inductive hypothesis, we can substitute the sum in parentheses to get $(F_{k+2} - 1) + F_{k+1}$. Rearranging terms gives $F_{k+2} + F_{k+1} - 1$ and then by the Fibonacci recurrence relation we have $F_{k+3} - 1$. This is what we wanted to prove. 

### Option 2

The proposition is equivalent to saying: For all $n \geq 1$, the Fibonacci number $F_{3n-1}$ is even. This proof uses weak induction. 

The base case in this form is $n=1$. This gives the number $F_2$ which is equal to $2$, which is even. 

Now assume that $F_{3k-1}$ is even for some $k$. We want to prove that $F_{3(k+1)-1}$ is even. In the subscript, $3(k+1) - 1 = 3k + 2$. So we want to show that $F_{3k+2}$ is even. Using the Fibonacci identity gives us: $F_{3k+2} = F_{3k+1} + F_{3k}$. We also know from the Fibonacci identity that $F_{3k+1} = F_{3k} + F_{3k-1}$. 

Substituting this last expression into the first term of the first expression gives: 

$$F_{3k+2} = F_{3k+1} + F_{3k} = (F_{3k} + F_{3k-1}) +F_{3k}$$

Adding like terms gives  $F_{3k+2} = 2 F_{3k} + F_{3k-1}$

Now, $2 F_{3k}$ is even because it is an integer multiple of $2$; and $F_{3k-1}$ is even by the inductive hypothesis. Therefore $F_{3k+2}$ is the sum of two even numbers, which is even. 

### Grading notes for Part C

- **"The pattern continues" is not a proof:** In option 2, a number of submissions use the approach of calculating a few values of the Fibonacci numbers and attempting a general argument that there's an alternating pattern of odd, odd, even in these. There is an approach to a proof of this option that does this, but these submissions gave a few examples and said, "the pattern continues". That statement alone is asking the reader to take it on faith that what you are observing in the Fibonacci numbers does, in fact, continue. What the problem is asking you to do, on the other hand, is give a convincing general mathematical argument that this is the case. Again, this can be done without induction on this particular proposition, but it didn't happen in any of the submissions that I saw. 
- **Indexing matters:** Also on option two, there were a number of submissions that struggled with interpreting what every third Fibonacci number actually means. As you see in the solution above, it helps to tramslate this into a proposition about the indexes on the Fibonacci numbers. In my solution for example, "every third Fibonacci number" means "Fibonacci numbers with indices $3n-1$ where $n$ is a positive integer", so $F_2, F_5$, and so on. Variations from incorrect approaches included things like $F_{n+3}$ which does not skip Fibonacci numbers three at a time. 

---

## Part D 

### Option 1

The adjacency matrix for the graph would have one row and one column per node in the graph. That means the matrix is $10000 \times 10000$ so there are $10000 \times 10000 = 100000000$ (one hundred million) entries. 

If it were a dictionary, then there would be one set of key-value pairs per node --- so, $10000$ of those, and according to the problem data each key has 20 values on average in its adjacency list. The math we do next depends on how you interpret an "entry". If we interpret that as meaning an entry in the adjacency list, then there are going to be $20 \times 10000 = 200000$ (two hundred thousand) of those. If you count the keys too, then it's $200000 + 10000 = 210000$. (Either one is OK for a response here, all that matters is the logic being used.) 

For the `is_friend` function, here is the basic logic behind how it would work in each representation: 

- For the adjacency matrix, go to the row for `user_a` and the column for `user_b` and just return the value that lives at that entry. This will be either a `0` or `1` depending on whether `user_a` is connected to `user_b` in the network, so you can use the raw matrix entry as the function output. (The exact Python syntax used to access the entry of a matrix in a particular row and column is somewhat dependent on the package used to handle matrices, so the above is good enough.)
- For the dictionary, just ask Python to tell you if `user_a` is in the adjacency list for `user_b` (or vice versa). A one-liner like `return user_b in d[user_a]`, where `d` is the dictionary for the graph, would do it. 

### Option 2

Suppose $G$ is the graph and `dict_g` is its dictionary. To calculate the number of elements stored across all adjacency lists, do something like this: 

- Initialize a `count` variable to `0`
- For each node `v` in the graph, find `len(dict_g[v])` and add it to `count`. This is just looping over the keys in the dictionary, finding the length of the list attached to `v`, and adding it to the accumulator `count`. 
- Then return `count`, which will give you the number of elements total in all the lists. 

But notice that the **length of the adjacency list for node `v` is just the degree of $v$**. So in the above, what we're really doing is adding up the degrees of each node. Therefore `count` is just $\sum_{v \in V} \deg(v)$, the degree sum for the graph. The Handshake Lemma says that this equals $2|E|$, twice the number of edges. 

If the graph is complete, it has a lot of edges, in fact it has the maximum possible number of edges, and the adjacency lists in the dictionary are relatively long. Searching for a specific edge in a graph means determining if node `a` is adjacent to node `b`. In a dictionary, it means going to node `a` and searching through the list attached to that key to see if `b` belongs to it. In a complete graph $K_n$ that means the adjacency list is $n$ units long, so it's a linear search through a list of length $n$. (In algorithms/CIS 263 language we would say that the process is $O(n)$.) 

But in an adjacency matrix, it doesn't matter how many other nodes `a` is connected to --- we just go to the row for `a` and the column for `b` and look at that one entry. There are significantly more entries in the matrix (see Option 1) but we can skip most of them because we can do a direct lookup for two particular nodes. This does not depend at all on the number of nodes. (In algorithms/CIS 263 language we would say that the process is $O(1)$ or constant-time.) 

So the dictionary approach works very well for "sparse" graphs where the adjacency lists are short because the search space is much smaller. **But for full graphs, the matrix representation works better.**

### Grading notes for Part D

- **Follow directions:** A number of solutions on both these options simply omitted parts of the problem. For example, finding the number of entries in the dictionary for the graph, but not doing the number of entries for the matrix, or giving the pseudocode for the two functions without any counting of the number of entries in either data structure. 
- **Doing both parts:** Some submissions for option two had correct logic and a basically correct proof for the first part of option two, and an explanation for the second part of option two, but those two parts of option two did not relate to each other. What you're asked to do in option two is, as it says, "use the result to explain which representation would be more efficient". So you have to prove the result and then use the result. Giving an explanation that seems to address the efficiency issue, but does not use the mini-theorem you proved in the first part is not a complete or correct solution to this option. 