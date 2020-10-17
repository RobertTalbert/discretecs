**Ordering:**

1. "Counting subsets and bit strings"
2. "Counting the k-element subsets of a set"
3. "Counting bit strings of weight k"
4. "How sets and bit strings are the same"
5. "Introducing the binomial coefficient" 

---

## Counting the number of subsets of a set
- Example using 3 elements then list them 
- Example using 5 elements
- Example in general
- How this is like counting bit strings 


## Counting the k-element subsets of a set

- How not to count the number of $k$-element subsets of a set 
	- Using the multiplicative principle and 4 elements 
	- Overcounting 
- The right way to count the number of $k$-element subsets of a set
	- Start off the "wrong" way
	- Count the number of ways to rearrange the $k$-element sets -- multiplicative principle
	- Then divide off
	- Example: 6 element subsets of a 10-element set -- compute, then use Python


## Counting bit strings of weight k

- Counting bit strings of weight $k$ using recursion 
	- What "weight k" means 
	- Problem: How many n-bit strings of weight k? 
	- Notation $B_k^n$ and the cardinality of that set is the number
	- Example $B_2^4$ so the cardinality is 6$
		- 1100, 0011, 1010, 0101, 1001, 0101
	- What is $|B_3^5|$? 
		- Enumeration not a good idea
		- Use recursion! Defining a problem in terms of smaller versions of itself 
		- Given a bit string xxxxx in this set: It's either 
			- A string of the form 1xxxx with weight 2 or 
			- A string of the form 0xxxx with weight 3
			- Two sets, disjoint
			- So $|B_3^5| = |B_2^4| + |B_3^4|$
			- Now look at $B_2^4$ -- can be split into sets with strings of the form 1xxx of weight 1 or 0xxx of weight 2, so $|B_2^4|= |B_1^3| + |B_2^3|$   -- can count those directly, 3 and 3 respectively
			- Can count $B_3^4$ directly -- must be 4
			- So $|B_3^5| = 3 + 3 + 4 = 10$. 
	- Recurrence relation in general.... 

## How sets and bit strings are the same

- Why counting bit strings is the same thing as counting subsets 
	- Number of 3-element subsets of a 5-element set --- 5x4x3 / 3x2x1 = 10....... 
	- Bijection between counting problems: 
		- Map 3-element subsets onto 5-bit strings of weight 3:
		- Original set is {a,b,c,d,e}. Let {x,y,z} be a 3-element subset. 
		- Set up a bit string xxxxx. If a is in the subset, first bit is 1, 0 otherwise.   If b is in the subset, second bit is 1, 0 otherwise, and so on. 
		- Example: {c,d,e} would map to the string 00111. {a,c,d} maps to 10110. {d,c,a} maps to 10110 so notice same set, different arrangement maps to the same string, so this is a function. 
		- Is is a surjection? Yes, given any 5-bit string of length 3 you can find the set that maps to it. Example 01101 is hit by {b,c,e}. 
		- Is it an injection? Yes, there are no collisions -- if two sets are really different, then one has an element the other does't have, which will result in a different 1 bit. 
	- So the set of k-element subsets is the same cardinality as the set B_3^5. Therefore the number |B_3^5| counts them both! 
	- This is a "combinatorial proof" 

## The binomial coefficient 
- Wolfram|Alpha -- expand (x+y)^n and look at the coefficient on the terms. 
- Do (x+y)^5 -- look at 3d term -- look familiar? 
- The binomial coefficient binom(n,k) counts ALL these things:
		- k-element subsets
		- weight k bit strings
		- coefficient on terms
		- In general the number of ways to select ....

- Bonus: A recursive look at why binom(n,k) is the coefficient on the kth term 
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkxNDgwOTAwOSw4MTQ1NTY5NzYsLTgzMj
IyODI4LDEwNDgwNzQ5MDhdfQ==
-->