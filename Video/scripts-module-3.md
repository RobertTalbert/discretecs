# Scripts for Module 3 videos

## 3.1 

- What is a set 
    - Already seen we need to talk about collections of items
    - Truth set of a predicate
    - Data structures in CS --- iterating over a range; sorting a list; etc. 
    - Definition of a set : "An unordered collection of objects" 
- Rules of sets
    - Order doesn't matter
    - Items can't be duplicated
    - Otherwise that's it, there's no restrictions on what can go into a set (sets with mixed objects, even sets with other sets inside it)
- Finite and infinite sets 
    - Finite: Example
    - Infinite: Example
- Using curly braces with sets -- "roster" of elements  
- The "element of" notation
- Empty set 
- Famous sets: natural numbers, integers, real numbers


Welcome to Module 3 of this course. We've learned a lot so far about the mathematics that computer science is built on. We've learned how to represent integers in different number bases that make it possible for computers to do math with them. We've also learned about the logic that both humans and computers use to process information. In this new module we're going to study another fundamental building block of computer science, the notion of the SET. 

We've actually already encountered this idea more than once in the previous videos. For example, when we introduced predicates, we talked about their "truth set". This was the collection of all input values that makes a predicate true. For example the truth set of the predicate P(x) which is the statement that x mod 5 is 3, consists of the numbers 3, 8, 13, 18, and so on as well as -2, -7, -12, and so on. We need a handy and precise way to talk about this collection. And that's what a set gives us. 

A set is simply an unordered collection of objects. That's it. There are no restrictions on what can go into a set, and there's no restriction on the order in which we put things in a set. The only restriction really there is on a set is that we cannot duplicate objects. Once an object is in a set, we don't put it in twice. 

The objects in a set are often called *elements* of the set. And for notation, sometimes we often use capital letter variables to represent a set, and we usually use curly braces like these to enclosed the elements of a set. For example this set T is the truth set of the predicate P(x) we mentioned earlier whose elements are the integers that are 3 mod 5. 

Sets are foundational in computer science because every data structure you will ever use in computer science is based on sets. Python lists and dictionaries for example are not sets (because for example in a Python list, you can have elements duplicated and the order matters) but they behave like sets and use a lot of the same language to describe them. Any time we use one of these data structures, for example when we do a FOR loop over the range from 0 through 100 or look through a database or dictionary to find something, we are working basically with sets. 

Sets in mathematics, unlike data structures in computer science, can be both finite or infinite. For example here is a finite set whose elements are the letters of the English alphabet. And here is an infinite set whose elements are the positive integers. The three dots indicate a pattern that continues. This set, consisting of all even integers, is infinite in both directions. 

As we said, the objects in a set are called "elements" and if we want to say that a particular object is an element of a set we use this notation here, which looks like an e. This for example says that the number 8 is an element of this set. And this notation here, with a slash mark through the "element of" symbol, is saying that the number 11 is not an element of this set. 

We can even have a set with no elements in it at all. This is called the empty set, and it's denoted either as just an empty set of braces, or this symbol here which looks like a 0 with a line through it. 

Some sets are so commonly used in math and computer science that they have their own notation. The set of integers, including 0 and negative integers, often uses this stylized letter Z to denote it. The Z is the first letter in the German word "Zahlen" which means "to count". Another important set is the set of all integers bigger than or equal to 0. This is called the set of *natural numbers* and it uses this stylized "N" to represent it. Finally the set of all real numbers, any number at all that can be located on the number line including integers, fractions, and numbers like pi and square root of 2 that can't be expressed as fractions, is denoted with an R. 

So now you know what a set is, what an element of a set is, how to use curly braces to enclose the elements of a set, what a finite and infinite set is, what the empty set is, and notation for the special sets of integers, natural numbers, and real numbers. In the next video we'll look at two different ways to write sets. See you there. 


## 3.2 

- Roster notation
    - Defining what's in a set just by listing the elements 
    - "Roster" notation
    - Example -- finite set (Simple list; all the solutions of an equation)
    - Example -- infinite set with a pattern (Integers; integers that are 3 mod 5)
- Set builder notation
    - Defining what's in a set by "building it" by starting with a set and filtering out elements using a predicate. 
    - Example: Integers that are 3 mod 5
    - Notation
        - Curly braces 
        - Variable and where it comes from
        - Colon ("such that")
        - Predicate that filters out elements 
    - Example: {x in Z : x mod 5 = 3}
    - Example: {x in R : x**2 = 1}
    - Example: {x in {0,1,2} : x < 0} -- empty! 
- Practice: Give a set in roster notation; which set-builder notation is correct
- Practice: Give a set in set-builder notation; which roster notation is correct
- A word about syntax: Putting the predicate first doesn't make sense, example why
