# Module 5 scripts 

## 5.1
 
Welcome to Module 5, the final group of lessons in this course. We've come a long way since first learning about binary and other number bases, then logic, then sets and functions and then counting. In this last module, we will focus in on perhaps the biggest concept of the whole course --- *recursion*. We've seen this idea before, particulary with the binomial coefficient, and in this module we're going to drill deeply into this idea and learn how to work with recursion and how to craft mathematically sound arguments about recursion. But first let's start small. 

Here's an interesting visual pattern that I'd like you to think about. It's a sequence of figures. THe first figure is just a circle. The second is this triangle. Then the third is this triangle. Here's the fourth. Pause the video now, and see if you can guess the pattern and draw the next figure in the list. 

Here's the next one that I had in mind. What's the pattern exactly? It looks like in order to create a new figure, we look back at the previous figure and add a row of dots along the right side of the triangle. So the fifth figure should look like this. 

Now let's count the number of circles in each figure. The first one has 1. The second 3, then 6, then 10, then 15. Can you guess the next one? Can you guess it without drawing a triangle? Try it! 

Did you guess 21? Let's draw the triangle and see: here it is. The visual pattern says we make the new triangle by taking the previous one and adding a row of circles on the right. We already know that the previous figure has 15. Since the previous right side had five circles, the new one should have six. We just need to add the 6 circles here, so that's 21. 

This list of numbers is called a *sequence*. This word refers to any ordered sequence of numbers. The numbers in a sequence are called the *terms* of the sequence. So not a *set* of things, but a *list* with a definite first term, second term, third term, and so on. Sequences occur throughout mathematics and computer science in all kinds of ways, and they are often a key to many applications as well as interesting objects unto themselves. 

We often label the terms of a sequence with a letter and a subscript. For example to denote this sequence 1, 3, 6, 10, 15, 21, and so forth we could use the letter T (for triangle) with subscripts to tell which term in the list we mean, so T_1 is 1, T_2 is 3, T_3 is 6, T_4 is 10, and so on. A number in a subscript is called an *index* and the plural form of index is *indices*. This particular sequence has a special name, the *triangular numbers* because the numbers emerge from this visual pattern you see here. 

Here's another sequence, which this time starts the index at 0: f_0 = 1, f_1 = 1, f_2 = 2, f_3 = 3, f_4 = 5, f_5 = 8, and so on. First of all note that unlike with sets, sequences can and often do have duplicate terms. THe pattern in this sequence is that the first two terms are both 1, and every other term is the sum of the previous two. This one is called the Fibonacci sequence and it plays a big role in mathematics and computer science. 

Sequences can also be spelled out with a formula, like this: The sequence g where g_i is equal to 2**i for each i in the natural numbers. So g_0 = 1, g_1 = 2, g_2 = 4, g_3 = 8, and so on. 

Sequences don't *have* to have any pattern at all. Look at the sequence h given by h_0 = 3, h_1 = 1, h_2 = 4, h_3 = 1, h_4 = 5, h_5 = 9, and so on. The "pattern" here is that h_n is the nth digit of the number pi. There's no formula or pattern here, just a direct mapping from the index to the digit. 

As we just saw, there are two main ways to generate sequences. One is with a closed formula, where you plug in the index and the formula tells you what the sequence term is at that index. For example the sequence g where g_i is equal to 2**i uses a closed formula, and we can quickly generate as many terms in this sequence as we want using Python, or a spreadsheet. Here's another, b_n = 3(1.1)^n and here are the first 10 terms of that sequence. This also shows you that sequences don't have to consist only of integers -- although the indices in a sequence have to be integers because they count the positions of the terms. 

The other major way to generate a sequence gets us to the heart of this module --- we can define sequences recursively. A recursive definition of a sequence computes an term of a sequence in terms of one or more of the previous terms in the sequence. The Fibonacci sequence was recursive because the third, fourth and so on terms of the sequence were the sum of the previous two. We can phrase this using notation by writing f_n = f_{n-1} + f_{n-2}. That relationship is called a *recurrence relation* --- A recurrence relation is a math expression that tells how one term in the sequence relates to previous terms. We also had some starting terms given as part of the definition of the sequence. Those starting terms are called the initial condition. 

