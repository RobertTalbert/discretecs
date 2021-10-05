## Module 4 video scripts

## 4.1 

Welcome to Module 4! So far in this series of videos, we've learned about how computers represent and work with integers, about the logic behind how those and other computer operations work, and in Module 3 we learned about sets and functions which are the prototypes for computer data structures and programs. All of that materiall lays the groundwork for what the next two moodules are about -- thinking mathematically about underlying problems that show up throughout computer science. 

One of the major categories of those kinds of problems is *counting*. I don't mean simple counting, like you learned when you were a toddler. We mean counting complex arrangements of things. For example: How many 16-bit strings are there that have exactly 10 "1" digits? Or, if your computer password has to be a 12-character string that must contain a number, a capital letter, and a special character, how many passwords are possible? Or, if you are trying to sort a long list of numbers or words, how many steps are needed? 

The particular area of mathematics that deals with counting complex arrangements of things is called **Combinatorics**. 
Combinatorics is central to computer science for many reasons. Maybe the biggest reason is that before we write code in a computer program, we first of all have to understand the underlying algorithm that we are trying to implement in that code. And part of that understanding resides in how many steps or computations are needed. For example, going back to sorting, if we're given a long list of numbers or words to sort, then there are some ways of sorting them that are more efficient than others, because although different methods may give the same results, some take less time than others and scale up better for longer lists than shorter ones. To be able to understand the efficiency of algorithms, we need to be able to count the steps. 

This module is an introduction to the basics of combinatorics, and I hope that as we work through the ideas here you will not only see their usefulness in computer science, but also that you'll be impressed by how cool and beautiful some of these methods for quickly counting complex arrangements are. 

---

Let's begin with a basic problem that we literally encounter every day: Choosing clothes to wear. In my room at home, my shirts are put in a few different places. The long-sleeve dress shirts are on a rack in my closet. Short-sleeve dress shirts are on another rack in the closet. T-Shirts are in a drawer. These are three separate locations for my shirts. Now let's suppose I'm getting ready for work and I need to pick a shirt. If I have 6 long-sleeve shirts and 10 short-sleeve dress shirts. If those are the only shirts I have, then how many possible ways can I pick a shirt? 

Visualize my shirt arrangements like this, where the shirts live in separate bins. My room doesn't actually look like this, but the drawing here is an abstraction that represents the bins. Importantly: these bins don't overlap. there is no such thing as a shirt that is long-sleeve and short-sleeve at the same time. Well, if I pick one shirt, then there are 6 possible choices from the long-sleeve bin. But I also have 10 possible choices from the short-sleeve bin. So in all, because it's one choice and none of these bins overlap, that's 16 possible shirt choices. That's all my shirts, each one lives in one of these bins, and I am just picking one shirt. 

What we've just illustrated is something called the *Additive Principle of counting*. The Additive Principle says that if an event A can occur in "m" ways and another event B can occur in "n" ways, and those events are disjoint, then the event "A or B" can occur in m+n ways. Let's unpack the language here. First of all an "event" refers to the *outcome* of an action. So in our example "choosing a shirt" is an action, with two possible *events* as outcomes --- event "A" is I picked a long sleeve shirt and event "B" is that I picked a short sleeve shirt. And when we say two events are "disjoint" we mean the same thing as when we say two *sets* are disjoint: They have no intersection, no common elements. Two disjoint events are events that can't both happen at the same time, like picking a shirt that is both long-sleeve and short-sleeve. So in our case, I am making a single choice, that has two disjoint outcomes --- or you can think of it as I am making a single choice from among two disjoint sets or bins. The Additive Principle just says that in these conditions, the total number of choices is just the sum of the possible outcomes over each bin. 

Here's another example: I also have  20 t-shirts in a drawer in my room. Six of those are black, 4 are green, 8 are blue, and 2 are white. None of them are multi-colored. If I don't want to pick a dress shirt (long or short sleeve) today but a t-shirt instead, how many ways are there to pick either a black or a blue t-shirt? Pause the video for a second and work this out. 

