Hello again. We're looking some more at processes for counting complex arrangements of objects. In the first two videos we learned how to count the number of subsets of a finite set, the number of bit strings of length n, and then the number of k-element subsets of an n-element set. In the last video we saw that counting these arrangements isn't always as simple as applying the additive or multiplicative principles, but that we have to beware of overcounting. 

In this video we're going to take on yet another counting problem, counting the number of bit strings that have a certain "weight". 

Specifically we are going to look at the problem of counting the number of n-bit strings that have a weight of k, and we're introducing a new method for doing so, namely the extremely important idea of recursion and the related notion of a recurrence relation. 

First of all by the weight of a bit string we just mean the number of 1's that are in it. Or you can think of weight as the sum of all the bits. For example here's an 8-bit string with weight 4. Some notation here. B,n,k is the set of all n-bit strings with weight k -- for example here's B,4,2 which is the set of all 4-bit strings having weight 2 and you can see that the cardinality of this set is 6. 

So let's think about the cardinality of B,5,3 which is the number of 5-bit strings that have a weight of 3. We could sit down and look at all 2^5 or 32 possible 5-bit strings and just highlight the ones that have weight 3, but that seems inefficient and it wouldn't scale up to longer bit strings. Instead, we're going to introduce a powerful concept used throughout computer science to solve problems --- recursion. 

Recursion is the process of solving a problem by reducing it to smaller or simpler copies of the same problem, that eventually terminate in a starting condition. 

Recursion is used in many, many real applications, for example sorting algorithms. One common algorithm, merge sort, sorts a list of numbers by defining how to sort a 0- or 1-element list, then defining "mergesort" of an 8-element list" is a combination of mergesort on two 4-element lists. Note here in the Python code that the function calls itself, on a smaller list. That's the essence of recursion. Then the mergesort on 4 element lists is done by calling mergesort on 2-element lists, which is then done by calling mergesort on 1 elements lists -- and then the starting conditions kick in, and the program tells how to piece together the smaller lists.  

Let's see how recursion can be used to help us count the number of 5-bit strings of weight 3. First, here are a couple of examples. The key observation here is simple: Every 5-bit string of weight 3 --- in fact any 5-bit string of any weight --- has to start on the left with either a 0 or a 1. So a 5-bit string of weight 3 is one of two things: Its either a 1 followed by a 4-bit string of weight 2 (since the total weight is 3, the rest of the bits have to add up to 2) or it's a 0 followed by a 4-bit string of weight 3. 

Since no 5-bit string can have with both a 1 and a 0 in the leftmost bit, the number of 5-bit strings of weight 3 will be the SUM of two things: The number of 4 bit strings of weight 2, plus the number of 4 bit strings of weight 3. This is the additive principle of counting which we haven't seen in a while. We don't have to apply the principle of inclusion-exclusion here because these two sets have no elements in common. 

So although we have't yet counted the number of 5-bit strings of weight 3, we've expressed this number in terms of smaller and simpler versions of the same problem. This equation you see here isn't a formula where we plug in the numbers and get an answer, but rather it's called a recurrence relation --- it expresses the quantity we want to find in terms of smaller versions of itself. 

Now we need to find out how to get these two other numbers. 

We can make up a similar recurrence relation for B,4,3 and B,4,2. Let's focus just on B43 for now. 

B43 is the set of 4-bit strings with weight 3. Just as with B5,3, every such bit string is one of two things: A 1 followed by a 3-bit string with weight 2, or a 0 followed by a 3 bit string of weight 3. Now we know there are B32 of the first kind and B33 of the second kind and there's no bit string that belongs to both sets. So B43 is B33 plus B32. It's yet another recurrence relation. 

At this point it's helpful to stop and make a generalization about Bnk for ANY value of n and k. The same recurrence relation should hold. Let's say you have an n-bit string of weight k. That bit string has to start on the left with either 0 or 1. So it's one of two things: A 1 followed by a bit string of 1 fewer bits (length n-1) that has a weight of k-1 since all the bits have to add up to k; or it's a 0 followed by an n-1 bit string of weight k since again all the bits have to add up to k. The number of the first kind is B,n-1,k-1 and the number of the second kind is B,n-1,k. So we get this recurrence relation here for any n,k by adding the two cardinalities together. 

We're going to use this recurrence relation to finally compute B5,3 but there's two special cases to bring up. One is where the n and k are equal to each other. The set Bnn is the set of all n-bit strings that have weight n but there is only one such bit string, namely the bit string of all 1's. If you had any 0's in a string of length n, the weight would be less than n. Therefore the number Bnn is 1. 

Similarly Bn,0 is the set of all n-bit strings of weight 0, and there's only one such string, namely the string of all 0's. Therefore the number Bn0 is also 1. 

So armed with the recurrence relation and these two special cases, we can now compute B53. [[..just talk ]]] 

--

Two observations to make at this point. 

First, the computation on the previous slide works, but it seems inefficient still. In fact, unless we wrote some code to do this for us, it seems like recursion is not a great way to actually count things. Instead it's a really great way to identify deep relationships between the objects that we're counting. So don't take all this as a kind of algorithm-- think of it more as a way of understanding the mathematical relationships between the objects. 

Second, doesn't this seem familiar? The number of 5-bit strings of weight k was 10. And earlier we saw that the number of 3-element subsets of a 5-element set was also 10. Is this a coincidence? Stay tuned to find out. 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM4OTc4NDUzOF19
-->