A complete recursive definition of a sequence requires both a recurrence relation *and* an initial condition. With both the recurrence relation and the initial condition in place, we can compute any term of the sequence we want. If we wanted to know what f_3 is in the Fibonacci numbers, then it's equal to f_2 + f_1. But what's f_2? Well, that's f_1 + f_0. If I had *only* the recurrence relation, it would just keep pushing me further and further back in the sequence -- in order to actually find the terms in the sequence, I need a starting point. That's called an *initial condition*. In the Fibonacci numbers, the initial conditions are f_0 = 1 and f_1 = 1. Again with those initial conditions *and* the recurrence relation, I can compute any term of the sequence I wanted. 

For example look at a_n = 2 * a_{n-1} with initial condition a_0 = 3. Let's write out the first 5 terms of this sequence. Well, the first one, a_0, is given to you: It's 3. a_1 by the recurrence relation is equal to 2*a_0  and a_0 is 3, so a_1 is 6. Likewise a_2 is 2 times a_1, so that's 12. Pause the video and see if you can get a3 and a4. 

So, a3 is 2*a2 which is 2 times 12 or 24. And a4 is 2 times a3 which is 2 times 24 which is 48. So those are your first five terms: 3, 6, 12, 24, 48. We're doubling each time, which makes sense when you look at the recurrence relation. Notice with this sequence we needed only one initial condition because you only had to go back one step in the sequence to compute a new term. Whereas with the Fibonacci numbers, you had to go back two steps, so we needed two initial conditions. 

Many times we can represent a recursive sequence with a closed formula, and vice versa. It's going to be important to phrase a given sequence in both ways if possible. Let's try this with the triangular numbers we opened with: T_1 = 1, T_2 = 3, T_3 = 6, T_4 = 10, T_5 = 15, T_6 = 21. Can we first come up with a recursive definition for this sequence? It helps to go back to the visual pattern. The first number is 1. The second one we got by adding two circles on the triangle. The third we got by taking the second figure and adding 3 circles onto the triangle. The fourth one we got by taking the third, and adding four circles. I think I'm beginning to understand the pattern: At stage n, I get T_n by dropping back to the previous stage, n-1, and adding n circles. So T_n should be T_{n-1} + n. That's the right recurrence relation, so all I need is the initial condition, which is T_1 = 1. 

Here's a recursive Python function that should generate this sequence. You can see in the second line I have the initial condition coded in, and then in the remaining lines it uses a recursive function call to implement the recurrence relation. Down below I'm going to make a list comprehension with this function to generate terms of the sequence. And when I execute it, I can see that it seems to be generating the right numbers, so I think my recursive definition, both the recurrence relation and the initial conditions, was right. 

What about a closed formula for this? This is harder here. Just looking at the numbers, it's hard to guess --- there's not a totally obvious formula that produces all these. But remember the problem-solving concept of *looking at the problem in different ways*. If I look back at the picture and draw the triangle more like this, I can make a copy of that triangle and rotate it, and attach it to the original triangle to form a rectangle like this. This rectangle has n circles on one side and n+1 on the other. The total number of circles in the rectangle is n times n+1. But the original triangle has exactly half of those circles in it, which is n(n+1)/2. So that's a closed formula. Is it right? Here's a list comprehension that tests this directly, and I can see that it produces the same sequence. Note there's no need for initial conditions with a closed formula -- the formula just directly produces the output. 

In this video you learned what a sequence is, how to represent one recursively using a recurrence relation and initial conditions, and how to represent one as a closed formula. And we've gotten a taste of how to look at a visual pattern and write a recursive definition for it, also how to use the same visual pattern to write a closed formula. Next up we will discuss how to add and multiply terms of a sequence together using a notational trick. 

## 5.2

One of the things we often do with sequences, which we learned about in the last video, is add their elements together or multiply them together. This video is going to demonstrate some mathematical notation for writing these in a compact and efficient way. 