The Additive Principle applies here because we are making a single choice that has multiple *disjoint* outcomes. Again I don't actually keep the t-shirts in separate drawers, but you can think of it as separating the different colors into different bins and making one choice from among these bins. And again, note that none of the shirts are multi-colored so the bins are disjoint. The number of ways to pick a black shirt is 6, and the number of ways to pick a blue shirt is 8. So the Additive Principle would say that the total number of ways to pick either black or blue, is 8+6 or 14. 

Now let's make this a little more complicated. Suppose that not only my t-shirts but also my long-sleeve and short-sleeve shirts have colors. Remember there were 16 dress shirts in all. Let's say that 8 of those are white, 5 are pink, and 3 are blue. If I were going to pick a shirt, and it can be from any of the shirts I own --- long-  and short-sleeve, or t-shirt --- then how many ways are there to pick a shirt that is either a t-shirt or is colored blue? 

You might answer by saying there are 20 t-shirts; and for blue shirts, there are 3 blue dress shirts and 8 blue t-shirts for a total of 11. So the Additive Principle would say there are 20+11 = 31 ways to pick a shirt that's either t-shirt or blue. But this is incorrect. There are definitely 20 t-shirts and so 20 ways to pick one. And there are definitely 11 blue shirts and so 11 ways to pick one of those. But there are 8 shirts that are both blue and a t-shirt. So when counting the number of shirts to pick, those get counted twice and so the number 31 is too big. To correct it, I need to subtract off the number of shirts that are both blue and t-shirts because again I counted those twice when I added, so subtracting that number off will result in counting those shirts only once. So the true number is 20, plus 11, *minus 8* for a total of 23 ways to pick a shirt that's either blue or a t-shirt. 

The reason that the Additive Principle didn't apply here directly is because the bins aren't disjoint. The two "events" or outcomes of my choice --- either a t-shirt or a blue-shirt --- can overlap because there are some shirts that are both. So instead of the Additive Principle, we are using a simple version of what's called the *Principle of Inclusion and Exclusion* or PIE. It's phrased in terms of sets and cardinality: The cardinality of a finite set A union with another finite set B, is the cardinality of A plus the cardinality of B minus the cardinality of the intersection. This is just what we saw in the example. "A" was the set of t-shirts and "B" was the set of blue shirts. And A union B is the set of shirts that are either t-shirts or blue. That number, the cardinality, was the number of tshirts, plus the number of blue shirts, minus the number of blue t-shirts because if we just added, then that intersection is counted twice. So subtracting off one intersection corrects the count. 

Notice that if A and B do happen to be disjoint, like in our initial example then the formula here in the PIE gives an empty intersection, which has cardinality zero and that gets us back to the basic Additive Principle. 

We'll be returning to the Principle of Inclusion and Exclusion later in this module to deal with complexities that come when you have three or more sets of objects that you're choosing from, where there are two-way intersections and three-way intersections at work. 

So in this video you learned about the important field of combinatorics and why it matters to computer science, the Additive Principle which tells you how to count the number of ways to make a single choice from a disjoint collection of bins, and the basic Principle of Inclusion and Exclusion which counts the number of ways to do this if you have two bins that aren't disjoint. Next up is a counting principle that goes with these, for how to count multiple choices. 



## 4.2

In the last video we learned about the Additive Principle of counting and the basic Principle of Inclusion and Exclusion. These are guidelines for how to count the number of outcomes of in this case a single choice, made from a collection of sets. Here's a different counting problem that we often encounter, where this principle does NOT apply. 

Go back to choosing clothes to get ready for work. Obviously I don't *just* wear a shirt to work but I also have to choose a pair of pants, and a pair of shoes to wear among other things. Let's suppose I definitely want to wear a long sleeve dress shirt today, and I don't care what color it is -- last time I said I have six of those in my closet. I also need to choose a pair of pants to wear, and I have 5 pairs. And finally I need to choose shoes, and I have three pairs from which to choose. (This of course is ignoring other choices I have to make like socks, underwear, belts, and so on). How many possible outfits can I pick, given that range of choices? 

Before we answer that, notice that the additive principle does NOT apply this time because I am not making *one* choice from a bunch of disjoint bins, but a *sequence* of *three* choices, each of which has its own number of possible outcomes. I am not just picking a single outfit from a collection of outfits. I am picking a shirt, *and then* picking pants, *and then* picking shoes. It's a *sequence of choices*. So this is not the kind of situation where the Additive Principle or the Principle of Inclusion and Exclusion apply. 

