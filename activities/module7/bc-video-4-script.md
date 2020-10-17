Welcome to this fourth video in a series on counting complex arrangements. Previously we've learned how to count the number of subsets of a finite set and the number of bit strings with length n; and the more complex situations of k-element subsets of an n-element set and n-bit strings with weight k. At the end of the last video we teased a connection between these last two that we're going to explore now. 

So in this video, we're going to revisit an earlier idea that if I want to count a two collections of objects and I know how to count one of those collections, I can count the other by setting up a bijection between the two sets I'm counting. In this video we're going to build a bijection between the collection of k-element subsets of an n=element set and the collection of n-bit strings with weight k. Since those are both finite sets, this will show they have the exact same number of elements so the count of one set equals the count of the other --- and more importantly all the methods and relationships we used to count one can be used to count the other. 

We already did this in a special case earlier, when we were counting bit strings and subsets. We said that we can form a subset of a finite set by voting for it using a ballot, and then noticed that every ballot is really just a bit string in disguise. That mapping of ballots onto bitstrings was a bijection, so the number of subsets and the number of bit strings was the same. 



<!--stackedit_data:
eyJoaXN0b3J5IjpbMjg2NjIwNjk3XX0=
-->