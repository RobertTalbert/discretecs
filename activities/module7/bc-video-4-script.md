Welcome to this fourth video in a series on counting complex arrangements. Previously we've learned how to count the number of subsets of a finite set and the number of bit strings with length n; and the more complex situations of k-element subsets of an n-element set and n-bit strings with weight k. At the end of the last video we teased a connection between these last two that we're going to explore now. 

So in this video, we're going to revisit an earlier idea that if I want to count a two collections of objects and I know how to count one of those collections, I can count the other by setting up a bijection between the two sets I'm counting. In this video we're going to build a bijection between the collection of k-element subsets of an n=element set and the collection of n-bit strings with weight k. Since those are both finite sets, this will show they have the exact same number of elements so the count of one set equals the count of the other --- and more importantly all the methods and relationships we used to count one can be used to count the other. 

We already did this in a special case earlier, when we were counting bit strings and subsets. We said that we can form a subset of a finite set by voting for it using a ballot, and then noticed that every ballot is really just a bit string in disguise. That mapping of ballots onto bitstrings was a bijection, so the number of subsets and the number of bit strings was the same. 

So let's do something similar now. We're going to build a bijection from the set of k-element subsets of an n-element set, to the set of n-bit strings with weight k. We never really came up with a formula for the size of the first set, just a method for counting it that involved doing an incorrect count and then dividing off by an error factor to correct it. But we do have a number for the second set, namely Bnk which we can get by repeated application of a recurrence relation. Once we have a bijection, we can conclude that Bnk also counts the first collection. 

Here's the mapping. We start with a main set with n elements, labeled a1 through an. Take a k-element set which is some selection of k elements from this n element set. We will turn this into a bit string as follows: 

Set up an n-bit string with n blanks in it. 
Look at the main set and loop through its elements: 
If ai is in the subset we have, then we put a 1 for the bit in position i. Otherwise we put a 0. Then return the bit string. 

Notice that the bit string will have weight k because the process above puts exactly k "1" bits in the string. 

Here's an example of the inputs on the left and the outputs on the right of this process in the case where we are looking at 3-element subsets of a 5-element set. 

In the second line, it shows that if we take the same set but written in a different order, it produces the same output which is what it should do. That's not a collision but rather illustrating that this mapping is a well defined function. 

[talk through bijection]

So what this proves is that the collection of k-element subsets of an n-element set, and the collection of n-bit strings of weight k, are in a very deep sense THE SAME. They have the same number of elements, namely this number Bnk. And importantly they obey the same relationships with each other, especially the recurrence relation we built up in the last video. They are really just two different viewpoints or expressions of the same data structure and we can represent one with the other. 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc1MjA5MDI2LC01Mzc5NzEzMDVdfQ==
-->