Let's visualize my possible choices here. If I pick the shirt first, I have six choices. Now if I pick the pants, I have five choices *for each* of the shirt choices I made. So far that gets me up to 30 possible outfits -- 6 times 5 because for each shirt, I can choose 5 pairs of pants. Finally I choose shoes, and there are three choices of shoes for each of the 30 outfits-in-progress I have already picked. So the total number of outfits should be 30*3 or 90. It's the product of 6, 5, and 3. 

What this tree structure shows you is that given a situation where we are making a sequence of choices, not just a single choice, and each choice has a certain number of outcomes, we get the total number of outcomes by multiplying all the individual number of outcomes together. This is formally expressed in the *Multiplicative Principle* which states that if an event "A" can occur in "m" ways, and for each possible outcome of A there is another event B that can occur in "n" ways, then the event "A and B" can occur in m*n ways. Again, perhaps more simply put, if you are making a *sequence of choices* then the total number of outcomes of that sequence of choices, is the product of the number of outcomes of each individual choice. 

Here's an example that doesn't have to do with clothes. We mentioned passwords earlier, and counting the number of passwords in a computer system is really important because we want to make sure the space of passwords available to users is large enough that we don't run out, and also large enough that it would be impractical for a hacker to get someone's password by brute force --- that is, just running through all possible passwords until something works. Let's say that a university has these rules for passwords: They have to be 12 characters long exactly, and the characters have to be either uppercase letters A-Z, lowercase letters a-z, digits 0-9, or chosen from a collection of 14 non-alphanumeric characters. Under those rules, how many passwords are possible? 

This will use the Multiplicative Principle because choosing a password involves making a sequence of 12 choices --- one choice for each of the characters in the password. We can visualize this by starting with an empty password like this. In each box, I have to make a choice. Since this is a sequence of choices each of which has a certain number of ways of happening, in the end the total number of passwords is the product of the number of ways to fill each blank. OK, so how many ways are there to fill each blank? Well, each blank is filled by picking one thing from this collection and notice *this* is a sub-problem that uses the Additive Principle --- it's the same basic problem as picking a shirt from the different racks in m closet. There are 26 ways to choose a capital letter, 26 ways to choose a lower-case letter, 10 ways to pick a digit, and 14 ways to choose a non-alphanumeric character --- all of these are disjoint, so that's a total of 76 ways to fill each blank. 

Back to the main problem, we've now determined there are 76 ways to make each choice of character, and 12 characters. So the total number of passwords is 76, times 76, times 76.... 12 times, which is 76 to the 12th power. This is an enormous number that's on the order of 10 to the 22.  To put that number in perspective, it's estimate that the number of grains of sand on planet earth is around 10^21, so there are roughly 10 times as many passwords available in this system as there are grains of sand. If a hacker were to try to find a password in this system by brute force by trying one at a time at a rate of 10000 per second, this would take 10^17 seconds, which is roughly equal to the age of the known universe. So this university is safe in terms of passwords.

What if you chose a password in this system but weren't allowed to duplicate any of the characters? That would keep people from choosing passwords like these. Pause the video and see if you can modify the solution to the previous example to solve this problem. 

OK, let's count. There are still 12 blanks to fill, and filling them is a sequence of choices. There are still 76 ways to pick the character in the first blank. But if we can't duplicate, then there are only 75 ways to make the second choice, because the first character we picked is no longer available. then there are only 74 choices for the third blank, 73 for the fourth, and so on until we have 65 choices for the twelfth and final blank. Again this is a sequence of choices and we see the number of possible outcomes for each choice. So the total number of passwords now is the product of all these, which is still a huge number but not as huge as it was before. Which makes sense because we are counting a smaller space of outcomes now. 

So in this video we learned a new counting technique, the Multiplicative Principle, which shows us how to count arrangements when the arrangements are the outcome of a sequence of choices each of which has a certain number of outcomes. We also saw the Additive Principle make an appearance to help determine the number of outcomes of some of those choices, which shows that these principles don't always stand alone but have to work together, and it's our job as intelligent humans to know what tool to use in which situations. Next up is a mini-series of videos where we're going to learn a central tool for counting, and in the process learn some more techniques for counting these complex arrangements. See you there! 

## 4.7

