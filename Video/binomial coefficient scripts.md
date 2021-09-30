# Scripts for Binomial coefficient videos

## Overall plan

Edit these down or redo the audio and video to get: 

- The BC as solution to a counting problem
- The BC as the entries of Pascal's triangle
- The BC as a formula

As it is: 

- Video 1: Doesn't involve the BC but shows how to count the elements of one set by counting another and then using a bijection; subsets of A vs. bitstrings 
- Video 2: Counting number of k-element subsets by overcounting then dividing off by error factor
- Video 3: intro to recursion and recurrence relations, and counting weight k bit strings
- Video 4: Counting k-element subsets by countint weight k bit strings 
- Video 5: Introducing BC at last (and doing stuff with (x+y)^n)

**Maybe need:** 

- Another video for a formula for the BC 


## Video 1

Hello there. This is the first of a short sequence of videos that will introduce some very important and fundamental ideas about counting complex arrangements. 

In this video, we're going to give an argument for how to count two different collections of objects: First, we'll count the number of subsets that a finite set with n elements has, and second we'll count the number of ways to form a string of bits of length n. Importantly, we're going to see that there's a deep connection between these two counting problems and that actually they are the same counting problem, and by counting one collection we count the other automatically. 

Let's first look at subsets. Just a reminder of two facts about subsets: First given any set A, the empty set or null set is a subset of A, because of the underlying logic of how  "being a subset" is defined; and secondly, A is automatically a subset of itself also by the logic of the definition. 

With that in mind, let's see if we can figure out a pattern in the number of subsets that a set with n elements has, by first looking at some examples. 

Let's start with the simplest possible set, the empty set. You might think that the empty set has no subsets, but in fact it has exactly one: The empty set itself, because of what we mentioned on the previous slide. The empty set has zero elements, but 1 subset. 

What about a set with one element? Let's just call that generic element "a". Well, this one-element set has two subsets --- the empty set, and the entire set we started with. 

What about a set with two elements, which we'll call a and b? This has 4 subsets -- the empty set, both one-element proper subsets, and the entire set itself. 

And you can see that if n = 3, a set with three elements has 8 subsets, and if n = 4, a set with four elements will have 16 subsets. It feels like the number of subsets is growing exponentially and that is precisely the right term to use, because all of these numbers in the rightmost column are powers of 2, and every time we add an element to our main set, we double the number of subsets it has. 

So a good conjecture, which is math-speak for an "educated guess", is that if A has n elements, then it has 2^n subsets. How can we prove that this will be true for every natural number n? We can't just continue to give examples because we'll never cover all possible examples. So we need to use some logic and argumentation. Here's one argument. 

A way to think about creating a subset of A is to loop through all n of its elements and essentially vote for whether to include it or not. Make a little ballot with one entry for each of the elements of A, and put a check next to that element if you want to include it in the subset and an x otherwise. All the elements that have checks under them would then go into the subset. Now, every subset of A can be created with such a ballot, so if we can count the number of possible ballots that could be made out, we'll have counted the number of subsets of A. In other words, there are exactly the same number of subsets of A, as there are ballots used to create those subsets. 

So how many ballots are there? Well, filling out a ballot is a sequence of tasks. There are two outcomes for each task -- either a check or an x -- and each task is independent of the othrs. Ad there are n of them. So the multiplicative principle of counting says the number of outcomes is 2 times 2 times 2... etc until we have n 2's multiplied together. That's 2^n and that's the number of subsets of A. 


With that counting problem solved let's look at another, namely counting the number of strings of bits --- 0s or 1s --- of length n. Well, how do you form an n-bit string? You can think of it as creating n blanks, one for each bit, and then deciding for each blank to put either a 0 or a 1 in it. How many ways are there to do this? Well, we choose 0 or 1 for each bit; This is a sequence of n tasks, all independent and each with 2 choices. So the number of ways to complete this sequence is 2^n. 

Now this ought to look and feel very familiar. 