First, realize that when we say "add or multiply the elements of a sequence" we don't necessarily mean ALL the elements. Sequences are infinite, and it's a tricky question as to whether it even makes sense to "Add up infinitely many things". So we always mean what we call a *partial sum* or *partial product* --- starting at a certain point in the sequence (usually the beginning) and adding up or multiplying together the first "n" elements of a sequence. For example, in the sequence given by f(n) = 2**n where n starts at 0, here's the sum of the first 5 terms and the product of the first 5 terms, called the fifth partial sum and fifth partial product respectively. 

To write the sum of a sequence "a" starting at index 1 and going through index n, we write this: The big symbol here is a giant Greek capital letter "sigma", which starts with s to remind you of sums. Read this as "the sum of a_k, from k = 1 to k = n". THis means a1 plus a2 plus a3 plus a4, and so on through an. We can change a lot in this "sigma notation". For example the name of the index is irrelevant. We can also start the summing in a different place, or end it in a different place, or both. 

For example here's the sum of 2^i where i goes from 0 through 4 as we saw above, and here's the sum of 2^k where k goes from 3 to 8. Notice it doesn't really matter what I call the index, as long as it's the same variable used inside the sigma -- it's just a counting variable, like you would use in a FOR loop. Also there's no rule saying the counter must start at 0 or 1. 

In fact, sigma notation is really just a mathematical way of writing a FOR loop with an accumulating variable that we change by adding. For example, this sigma notation adds up the expression n(n+1)/2 from n = 0 to 10. Here's the corresponding FOR loop that does the same thing. And you can also do this with a list comprehension by generating a list of the terms of the sum and then using the `sum` command to add them up. 

We can also multiply sequence elements together, and we use a giant Greek letter pi for that. So this notation means take the elements of sequence "a" from 0 through n, and multiply them together. For example, the product of k^2 from k = 1 to 8 is this number. Notice that if we look at the product of just the variable "k" from 1 to n, this is 1 times 2 times 3 times and so on up through n-1 times n, which is n factorial. 

Just as sigma notation is math shorthand for a FOR loop that accumulates by adding, pi notation is shorthand for a FOR loop that accumulates by multiplying. For example this product is equivalent to this FOR loop. 

In this video you learned the sigma notation shorthand for adding up a finite piece of a sequence and pi notation for multiplying elements of a sequence. THis shorthand helps us think and write about mathematical ideas, as we'll see later. 


## 5.3 

- Two special kinds of sequences where the elements have a special relationship
- Arithmetic
  - The sequence is growing by the same amount each time
  - Example: 3, 5, 7, 9, 11, ... always +2
  - Example: 10, 5, 0, -5, -10, .... always -5
- Geometric
  - The sequence is growing by the same factor each time
  - Example: 3, 6, 12, 24, 48, ... always *2 
  - Example: 5, (grow by *1.1)
- Quiz: Label each as geometric, arithmetic, or neither 
- Example: Summing up powers of 2 --- conjecture?

So far in this module we've learned what a sequence is, how to represent sequences using closed formulas and recursive definitions, and how to use sigma and pi notation to find partial sums and products of sequences. In this video we're going to examine two special types of sequences that have some distinctive behaviors. 

Take a look at this visual pattern and let's see if we can count the number of stars at each stage. Let s_n be the number of stars in the figure at stage n. If we start the indexing at 1, then s_1 is 3, s_2 is 5, and s_3 is 7. I bet you can probably guess what the next several terms of the sequence are going to be, without either a closed formula or a recursive definition. It's a safe guess that s_4 will be 9, then s_5 is 11, and so on because all we are doing to get from one stage to the next is taking the current stage and adding 2. We can say in this case the sequence is increasing by a constant amount --- namely 2 each time I go from one stage to the next. 