- Number of n-bit strings with weight k = number of k-element subsets of an n-element set 
- Not just happens to be equal but are equal because on some deeper level they are the same thing
- We are taking a collection of n objects and selecting k things out of it
- We will now call this number something: The **binomial coefficient** $\binom{n}{k}$ pronounced "n choose k" because that's what you're doing. 
  - It's not a fraction, it's like a little matrix with the size of the collection on top and the size of the set you're selecting on the bottom. 
  - It replaces the notation |B(n,k)| from earlier videos. 
- Examples: 
  - 5 choose 3 is 10 
  - Special cases are easy: 5 choose 0 is 1, in fact anything choose 0 is 1
  - 5 choose 5 is 1, in fact anything choose itself is 1 
- Fundamental recurrence relation

In this miniseries of videos, you've learned a lot about counting complex arrangements. You've learned some techniques and tricks for counting as well as some pitfalls to avoid when solving a problem about counting. There's one finding from what we've seen that really stands out. 

That's the fact that the number of n-bit strings with weight k, is the same as the number of k-element subsets of an n-element set. The fact that these two numbers work out to be the same is a little mysterious because when you look at the objects that are being counted, they don't look like each other. But the numbers are the same, not by coincidence but because on some deep level, they are just two ways of expressing the same thing. We built a bijection between the two sets to express this. What that bijection expresses is that a string of bits with a number of 1 bits in it, is a way of voting for what elements from a set to include in a subset. 

In other words, these processes -- finding n-bit strings of a given weight and finding subsets of an n-element set of a given size -- are really doing the same thing. They are starting with a collection of distinct objects and then selecting items out of that collection. The number of ways to take a collection of n distinct objects and select k items from that collection is really what we have been computing all this time. 

This idea of selecting k elements from a collection of n elements is such an important type of counting problem that we are going to give it a special name. The binomial coefficient -- notated like this, and pronounced "n choose k" -- is the number of ways to select k elements from a collection of n distinct elements. This is the same thing as the number of k-element subsets of an n-element set; which is also the same as the number of n-bit strings with weight k. 

Please note, this notation is NOT a fraction. It is just notation and there is no algebra manipulation we can do with it. 

For example: 5 choose 3 is 10. We know this because we computed it earlier as the number of 5-bit strings with weight 3. We also know from previous work that there are special cases: 5 choose 0 is 1 because there is only one 5-bit string with weight 0; and there's only one way to select a 0-element subset from a 5-element set. This is true for any value of n --- n choose 0 is 1. Likewise n choose n is 1 because there's only one n-bit string with weight n (the bitstring that's all 1's) and only one way to choose a subset of n elements from an n-element set (which is to choose the entire set itself). 

We also know that there's a recurrence relation that governs these arrangements. We learned that for any n and k, the number of n-bit strings with weight k is equal to the number of n-1 bit strings of weight k, plus the number of n-1 bit strings with weight k-1. Phrased using the binomial coefficient, this would say that n choose k equals n-1 choose k plus n-1 choose k-1. 

We can use these initial conditions and the recurrence relation to compute n choose k using a visual trick. Look at this triangle of binomial coefficients. We know 0 choose 0 is 1 because any natural number choose 0 is 1. We also know 1 choose 0 is 1 and 1 choose 1 is 1. In fact all these numbers along the sides of the triangle are equal to 1. Now look at the highest binomial coefficient we haven't done yet, 2 choose 1. We know this is equal to 1 choose 1 plus 1 choose 0 so that's 2. Now 3 choose 1 is 2 choose 1 plus 2 choose 0, wich is 2+1 or 3. Likewise 3 choose 2 is the sum of 2 choose 2 and 2 choose 1 which is 3. So in this triangle, the recurrence relation that governs how the binomial coefficient works will let us find any binomial coefficient in the middle here as the sum of the two just above it. This triangle is called Pascal's Triangle after the great mathematician Blaise Pascal. 

For example, look at 5 choose 3 again. This is equal to 4 choose 3 plus 4 choose 2. In Pascal's Triangle 4 choose 3 is the sum of the two numbers above it, which is 4; and 4 choose 2 is the sum of the two numbers just above it, which is 6. So 5 choose 3 is 6 + 4 or 10, which verifies what we already know. 