In fact the ballot that we used to count subsets could very easily be thought of as a string of n bits. You can take a ballot and turn it into an n-bit string just by creating n blanks and putting a 1 in a blank if there's a check in the corresponding place on the ballot, and putting a 0 in the bit string otherwise. This way of mapping ballots onto bit strings is actually a bijection. No two different ballots get mapped to the same bitstring; and given any bit string, I can reconstruct a ballot that gets mapped to it. Since the set of ballots is finite, and there's a bijection from it to the set of n-bit strings. the set of n-bit strings has the exact same number of elements as the set of ballots, namely 2^n.


So what we've learned here is that 
- Every n-element set has 2^n subsets
- There are 2^n n-bit strings 
- And in fact there's a bijection between the set of subsets of an n-element set and the set of all possible n-bit strings. 
- So this illustrates and important counting rule: If I can count a finite set of objects and create a bijection between it and another collection of objects, then I've counted the second collection as well. 

Thanks for watching. 

## Video 2

Hi again. This is the second video in a series introducing some fundamental tools and concepts for counting complex arrangements. In the previous video, we learned how to count two different-looking collections of objects: The collection of all subsets of a finite set having n elements, and the collection of all n-bit strings. We learned that the number of such objects is 2^n for both collections and this was no coincidence, since there was a bijection between the two sets that identifies each element of one collection as an element of the other.

In this video, we're going to look at a similar but different problem: counting the number of subsets of an n-element set, that have exactly k elements. We're going to see that there's a wrong way to count this collection and a right way. And the right way is going to introduce an important new idea for us.

First of all here's what we mean by "k-element subsets of an n-element set". For example we might want all the 3-element subsets of a 5-element set. We learned last time that there are 2^5 of 32 subsets of a set with 5 elements. To really see these subsets and start to detect patterns in how they are built, I encourage you right now to stop the video and just try writing all 32 subsets of the set {1,2,3,4,5}. Go ahead, try it!

If you've found all of them, you should be looking at this list. Of those 32 subsets, you can see that just 10 of them have 3 elements. So the number of 3-element subsets of a 5-element set, is 10. The number of 4-element subsets of a 5-element set is 5. And so on.

So how would we count the number of 3-element subsets of a 5-element set OTHER than by enumerating them -- that is, by listing them and counting on our fingers? We need some kind of algorithm for doing this in case we need to count a collection so large that enumeration isn't practical (like, the number of 100-element subsets of a 1000-element set).

Here's a well-intention but WRONG way to do this.

So we begin by creating a generic 3-element subset and leave three blanks where the elements should go. Since there are 5 elements in the main set, there are 5 ways to fill in the first blank, then 4 ways to fill in the second because repetitions aren't allowed in sets, then 3 ways to fill in the third one. Since that's a sequence of tasks, we multiply 543 to get 60 possible ways to form those sets.

This sounds good at first because it's a similar counting process to how we counted the number of subsets of a set, and the number of n-bit strings in the first video. But it's wrong -- on two counts.

First of all, the number of 3-element subsets can't possibly be 60, because there only 32 possible subsets of ANY size for this 5-element set. So this number 60 is impossibly large.

And second, the reason that it's so large is that we've counted many subsets more than once. For example in this sequence-of-choices approach I could choose the number 1 for the first slot, the number 2 for the second, and the number 3 for the third slot to get the set {1,2,3}; or I could choose the number 2 for the first slot, 1 for the second, and 3 for the third and get the set {2,1,3}. Now obviously those are the same set because ordering of elements doesn't matter; but my counting process counts them as different outcomes. So when I count 60 subsets, that 60 includes a lot of duplicates that are only superficially the same.

There are 6 versions of that one subset {1,2,3} that are counted separately. In fact, in the "wrong way" method, every possible rearrangement of a 3-element subset is counted separately. So let's solve a different counting problem: How many possible rearrangements of a 3-element set are there?

We could do it this way. Start with a blank 3-element set. There are 3 choices for the first blank, 2 for the second, and 1 for the third. Since that's a sequence of choices, we can multiply the possibilities and see that there are 6 possible rearrangements of elements of a 3-element set.

So the count of 60 is off by a factor of 6 since every time a 3-element subset of {1,2,3,4,5} is chosen, the "wrong way" method counts it six times. So we can actually redeem the "wrong way" method by taking its outcome of 60 and dividing by 6, and there's the 10 that we counted by listing those subsets.

