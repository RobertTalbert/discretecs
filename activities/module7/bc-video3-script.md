Hello again. We're looking some more at processes for counting complex arrangements of objects. In the first two videos we learned how to count the number of subsets of a finite set, the number of bit strings of length n, and then the number of k-element subsets of an n-element set. In the last video we saw that counting these arrangements isn't always as simple as applying the additive or multiplicative principles, but that we have to beware of overcounting. 

In this video we're going to take on yet another counting problem, counting the number of bit strings that have a certain "weight". 

Specifically we are going to look at the problem of counting the number of n-bit strings that have a weight of k, and we're introducing a new method for doing so, namely the extremely important idea of recursion and the related notion of a recurrence relation. 

First of all by the weight of a bit string we just mean the number of 1's that are in it. Or you can think of weight as the sum of all the bits. For example here's an 8-bit string with weight 4. Some notation here. B,n,k is the set of all n-bit strings with weight k -- for example here's B,4,2 which is the set of all 4-bit strings having weight 2 and you can see that the cardinality of this set is 6. 

So let's think about the cardinality of B,5,3 which is the number of 5-bit strings that have a weight of 3. We could sit down and look at all 2^5 or 32 possible 5-bit strings and just highlight the ones that have weight 3, but that seems inefficient and it wouldn't scale up to longer bit strings. Instead, we're going to introduce a powerful concept used throughout computer science to solve problems --- recursion. 

Recursion is the process of solving a problem by reducing it to smaller or simpler copies of the same problem, that eventually terminate in a starting condition. 

Recursion is used in many, many real applications, for example sorting algorithms. One common algorithm, merge sort, sorts a list of numbers by defining how to sort a 0- or 1-element list, then defining "mergesort" of an 8-element list" is a combination of mergesort on two 4-element lists. Note here in the Python code that the function calls itself, on a smaller list. That's the essence of recursion. Then the mergesort on 4 element lists is done by calling mergesort on 2-element lists, which is then done by calling mergesort on 1 elements lists -- and then the starting conditions kick in, and the program tells how to piece together the smaller lists.  

Let's see how recursion can be used to help us count the number of 5-bit strings of weight 3. First, here are a couple of examples. The key observation here is simple: Every 5-bit string of weight 3 --- in fact any 5-bit string of any weight --- has to start on the left with either a 0 or a 1. So a 5-bit string of weight 3 is one of two things: Its either a 1 followed by a 4-bit string of weight 2 (since the total weight is 3, the rest of the bits have to add up to 2) or it's a 0 followed by a 4-bit string of weight 3. 

Since no 5-bit string can have with both a 1 and a 0 in the leftmost bit, the number of 5-bit strings of weight 3 will be the SUM of two things: The number of 4 bit strings of weight 2, plus the number of 4 bit strings of weight 3. This is the additive principle of counting which we haven't seen in a while. We don't have to apply the principle of inclusion-exclusion here because these two sets have no elements in common. 

So  count the number of 5-bit strings of weight 3 




<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY3NzU3Mjg3OSwtODE0NDUxNTc4XX0=
-->