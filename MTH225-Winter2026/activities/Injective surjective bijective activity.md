# MTH 225: Injective, surjective, and bijective functions

## Part 1: Return to Python

Using the 13 small Python functions from the activity in the previous class, classify each one as injective, surjective, or bijective or none of these. If a property fails, give an example of inputs and outputs that make the property fail. Organize your results in the table below by placing a check mark in the box if the property holds, and an "X" if it doesn't. 

| Function | Injective? | Surjective? | Bijective? | 
| :-----: | :-----: | :------: | :-----: | 
| `f1` |   | | | 
| `f2` |   | | | 
| `f3` |   | | | 
| `f4` |   | | | 
| `f5` |   | | | 
| `f6` |   | | | 
| `f7` |   | | | 
| `f8` |   | | | 
| `f9` |   | | | 
| `f10` |   | | | 
| `f11` |   | | | 
| `f12` |   | | | 
| `f13` |   | | | 


## Part 2: Combinatorial proof

An important method of proof we'll see much more of in a few weeks is called *combinatorial proof*. It is a method of reasoning used when you want to show that two sets have the same cardinality (i.e. the same "size"). The approach is to **create a bijective function from one of the sets to the other**. Since a bijection is a one-to-one correspondence between the elements of the domain and range, having a bijection lets us conclude that the domain and range have the same cardinality (size) even when those sets are infinite. 

This part runs through a basic example that will reappear soon. 

Let $B_4$ be the set of all binary strings of length $4$. For example `0111` and `1101` are both elements of $B_4$. Let $P(\{1,2,3,4\})$ be the power set of $\{1,2,3,4\}$ (the set of all subsets of $\{1,2,3,4\}$ as discussed in class earlier). 

1. Write out all the elements of $B_4$. There should 16 of these because they are just the decimal numbers 0 through 15 written in binary. 
2. Now look at the following function $f: B_4 \rightarrow P(\{1,2,3,4\})$. Given a binary string, create a subset of $\{1,2,3,4\}$ as follows: If the bit in position $n$ is 1, include the number $n$ in the subset. Otherwise do not include it. For example $f(0111) = \{2,3,4\}$ and $f(1101) = \{1,2,4\}$. 
3. Make a table of values for $f$ showing the outputs of all 16 possible inputs. Then use the table to explain why $f$ is a bijection. 
4. Based on question 3, how many subsets does $\{1,2,3,4\}$ have? 
5. Can you extend this idea to count the number of subsets of $\{1,2,3,\dots, n\}$ for any positive integer $n$? 


## Part 3: Cardinality of infinite sets is weird 

Consider the following function $f$ whose domain is $\mathbb{N}$ and whose codomain is $\mathbb{Z}$: 

- If the input $n$ is an even natural number, then $f(n) = 2n$. 
- If the input $n$ is an odd natural number, then $f(n) = -\frac{n+1}{2}$. 

Do the following: 

1. Make a table of values for this function from $n=0$ to $n=10$. (Watch your arithmetic when the input is odd. For example $f(5)$ should be $-3$.) 
2. Determine if the function is injective, surjective, bijective, or none of these. 
3. Based on the results of the second question, how does the cardinality of $\mathbb{N}$ compare to the cardinality of $\mathbb{Z}$? Don't rely on intuition -- use question 2 (also the idea in part 2). 
4. The outcome of question 3 should strike you as really weird. Why? 