Later in this series we're going to have a more efficient way of counting these k-element subsets, but just to illustrate the concept once again, let's count a collection of subsets that would be hard to do by listing all the objects--- the number of 4-element subsets of a 10-element set. There are 2^(10) or 1024 subsets of a 10-element set and I don't feel like listing all of those out!

So start with the wrong-way method, and set up a generic 4-element subset by listing 4 blanks. There are 10 ways to fill in the first blank, 9 for the second, 8 for the third, and 7 for the fourth, for a total of 5040 ways to fill in the blanks. Of course that's wrong because there are only 1024 total subsets possible. It's too big because when we count one 4-element subset we are counting all possible rearrangements separately. So how many such rearrangements are there?

Given a 4-element subset, there are 4 choices for the first blank, 3 for the second, 2 for the third, and just 1 remaining for the last one. So that's 432*1 = 24 possible rearrangements. That means my wrong-way count of 5040 was 24 times too large! So the real number of 4-element subsets is 5040/24 or 210 of them.

So in this video we've learned that counting the number of k-element subsets of an n-element set is NOT just a straightforward application of the multiplicative rule because we end up overcounting our objects. Always be careful about whether a counting algorithm counts objects more than once!

But we also saw that we can determined by just how much we overcounted, and correct the wrong count by dividing off by that factor. Thanks for watching.

## Video 3

Hello again. We're looking some more at processes for counting complex arrangements of objects. In the first two videos we learned how to count the number of subsets of a finite set, the number of bit strings of length n, and then the number of k-element subsets of an n-element set. In the last video we saw that counting these arrangements isn't always as simple as applying the additive or multiplicative principles, but that we have to beware of overcounting.

In this video we're going to take on yet another counting problem, counting the number of bit strings that have a certain "weight".

Specifically we are going to look at the problem of counting the number of n-bit strings that have a weight of k, and we're introducing a new method for doing so, namely the extremely important idea of recursion and the related notion of a recurrence relation.

First of all by the weight of a bit string we just mean the number of 1's that are in it. Or you can think of weight as the sum of all the bits. For example here's an 8-bit string with weight 4. Some notation here. B,n,k is the set of all n-bit strings with weight k -- for example here's B,4,2 which is the set of all 4-bit strings having weight 2 and you can see that the cardinality of this set is 6. So just to clarify, B,n,k is the *set* whose elements are n-bit strings of weight k, and this is the cardinality of that set, which is the number of n-bit strings of weight k. 

So let's think about the cardinality of B,5,3 which is the number of 5-bit strings that have a weight of 3. One way to count this number is by brute force, by just listing all 2^5 possible 5-bit strings of any weight and then picking out the ones that have weight 3 and counting the result. But that seems like more work than necessary, and it wouldn't scale up to longer bit strings. Instead, we're going to introduce a powerful concept used throughout computer science to solve problems --- recursion.

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

So armed with the recurrence relation and these two special cases, we can now actually find the number of 5-bit strings with weight 3. We're going to do this using recursion and the recurrence relation we saw earlier, which I've copied here for reference. We'll also need the two special cases to help us end the recursive process: B, n, 0 and B,n,n both equal 1 for any natural number n. 

Starting with B53, use the recurrence relation to reduce this to B43 plus B42. We don't know what those two numbers equal, but we can use the recurrence relation again on each of them to reduce some more. B43 becomes B33 plus B32, and B42 becomes B32 plus B31. Now I'm going to do a couple of things here. First, B33 equals 1 because that's one of our special cases. Second, I see two copies of B32 so I'm just going to combine those into one. I have B32 and B31 and I don't know the values of those, but again I can keep applying the recurrence relation to simplify. 

B32 becomes B22 plus B21 and the B31 becomes B21 plus B20. Now B22 equals 1, B21 is B11 plus B10, here's another B21 that equals the same thing, and B20 is 1 because that's our other special case. Everything that remains is now a special case and equals 1. So we have 1 + 2 times (1+1+1) + (1 + 1 + 1). That's 1 + 2*3 + 3 which is 10. 
--

Two observations to make at this point.

First, the computation you just saw, using recursion *works*, but it seems inefficient still. In fact, unless we wrote some code to do this for us, it seems like recursion is not a great way to actually count things. Instead it's a really great way to identify deep relationships between the objects that we're counting. So don't take all this as a kind of algorithm-- think of it more as a way of understanding the mathematical relationships between the objects. 