A sequence with this behavior, where the terms in the sequence increase by a constant amount added on every time we go from one term to the next, is called an *arithmetic sequence*. So this is an arithmetic sequence, and here are a couple of others. The first sequence on this slide is arithmetic because the terms increase by a constant amount of 10 each time. The second is also considered arithmetic, even though the terms are decreasing, because they are still changing by a constant amount, this time dropping by 3. But this sequence is not arithmetic because the different between the first and second terms is 3 but the differnt ce between the second and third terms is 6. Since that's not the same amount, this is not arithmetic. 

Arithmetic sequence increase (or decrease) like a staircase, always moving up (or down) by the same height each time we take a step. 

Coming up with closed formulas and recursive definitions for arithmetic sequences is fairly easy. To get a closed formula for our star sequence for example, we can use some concepts from basic algebra. If you think of a sequence as a function, which is what we do when we make a closed formula for it, then what you might notice about this function is that it increases at a constant rate, always up 2 for every increase of 1 in the input. Functions that behave like that are called *linear* functions. Linear functions are completely defined by their slope, which is the rate at which they change, and a point on the graph of that function. Well, the slope here is 2 because every increase of 1 in the input produces a change of 2 in the output. And i can look at the data here and see that the point (1,3) is on the graph of this function. So using what we called the point-slope form for the equation of a line back in algebra. we can write y - y1 = m(x-x1), or y - 3 = 2(x-1). That simplifies to y = 2x+1 so the closed formula is s_n = 2n + 1. Using a little Python to check shows me that this seems right. 

A recursive definition is even easier because we don't need any algebra. Just first of all realize that from the visual pattern, to get the figure at stage n we look back one step to n-1 and add 2. So the recurrence relation for this sequence would be s_n = s_{n-1} + 2. Since we go back one step, we need one initial condition, and we can get that from the picture -- s_1 = 3. 

So to determine if a sequence is arithmetic, just look to see if the terms increase or decrease by the same amount each time we move to the next term. Then we can use linear functions to write a closed formula and the pattern itself to write a recursive definition. 

Let's go back to a sequence we saw earlier that was NOT arithmetic. It had terms 3, 6, 12, 24, 48, and so on. This wasn't arithmetic because it didn't increase by the same *amount* each time. But you might have noticed that the terms do have some very noticeable behavior --- they *double* each time. So this the terms of this sequence increase not by the same *amount* but by the same *factor*. 

Here's another sequence whose terms change by the same factor: 1, 1/3, 1/9, 1/27, 1/81, and so on. The differences between the terms aren't always the same so this is not an arithmetic sequence. But there is a common multiple between each term --- each term is obtained by taking the previous one and multiplying by 1/3 (or dividing by 3). So each term is one-third the size of the one that came before it. 

A sequence like these, where the terms change by the same *factor*, is called a *geometric sequence*. You just saw two examples of geometric sequences. Here's another, because the terms are increasing by a factor of 5 each time. Here's one that is not geometric, because the second term is 2 times the first one but the third term is 3 times the second one. Since that's not the same multiple each time, it's not geometric. 

Just as with arithmetic sequences, geometric sequences are fairly simple to represent recursively or in closed form. Look at our first example. Recursively, we just note again that each term is twice the one before it. So the recurrence relation should be a_n = 2*a_{n-1} for n > 1. And for the initial condition, just look at the first term of the sequence to see that a_1 = 3. Likewise the second sequence would have an initial condition b_1 = 1, and for n > 1 we'd have b_n = 1/3 ( b_{n-1}. )

Closed formulas for geometric sequences are a little harder because they aren't linear functions but instead what we call *exponential* functions. The recurrence relation can actually help here: In this sequence, I start with a_1 = 3 and then if I want to go to the nth term, I need to multiply this by 2, n-1 times. So the formula would be a_n = 3(2)^(n-1). We can check to see that this is correct with Python or a spreadsheet. 

Let's review this for a moment. Here are six sequences. Pause the video and label each one as arithmetic, geometric, or neither. 

1, 1, 2, 3, 5, 8, 13, 21, ...
4, 8, 12, 16, 20, ...
1, 3, 6, 10, 15, ...
1, 1.1, 1.21, 1.331, 

Only the second sequence is arithmetic, because the terms are going up by the same amount, 4, each time. Looking at the differences between terms in the other three shows you that those *don't* increase by the same amount each time. 

