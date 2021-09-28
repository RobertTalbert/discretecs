## Module 4 video scripts

## 4.1 

- what is combinatorics 
- Making a single choice from multiple bins (and bins are disjoint)
  - *Additive Principle*
  - Example: choosing shirts of different colors 
- When the bins are not disjoint
  - Choosing shirts that are either red or long-sleeve
  - Double-counts any that are both
  - *Principle of Inclusion/Exclusion* 

Welcome to Module 4! So far in this series of videos, we've learned about how computers represent and work with integers, about the logic behind how those and other computer operations work, and in Module 3 we learned about sets and functions which are the prototypes for computer data structures and programs. All of that materiall lays the groundwork for what the next two moodules are about -- thinking mathematically about underlying problems that show up throughout computer science. 

One of the major categories of those kinds of problems is *counting*. I don't mean simple counting, like you learned when you were a toddler. We mean counting complex arrangements of things. For example: How many 16-bit strings are there that have exactly 10 "1" digits? Or, if your computer password has to be a 12-character string that must contain a number, a capital letter, and a special character, how many passwords are possible? Or, if you are trying to sort a long list of numbers or words, how many steps are needed? 

The particular area of mathematics that deals with counting complex arrangements of things is called **Combinatorics**. 
Combinatorics is central to computer science for many reasons. Maybe the biggest reason is that before we write code in a computer program, we first of all have to understand the underlying algorithm that we are trying to implement in that code. And part of that understanding resides in how many steps or computations are needed. For example, going back to sorting, if we're given a long list of numbers or words to sort, then there are some ways of sorting them that are more efficient than others, because although different methods may give the same results, some take less time than others and scale up better for longer lists than shorter ones. To be able to understand the efficiency of algorithms, we need to be able to count the steps. 

This module is an introduction to the basics of combinatorics, and I hope that as we work through the ideas here you will not only see their usefulness in computer science, but also that you'll be impressed by how cool and beautiful some of these methods for quickly counting complex arrangements are. 

---

Let's begin with a basic problem that we literally encounter every day: Choosing clothes to wear. In my room at home, my shirts are put in a few different places. The long-sleeve dress shirts are on a rack in my closet. Short-sleeve dress shirts are on another rack in the closet. T-Shirts are in a drawer. These are three separate locations for my shirts. Now let's suppose I'm getting ready for work and I need to pick a shirt. If I have 6 long-sleeve shirts, 10 short-sleeve dress shirts, and 20 t-shirts. (I have a lot of t-shirts.) 




## 4.2

- When making a sequence of choices that are independent of each other 
- *Multiplicative principle* 
- Example: Choosing an outfit of shirt, pants, shoes
- Example: License plates 