Second, doesn't this seem familiar? The number of 5-bit strings of weight 3 was 10. And earlier we saw that the number of 3-element subsets of a 5-element set was also 10. Is this a coincidence? Stay tuned to find out.

## Video 4

Welcome to this fourth video in a series on counting complex arrangements. Previously we've learned how to count the number of subsets of a finite set and the number of bit strings with length n; and the more complex situations of k-element subsets of an n-element set and n-bit strings with weight k. At the end of the last video we teased a connection between these last two that we're going to explore now.

So in this video, we're going to revisit an earlier idea that if I want to count a two collections of objects and I know how to count one of those collections, I can count the other by setting up a bijection between the two sets I'm counting. In this video we're going to build a bijection between the collection of k-element subsets of an n=element set and the collection of n-bit strings with weight k. Since those are both finite sets, this will show they have the exact same number of elements so the count of one set equals the count of the other --- and more importantly all the methods and relationships we used to count one can be used to count the other.

We already did this in a special case earlier, when we were counting bit strings and subsets. We said that we can form a subset of a finite set by voting for it using a ballot, and then noticed that every ballot is really just a bit string in disguise. That mapping of ballots onto bitstrings was a bijection, so the number of subsets and the number of bit strings was the same.

So let's do something similar now. We're going to build a bijection from the set of k-element subsets of an n-element set, to the set of n-bit strings with weight k. We never really came up with a formula for the size of the first set, just a method for counting it that involved doing an incorrect count and then dividing off by an error factor to correct it. But we do have a number for the second set, namely Bnk which we can get by repeated application of a recurrence relation. Once we have a bijection, we can conclude that Bnk also counts the first collection.

Here's the mapping. We start with a main set with n elements, labeled a1 through an. Take a k-element set which is some selection of k elements from this n element set. We will turn this into a bit string as follows:

Set up an n-bit string with n blanks in it. Look at the main set and loop through its elements: If ai is in the subset we have, then we put a 1 for the bit in position i. Otherwise we put a 0. Then return the bit string.

Notice that the bit string will have weight k because the process above puts exactly k "1" bits in the string.

Here's an example of the inputs on the left and the outputs on the right of this process in the case where we are looking at 3-element subsets of a 5-element set.

In the second line, it shows that if we take the same set but written in a different order, it produces the same output which is what it should do. That's not a collision but rather illustrating that this mapping is a well defined function.

[talk through bijection]

So what this proves is that the collection of k-element subsets of an n-element set, and the collection of n-bit strings of weight k, are in a very deep sense THE SAME. They have the same number of elements, namely this number Bnk. And importantly they obey the same relationships with each other, especially the recurrence relation we built up in the last video. They are really just two different viewpoints or expressions of the same data structure and we can represent one with the other.

[talk through takeaways]

In the next and final video, we're going to look one more time at this number Bnk and see what it's all about.

## Video 5

Welcome to the fifth and final video on counting complex arrangements. In the last video we made an important discovery -- that the number of k-element subsets of an n-element set is the same as the number of n-bit strings with weight k. In this video we're going to look at a third counting problem that seems totally unrelated to either of these, but see a familiar face in the results. This is going to lead us to define the all-important notion of the binomial coefficient. We'll end this video explaining what this binomial coefficient is and what it tells us.

Let's go back to counting the k-element subsets of an n-element set. We know this number is Bnk, which is the same as the number of n-bit strings with weight k. If n is 5, this table here allows us to actually say what some of these numbers are -- B5,0 and B55 are 1 (which we also stated earlier when talking about bit strings), B5,1 and B54 are both 5, and B52 and B53 are both 10.

Now let's look at something that on the surface appears completely different -- taking the algebraic expression x+y and raising it to the nth power. Here's what we get when n is 0, 1, 2, and 3 once we expand with algebra and simplify. Some things to notice here:

First, the exponents on the individual terms add up to the power we're raising this to. For example in the last line the exponents always add up to 3. Second, each term has a number multiplied to it that we call the "coefficient". For example the coefficient on the x^2y term in the last line is 3. The coefficient o the x^3 term is 1 although we don't write it explicitly.

