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

In this video we're going to look at two special kinds of sequences 