In this video, we introduced the binomial coefficient which is a number that gives the solution to two different counting problems -- the number of n-bit strings with weight k and the number of k-element subsets of an n-element set. And we stated two initial conditions for the binomial coefficient and the underlying recurrence relation for the binomial coefficient. And we learned about Pascal's triangle which is a way to get the value of the binomial coefficient using a visual pattern. In the next video, we'll look more closely at a more general problem of how many ways there are to select items out of a collection when the ordering of the selection makes a difference. 


## 4.8

- Binomial coefficient n choose k = number of ways to select k elements irrespective of ordering out of a set of n objects. 
- More generally how do we count selections and rearrangements? 
- NUmber of ways to rearrange n distinct objects: n! (why) 
  - This is called a permutation. 
  - Example: Arranging people around a dinner table
- How many ways to rearrange (permute) k objects chosen from a collection of n distinct objects? 
  - Example: Select 4 people from a group of 6 and then arrange them around a dinner table
  - First do the selection: C(6,4) But this is just a set of people, the order is not taken into account. So for each selection there are 4! ways to rearrange. 
- In general, a permutation of k objects selected from a collection of n objects is called a k-permutation
- Formula for k-permutation of n elements: n! times C(n,k) which equals n!/(n-k)!. Write this as P(n,k). 
- Example
  - Number of three-character airport codes possible --- select 3 from 26 and put in order. Not 26 choose 3 because that's just a set. We care about order, sp P(26,3). 
  - The formula isn't really necessary just think of filling boxes. 
- Differences between n!, C(n,k), and P(n,k) 

We've just added the binomial coefficient to our list of tools for solving complex counting problems. The binomial coefficient n choose k counts the number of ways to select a group of k things from a larger collection of n things. An important interpretation of this is it's the number of ways to choose a k-element subset of an n-element set. One important thing to remember about sets in general is that the ordering of the elements in a set doesn't matter. But what if we were making a selection from a larger group and the ordering did matter? That's what this video is about. 

Let's start with a simpler situation. Suppose I'm playing a game where I have some letter tiles and I need to rearrange them to spell out as many words as I can. Suppose that I have six of these tiles and they are all different letters. How many arrangements are there? That is, how many ways can I reorder this set of tiles? 

We can solve this pretty easily with the Multiplicative Principle. Imagine that I am going to physically reorder those tiles on an empty rack with six positions. Filling the empty rack is a sequence of choices, so let's count the choices at each stage. There are 6 ways to fill in the first slot, 5 for the second, then 4, then 3, then 2, then 1. So the number of rearrangements is the product of all these, which in this case is 720. More generally if I had "n" tiles and they were all different letters, then the number of rearrangements would be n times n-1 times n-2 times... and so on down to 3 times 2 times 1. This is *n factorial* which we defined in an earlier video, and back when we defined it, we said that it counts the number of arrangements possible of a list of n distinct or different objects. 

Now let's think about the problem we started this video with, counting the number of ways to select a group of objects from a larger group of objects in such a way that the ordering actually is taken into account. Again if the ordering were *not* taken into account, we'd just use the binomial coefficient because that's just forming a subset from a larger set. Here's an example of the kind of problem we're interested in. Suppose I have a class of 12 students and from that group, I need to pick 3 students to be the leadership team of the math club. One student will be the president, another the vice-president, and the other the treasurer. How many ways are there to make this selection? It's not 12 choose 3 because that treats the choice of Alice, bob, chuck the same as the choice of bob, chuck, alice and that's not it. So let's think about this. Imagine the leadership team choices as three spots to fill (because it *is* three spots to fill). Filling those spots is a sequence of choices. There are 12 ways to fill the first spot. Then 11 ways to fill the second, then 10 to fill the last one. So it's 12 * 11 * 10 or 1320 by the Multiplicative Principle. 

We could stop there, and just say that this problem of selecting an *ordered* list of objects from a larger group always works out like this, using the Multiplicative Principle, and that wouldn't be wrong. But let's look a little further. This number 12 * 11 * 10 is not a factorial but it's a piece of a factorial. In fact if you think about it, it's 12! with 9! divided off. So the number of ways to make this selection is 12!/9!. 