Likewise I can tell which one is geometric here by looking at the ratios between the terms. Wherever there's a common *ratio*, there's a geometric sequence. The fouth sequence here is the only one that's geometric because the terms are increasing not by a constant amount but by a constant *factor*, being multiplied by 1.1 each time. 

In this video, we learned what arithmetic and geometric sequences are, and methods for expressing both as closed formulas and recursively. Next up, we start a mini-series of videos on taking recurrence relations and figuring out ways to express those as closed formulas. We just saw how this might work in the special cases of arithmetic and geometric sequences, but what if the sequence is neither? Stay tuned. 

## 5.4 

This video is a mini-series in module 5 about *solving recurrence relations*. The purpose of this video is to define what we mean by "solving" a recurrence relation and outlining a method to check a solution to a recurrence relation. 

We've been using recurrence relations frequently throughout the course, starting back as early as the binomial coefficient and recently to describe recursively-defined sequences. As you know, a recurrence relation is an equation that relates one item, typically for us a number in a sequence, to one or more previously-computed numbers of the same type. For example the binomial coefficient n choose k can be related to two smaller, previously-computed binomials coefficients using this recurrence relation. The nth Fibonacci number obeys this recurrence relation which says that for indices above 2, f_n is the sum of the previous two numbers in the sequence. And the triangular numbers which we saw earlier arising from a visual pattern have this recurrence relation. 

Recurrence relations are central to mathematics and computer science because recursion is so central to math and computer science, and recurrence relations are the primary way to express how recursive relations operate. A recurrence relation, together with appropriate initial conditions, give us a framework for computing or constructing these recursively defined objects. 

But we've also seen that sometimes recursion is not a particularly efficient way to actually compute something. For example, computing 24 choose 8 using the recurrence relation for the binomial coefficient would require a tremendous amount of work, and memory if this is being done on a computer. It's much more efficient if we could have a *closed formula* for the thing we are computing. For example we generated a closed formula for the binomial coefficient that makes computing 24 choose 8 very easy. 

So a task of great importance to us, is the following: Given a recurrence relation for a sequence with initial conditions, come up with a closed formula that produces the same initial conditions and all the other elements of the sequence. If we have a closed formula that does this --- produces both the initial conditions and the terms of a sequence that is defined recursively, but does so without recursion --- we say that this closed formula is a *solution* to the recurrence relation. And *solving* a recurrence relation is the process of coming up with a closed formula solution. 

For example, here's a sequence we saw earlier that's defined recursively: s_1 = 3, and for all n > 1, s_n = s_{n-1} + 2. The terms of that sequence are 3, 5, 7, 9, 11, and so on. We saw that the closed formula s(n) = 2n + 1 produces the right initial condition: When n = 1, the closed formula gives s(1) = 2(1) + 1 = 3 and this is the initial condition stated in the sequence. And also, if we look at a table of values for s(n) = 2n + 1, we see we get 3, 5, 7, 9, 11, ... it appears to be producing all the elements of the original sequence, without going through recursion. So that makes s(n) = 2n + 1 a solution to this recurrence relation --- or at least it appears that way. But more on this in a minute. 

Here are some examples of functions that *are not* solutions to recurrence relations. Take the sequence 3, 6, 12, 24, 48, and so on. This is a geometric sequence because the terms are increasing by a common factor, in this case 2, each time. Recursively, we can define the sequence by  a_0 = 3 and for n > 0, a_n = 2a_{n-1} The function f(n) = 2**n sounds like a good choice for a solution because of the doubling behavior. But this isn't a solution since the initial condition isn't met. This time the indexing starts at 0, and f(0) which is 2^0 is 1, not 3 as the sequence says. Likewise g(n) = 3 + 2n has the correct initial condition, g(0) = 3 + 2(0) which is 3, but it doesn't produce the other terms in the sequence correctly as you can see here. 

To show that a function *is not* a solution to a recurrence relation, then, what it takes is showing that at least one of the terms in the sequence --- either the initial condition or some other term further down the list --- is not computed correctly by the function. To show that a function *is* a solution is much trickier. 

