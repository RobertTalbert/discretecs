Hello again. We're looking some more at processes for counting complex arrangements of objects. In the first two videos we learned how to count the number of subsets of a finite set, the number of bit strings of length n, and then the number of k-element subsets of an n-element set. In the last video we saw that counting these arrangements isn't always as simple as applying the additive or multiplicative principles, but that we have to beware of overcounting. 

In this video we're going to take on yet another counting problem, counting the number of bit strings that have a certain "weight". 

Specifically we are going to look at the problem of counting the number of n-bit strings that have a weight of k, and we're introducing a new method for doing so, namely the extremely important idea of recursion and the related notion of a recurrence relation. 

First of all by the weight of a bit string we just mean the number of 1's that are in it. Or you can think of weight as the sum of all the bits. For example here's an 8-bit string with weight 4. Some notation here. B,n,k is the set of all n-bit strings with weight k -- for example here's B,4,2 which is the set of all 4-bit strings having weight 2 and you can see that the cardinality of this set is 6. 

So let's think about the cardinality of B,5,3 which is the number of 5-bit strings that have a weight of 3. We could sit down and look at all 


<!--stackedit_data:
eyJoaXN0b3J5IjpbNjQxODg4MzM0XX0=
-->