This looks a little like the closed formula for the binomial coefficient. 12 choose 3 according to that formula would be 12! over not just 9! but 9! times 3!. So this ordered version of the binomial coefficient is missing the 3! on the bottom. But this makes sense, because we are taking the ordering into account now. The binomial coefficient, when we were defining it, divided off the 3! because choosing items with ordering counted each arrangement as different selections. That was not what we wanted when making sets, so we divided off that 3! to correct the count. But this *is* what we want when we are making ordered selections, so we don't divide it off. 

In general, when you make a selection of k elements from a larger group of n elements and do so in a way that takes the order of the choice into account, this is called a *k-permutation* and this is denoted P(n,k). We just learned that P(n,k) is always equal to n!/(n-k)! For example we saw P(12,3) is 12! over 9!. This is not by magic but because this is just the Mutliplicative Principle at work. 

Here's another example. Suppose I have a set A with 4 elements and a set B with 10 elements. How many functions are possible from A to B, and how many of those are injective? 

To answer the first question, let's make a sequence of choices of where to send each element of A. Although the ordering doesn't matter in a set, let's pretend the set is {1,2,3,4} and go one at a time. Well, with no restriction on the function, there are 10 choices for where to map 1, then 10 for where to map 2, 10 for 3, and 10 for 4. So there are four blanks with 10 choices each so there are 10^4 or 10000 possible functions. That's not a k-permutation or a rearrangement but just the basic multiplicative principle. However if we require injective, then it's got to be less than 10000. Let's count: there are 10 choices for the output of 1, but now only 9 choices for the output of 2, 8 for 3, and 7 for 4. This is 10*9*8*7 which is 5040. You may not even realize it, but this is P(10,4) --- which makes sense in hindsight, because we're basically looking at the codomain of our function and making a selection of 4 things out of it, and putting the selection in order of which point in the domain maps to it. But I think it's actually clearer to *not* view this as a 4-permutation but just count things and use the Multiplicative principle. 

In this video we added two tools to our collection for counting: The factorial function for counting arrangements of items in a set, and the k-permutation for counting the number of *ordered* selections of k items from a group of n items. Next up, we introduce a new but not entirely unrelated counting problem of distributing items to different people. 

## 4.9

- Seen counting problems about selection and arrangements, now one about distribution
- 10 identical cookies, you want to give these to 3 different students. How many ways to do it? 
- Wrong answers: 
  - 3^10 -- Pick the cookie for the first student, then pick for the second, etc. This is wrong because it assumes one cookie per student, but there's no such restriction, could give all 10 to one student and none to anybody else 
  - 10^3 -- For each cookie pick the student to give it to. This lets you give a student more than one cookie, but it overcounts --- all the cookies are identical, so giving first three cookies to alice, the next three to bob, and the next four to chuck is the same as giving the first four to chuck, the next three to bob, and the next three to alice --- but they are counted as different. 
  - 10 choose 3 -- Popular choice, but wrong because 10 choose 3 counts the number of ways of picking 3 things from a collection of 10, and we're not doing that. We're not selecting a subset of the cookies to give away. 
  - Nor is it P(10,3) because this is just 10 choose 8 with the ordering taken into account, and it's still the wrong situation. 
- So this is a new kind of problem where we are *distributing 10 identical items among 8 people*. How to conceptualize this? 
  - For example: Suppose we're giving 5 cookies to alice, 4 to bob, 1 to chuck. 
  - Pretend that the students are line to receive the cookies. Count out 5 cookies to alice, then switch to bob and count out 4, then switch and count out 1. 
  - Represent each cookie with a star and each switching point with a vertical bar. It would produce a little diagram like this: *****|****|*. 
  - What would that diagram look like if we gave 1 to alice, 6 to bob, 3 to chuck? *|******|***
  - What if we gave 8 to alice, none to bob, and 2 to chuck: ********||**
  - So each possible distribution can be represented by one of these diagrams, and each diagram tells you a distribution. In other words there are exactly as many ways to give out the cookies as there are diagrams of this form. "Stars and bars" --- abstracts things away from cookies ad students. This could represent *any* form of distribution. 
- So how many stars/bars diagrams are there in this case? 
  - there are 10 stars and 2 bars since 10 cookies to give and three students, therefore two switchovers. 
  - These diagrams are the same thing as bit strings --- with 10 zeroes and 2 1's. 
  - IOW each diagram is a 12-bit string with weight 2. 
  - The number of such diagrams is 12 choose 2, or 66. 