Think back to the example we just saw of the sequence 3, 5, 7, 9, 11, and so on. We speculated that the function s(n) = 2n + 1 was a solution because s(1) agreed with s_1, s(2) agreed with s_2, and so on up through the first five terms. Therefore s(n) solves the recurrence relation, right? Well, hold on one second. 

The fact that s(n) produces the first five terms correctly only means that s(n) *appears* to solve the recurrence relation. We don't actually *know* that this is a solution yet, because a real solution would have to produce *all* the terms in the sequence correctly, and we don't know that it does because there are infinitely many terms in the sequence but only five items in my list of sample outputs. We only know from the table that this formula produces the first five terms correctly. That doesn't make it a solution though! 

In fact, here's another formula that also produces the correct initial condition, and it also produces the first five terms correctly. But it does *not* produce the sixth term correctly, so despite initial appearances this formula is not a solution to the recurrence relation. Similarly here's another formula that produces the first six terms correctly but fails to give us the right seventh term. The moral of the story here is a familiar refrain for us: **Examples do not prove that something is always true.** Just because a function might produce the first 5, 6, 7, or million terms of a sequence correctly *does not mean* that it's a solution to the recurrence relation. To prove that a closed formula is a solution to a recurrence relation, we'll need to somehow show that *every* term is produced correctly. 

So how do you take a formula that you *think* is a solution to a recurrence relation and actually prove that it really *is* a solution? It takes more than examples -- it takes mathematical reasoning that does not use examples. 

If the closed formula that we *think* is a solution really *is* one, then no matter which term I am generating with it, the recursion in the recurrence relation will work correctly. For example, that formula s(n) = 2n+1 would say that s(20) = 2(20) + 1 = 41 and s(21) = 2(21) + 1 = 43. So the 21st term is indeed 2 plus the previous term, hence the recursion "works correctly". But again we can't just use isolated examples. So intead of picking out specific values of n to plug and chug, just use the formula itself. Look at the recurrence relation, s_n = s_{n-1} + 2. This is an equation with a left side and a right side. If I replace s_n on the left with the formula s(n) = 2n + 1, I get this. If I replace the s_{n-1} on the right with the formula s(n-1) I have s(n-1) + 2. Well, as a function, if I calculate s(n-1) that's 2(n-1) + 1. So now I have 2(n-1) + 1 + 2. Doing the algebra gives me 2n -2 + 1 + 2 which is 2n+1. Now look: the left side and the right side are equal. 

What this tells me is that replacing the terms of the sequence with the output that the function would produce, gives me a correct



Let's see how this might be done. 

Let's stick with the example of 3, 5, 7, 9, 11 which has the initial condition s_1 = 3 and recurrence relation s_n = s_{n-1} + 2 when n > 1. We suspect and would like to prove that the formula s(n) = 2n + 1 solves this recurrence relation. That means two things have to be true: First, s(n) has to meet the initial condition. In other words s(1), which is what I get when I plug 1 into the formula, has to equal s_1, the actual first term of the sequence. This part is easy to check because s(1) = 2(1) + 1 = 3, and that's what s_1 is supposed to equal. 

Now what we need to do is see if the formula satisfies the *recurrence relation too*. Keep in mind that a recurrence relation is an equation, with two sides. So if I replace s_n on the left side with the formula s(n), and replace s_{n-1} on the right side with the formula s(n-1), if this formula is really a solution then the results should be equal. Let's check and see if that happens. 

Well, on the left side s_n replaced by s(n) is 2n+1. On the right side, s_{n-1} replaced with s(n-1) is 2(n-1) + 1. There's a + 2 here as well because this is the other part of the right side. Doing the algebra here I have 2n - 2 + 1 + 2 and that's 2n+1. Pulling back and looking at the results, I see the left side does equal the right. So what does this show me? It shows me that the formula 2n+1 obeys the rules of the recurrence relation. So if I used that formula to generate the terms of the original sequence, the recursion will always work. Not just for the first five terms but *always*. 