Hi again. This is the second video in a series introducing some fundamental tools and concepts for counting complex arrangements. In the previous video, we learned how to count two different-looking collections of objects: The collection of all subsets of a finite set having n elements, and the collection of all n-bit strings. We learned that the number of such objects is 2^n for both collections and this was no coincidence, since there was a bijection between the two sets that identifies each element of one collection as an element of the other. 

In this video, we're going to look at a similar but different problem: counting the number of subsets of an n-element set, that have exactly k elements. We're going to see that there's a wrong way to count this collection and a right way. And the right way is going to introduce an important new idea for us. 

First of all here's what we mean by "k-element subsets of an n-element set". For example we might want all the 3-element subsets of a 5-element set. We learned last time that there are 2^5 of 32 subsets of a set with 5 elements. To really see these subsets and start to detect patterns in how they are built, I encourage you right now to stop the video and just try writing all 32 subsets of the set {1,2,3,4,5}. Go ahead, try it! 

If you've found all of them, you should be looking at this list. Of those 32 subsets, you can see that just 10 of them have 3 elements. So the number of 3-element subsets of a 5-element set, is 10. The number of 4-element subsets of a 5-element set is 5. And so on. 

So how would we count the number of 3-element subsets of a 5-element set OTHER than by enumerating them -- that is, by listing them and counting on our fingers? We need some kind of algorithm for doing this in case we need to count a collection so large that enumeration isn't practical (like, the number of 100-element subsets of a 1000-element set). 

Here's a well-intention but WRONG way to do this. 

So we begin by creating a generic 3-element subset and leave three blanks where the elements should go. Since there are 5 elements in the main set, there are 5 ways to fill in the first blank, then 4 ways to fill in the second because repetitions aren't allowed in sets, then 3 ways to fill in the third one. Since that's a sequence of tasks, we multiply 5*4*3 to get 60 possible ways to form those sets. 

This sounds good at first because it's a similar counting process to how we counted the number of subsets of a set, and the number of n-bit strings in the first video. But it's wrong -- on two counts. 

First of all, the number of 3-element subsets can't possibly be 60, because there only 32 possible subsets of ANY size for this 5-element set. So this number 60 is impossibly large. 

And second, the reason that it's so large is that we've counted many subsets more than once. For example in this sequence-of-choices approach I could choose the number 1 for the first slot, the number 2 for the second, and the number 3 for the third slot to get the set {1,2,3}; or I could choose the number 2 for the first slot, 1 for the second, and 3 for the third and get the set {2,1,3}. Now obviously those are the same set because ordering of elements doesn't matter; but my counting process counts them as different outcomes. So when I count 60 subsets, that 60 includes a lot of duplicates that are only superficially the same. 

There are 6 versions of that one subset {1,2,3} that are counted separately. In fact, in the "wrong way" method, every possible rearrangement of a 3-element subset is counted separately. So let's solve a different counting problem: How many possible rearrangements of a 3-element set are there? 

We could do it this way. Start with a blank 3-element set. There are 3 choices for the first blank, 2 for the second, and 1 for the third. Since that's a sequence of choices, we can multiply the possibilities and see that there are 6 possible rearrangements of elements of a 3-element set. 

So the count of 60 is off by a factor of 6 since every time a 3-element subset of {1,2,3,4,5} is chosen, the "wrong way" method counts it six times. So we can actually redeem the "wrong way" method by taking its outcome of 60 and dividing by 6, and there's the 10 that we counted by listing those subsets. 

Later in this series we're going to have a more efficient way of counting these k-element subsets, but just to illustrate the concept once again, let's count a collection of subsets that would be hard to do by listing all the objects--- the number of 4-element subsets of a 10-element set. There are 2^(10) or 1024 subsets of a 10-element set and I don't feel like listing all of those out! 

So start with the wrong-way method, and set up a generic 4-element subset by listing 4 blanks. There are 10 ways to fill in the first blank, 9 for the second, 8 for the third, and 7 for the fourth, for a total of 5040 ways to fill in the blanks. Of course that's wrong because there are only 1024 total subsets possible. It's too big because when we count one 4-element subset we are counting all possible rearrangements separately. So how many such rearrangements are there? 

Given a 4-element subset, there are 4 choices for the first blank, 3 for the second, 2 for the third, and just 1 remaining for the last one. So that's 4*3*2*1 = 24 possible rearrangements. That means my wrong-way count of 5040 was 24 times too large! So the real number of 4-element subsets is 5040/24 or 210 of them. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgyNzk1NjkzOSwtMTgxNjM1NzMxOV19
-->