Watch what happens as we take the powers higher. Let's look at (x+y)^5. when fully expanded it looks like this. Now, check out the coefficients on the terms. The coefficient on the x^5 and y^5 terms are 1 and although we don't usually write these, I've added them so you can see them. The coefficients on the x^4y and xy^4 terms are 5 and the coefficients on the x^2y^3 and 2^3y^2 terms are 10.

Do you notice anything familiar? You should! These coefficients are exactly the number B50, B51, B52, and so on through B55 that we used to count k-element subsets and bit strings of weight k! Can this possibly be a coincidence, that the coefficient on the x^k term of (x+y)^n is Bnk?

Let's see if we can understand this in a special case we haven't seen yet, namely (x+y)^10. Let C10,3 be the coefficient on the x^3 term in this expansion, and in general let Cnk be the coefficient on the x^k term in the expansion of (x+y)^n.

Since the exponents on x and y have to add up to 10, the term is actually x^3 y^7. You can think of this coefficient as the number of x^3y^7's we would have in the final answer. Now (x+y)^10 is just 10 copies of (x+y) multiplied together so one way to expand (x+y)^10 is to first expand (x+y)^9 and then multiply the result by x+y. When you do, you're multiplying this huge thing by x, then by y, then adding the results. Where would one of the x^3y^7 terms come from? Well, it would either come from an x^2y^7 term in (x+y)^9 that was multiplied by x; or it would come from an x^3y^6 term that was multiplied by y. And it can't come from both. So the number of ways to get an x^3y^7 term the first way is C9,2 and the number of ways to get it from the second way is C9,3.

Therefore C10,3 = C9,3 + C92. It's the same recurrence relation that we used to find n-bit strings of weight k. You can wrk out, althoguh we won't prove it here, that this relationship Cnk = Cn-1, k + Cn-1,k-1 holds in general

Furthermore the boundary conditions are the same --- Cnn = 1 because the coefficient on x^n in this expansion is always 1, similarly Cn0 is always 1.

-- So since the coefficients obey the exact same rules as Bnk, and they have the same boundary conditions, they are in fact the same numbers.

So this number Bnk is counting a LOT of different things. It counts the number of k-element subsets of an n element set; the number of n-bit strings with weight k; and it gives us the coefficient on the x^k term in the expansion of (x+y)^n. Because of its centrality and versatility, we're going to give it a special name and notatio.

We are going to now call this number the binomial coefficient, since we just saw that it gives us the coefficient on a term when we raise the binomial x+y to a power. We use this notation here, like a fraction but without the fraction bar, with n on top of k enclosed in parentheses. When we can't type it in nice looking notation like this, for example in Python, we just write binom(n,k).

So the binomial coefficient counts all the items we have already seen in terms of subsets, bit strings, and coefficients. In general -- the binomial coefficient counts the number of ways to select k objects from a group of n objects. That's just another way of referrign to subsets. So sometimes we say that binomial coefficient of n and k is "n choose k"

We also know from our earlier work that n choose k satisfies an important recursive property: namely that n choose k equals n-1 choose k plus n-1 choose k-1. Remember we got this by thinking about n-bit strings of weight k and where they come from. We also know some explicit values of n choose k, namely in the situation where k is n or 0, n choose k is 1.

What we don't have yet is an explicit closed-form formula for n choose k, but that's coming soon, and it'll require us to go back and think about how k-element subsets of an n-element set were formed. For now, what's important isnt' so much how to compute n choose k, but rather these takeaways

First, n choose k is the solution to three different counting problems. It is is the number of ways to form k-element subsets of an n-element set; the number of ways to form n-bit strings with k “1” bits in them; and the coefficient on xkyn-k in (x+y)n.

Second, n choose k obeys a fundamental recurrence relation with boundary conditions. So n choose k is fundamentally recursive in nature and that will lead us not only to some ways to compute this number, but also to some deep mathematical properties that govern how it works.

Finally what's more important than computing this number is how we got it in the first place, through a variety of counting arguments involving correcting an overcounted quantity as we saw early on, in finding a recurrence relation, and in forming a bijection between a set we want to count and one we already counted. Don't lose sight of these conceptual ideas because they are fundamentally important problem-solving approaches that will help you in many situations outside just these few.

Thanks for watching.