- Stars and bars method: 
  - For counting number of arrangements of n identical objects to k different locations. 
  - Each distribution consists of n stars and k-1 bars
  - So it's a n+k-1 bit string with weight k-1: n+k-1 choose k-1. 
- What if we wanted each person to get at least one cookie? 
  - Give one cookie out to each student. Now there are 7 left to give away. So... 7 stars, 2 bars. That's a 9-bit string with weight 2, so 9 choose 2 or 36. 

## 4.10

- Basic PIE
- What if you had three sets, with overlaps like this? How many elements in the union? YOu can verify it's 12 here.  
- Sum up the elements in all three: 20. Obviously we overcounted, but how? 
- This counts the elements in each two-way intersection twice, so we need to subtract those out: subtract off A ^ B = 3, A ^ C = 4, B ^ C = 3. But that would get us to 20 - 10 = 10... too small! What happened? 
- The three-way intersection was subtracted out, and now it needs to be added back in. That gets us to 12. 
- PIE for three sets 
- There are versions for four, five, etc. sets 
- Example: Back to giving 10 cookies to 3 students. How many ways to do this so that no student gets more than 4 cookies? 
  - Without the restriction the answer, we saw would be 12 choose 2 (10 stars, 2 bars)
  - Now add up the number of ways that the restriction could be violated and subtract that off. 
  - Number of ways that Alice could get more than 5 OR Bob OR Chuck -- it's a union. 
  - A = set of outcomes where Alice gets more than 4, B = bob, C = Chuck. WE're looking for the |A v B v C|. 
  - |A| = Give alice 5, distribute the remaining 5. That's 5 stars and 2 bars, so 7 choose 2. 
  - |B| also 7 choose 2
  - |C| same. 
  - Now the intersections: A ^ B -- this means Alice and Bob get 5 cookies each. If that's the case there are no more cookies to distribute, so there's only one way to o this. Same for the other two 2-way intersections 
  - Three-way intersection is impossible, so it's empty. 
  - So number of ways to violate the condition is 12 choose 2 minus 3 times 7 choose 2 + 0. 
- The application of the PIE is not obvious! Takes careful human-brain thinking to see that there's a union of three sets involved. 


## 4.11

- Counting problems can be very tricky because it's not always clear exactly what approach you should take -- might be a combination of approaches. And it's tempting to just start applying formulas before you truly understand the problem. Here are some guidelines -- not a foolproof algorithm but guidelines. 
- First use your human brain to study and analyze the problem --- play with examples --- what am I trying to do? 
- Flowchart
  - Making a single selection from a bunch of sets? 
    - Are they disjoint or not?
  - Making a sequence of selections with known outcomes for each? 
  - Selecting a group from a collection? 
    - Does order matter? 
  - Rearranging a list of objects? 
    - Are they all identical? 
  - Distributing identical items to different locations? 
- And realize that the right method may not be any single one of these, but a combo 
- Example: Class of 12 students and I want to split them up into 4 groups of 3. How many different ways to do that? 
  - Closest match in the flowchart is selecting a group from a collection, but it's not a perfect match --- 12 choose 3 is just picking one group. But maybe that helps. Think about the actual process that would take place -- I'd pick the first group, then the second, then the third, then the fourth. So it's a sequence of choices -- multiplicative principle. And each choice has outcomes, how many? 
  - First choice is picking the first group -- 12 choose 3. 
  - Second choice is picking the second group -- 9 choose 3
  - Then 6 choose 3
  - Then finally 3 choose 3. 
  - So first glance --- it's the product of these three binomial coefficients. 
  - But there's one subtle point: We have overcounted because this picks "group 1", then "group 2", etc. But if I put ABC in group 1 and DEF in group 2, that's the same, for me as putting DEF in group 1 and ABC in group 2. So I have overcounted because I am treating the ordering of the groups themselves as being different. That's not the case so I have to divide off by the number of ways to rearrange those groups, which is 4!. 
  - Guidelines: 
    - Use your human brain first
    - Play with examples until you understand the process
    - The flowchart helps, but most counting problems are a combo
    - Beware of overcounting 
