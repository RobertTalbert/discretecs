Hi again. This is the second video in a series introducing some fundamental tools and concepts for counting complex arrangements. In the previous video, we learned how to count two different-looking collections of objects: The collection of all subsets of a finite set having n elements, and the collection of all n-bit strings. We learned that the number of such objects is 2^n for both collections and this was no coincidence, since there was a bijection between the two sets that identifies each element of one collection as an element of the other. 

In this video, we're going to look at a similar but different problem: counting the number of subsets of an n-element set, that have exactly k elements. We're going to see that there's a wrong way to count this collection and a right way. And the right way is going to introduce an important new idea for us. 

First of all here's what we mean by "k-element subsets of an n-element set". For example we might want all the 3-element subsets of a 5-element set. We learned last time that there are 2^5 of 32 subsets of a set with 5 elements. To really see these subsets and start to detect patterns in how they are built, I encourage you right now to stop the video and just try writing all 32 subsets of the set {1,2,3,4,5}. Go ahead, try it! 

If you've found all of them, you should be looking at this list. Of those 32 subsets, you can see that just 10 of them have 3 elements. So the number of 3-element subsets of a 5-element set, is 10. The number of 4-element subsets of a 5-element set is 5. And so on. 

So how would we count the number of 3-element subsets of a 5-element set OTHER than by enumerating them -- that is, by listing them and counting on our fingers? We need some kind of algorithm for doing this in case we need to count a collection so large that enumeration isn't practical (like, the number of 100-element subsets of a 1000-element set). 

Here's a well-intention but WRONG way to do this. 

So we begin by creating a generic 3-element subset and leave three blanks where the elements should go. Since there are 5 elements in the main set, there are 5 ways to fill in the first blank, then 4 ways to fill in the second because repetitions aren't allowed in sets, then 3 ways to fill in the third one. Since that's a sequence of tasks, we multiply 5*4*3 to get 60 possible ways to form those sets. 

This sounds good at first because it's a similar counting process to how we counted the number of subsets of a set, and the number of n-bit strings in the first video. But it's wrong -- on two counts. 

First of all, the number of 3-element subsets can't possibly be 60, because there only 32 possible subsets of ANY size for this 5-element set. So this number 60 is impossibly large. 

And second, the reason that it's so large is that we've counted many subsets more than once. For example in this sequence-of-choices approach I could choose 1 for the first slot,  
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTc0MjQwMTIxXX0=
-->