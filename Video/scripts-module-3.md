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
- Practice: Give a set in roster notation; which set-builder notation is correct ( {x in {A,B,C,...,M} : x is a vowel})
- Practice: Give a set in set-builder notation; which roster notation is correct  [1, 7, 13, 19, 25, 31, 37, 43, 49, 55, 61, 67, 73, 79, 85, 91, 97] {x in N : x mod 2 = 1 and x mod 3 = 1}, {}
- A word about syntax: Putting the predicate first doesn't make sense, example why

In the last video we learned a lot of basic ideas about sets. In this video we're going to look at two different important ways to write sets. 

All the sets we saw in the last video were given like lists. We simply listed the elements of the set, and if there was a pattern we saw that helped us express that list then we used dots to represent it. For example, here's the set of all letters in the English alphabet. And here it is again where we assume that the pattern here in the dots is understood. And here's a finite set consisting of the elements -1 and 1. Finally here's an infinite set, the set of all even integers. 

When we express a set by simply listing its elements inside curly braces, this is called writing the set in **roster notation**. The word "roster" in everyday langauge means a list too, usually of people for example the starting eleven of a football team or the members of a college class. And that's the meaning we adopt here for sets. 

Roster notation is simple but it sometimes can hide information about *why* objects are the elements of a set. For example look at this infinite set. There are dots at the end, but what exactly is the pattern here? We'd like this pattern to be more easily understood by someone reading it. In fact the pattern is that every element of this set is an integer that is equal to 3 mod 5. It might be clearer just to *say* that. In other words, this is the set of integers that are equal to 3 mod 5. Being explicit about the *membership requirements* here makes it a lot easier to understand this set.

Here's an alternative way to express this set that makes the membership requirements clear. Here's how to read this: The curly braces mean "The set of". Before the colon, we have a variable and we are stating the domain of that variable. So this means "the set of all x in the integers". Then the colon means "such that". Then after the colon there is a predicate: x mod 5 is 3. So in all, this notation reads: The set of all integers x, such that x mod 5 is 3. And that's an economical way of writing the set we started with, that makes it clear what exactly is in this set, whereas it was a little hard to see when we just listed the roster. 

This kind of notation is called **set builder notation**. In set builder notation instead of listing the roster of elements, we *build* the set by starting with stating a range of variable values, for example all x in the integers, and then using a predicate to filter out all but the elements we want to keep. We first list the variable and its domain, then after the colon we list the predicate that filters out elements. 

Here's another example of set-builder notation: The set of all real numbers x such that x**2 = 1. What's this set in roster notation? Well, we start with the entire set of real numbers, which is a huge set. But then we use this predicate to filter out most of them. We are only going to keep the real numbers that make this predicate true. That's just x = 1 and x = -1. So this set in roster notation is the set consisting of 1 and -1. 

And here's another example: The set of all x values from the set {0,1,2,...,10} whose square root is bigger than 2. What's this in roster notation? Start with all the elements of the set {0,1,2,..., 10}. That's 11 numbers. Now apply the predicate to filter out. The numbers that meet the membership requirements, that make the predicate true, are the numbers 3 through 10. So that's our set in roster notation. 

In other words, when we write a set in set-builder notation we are expressing it as the truth set of a predicate, namely the predicate that comes after the colon. What comes before the colon is the initial set before we apply the filter. Then the predicate does the filtering. 

Now you try it. Here's a set in set-builder notation and some possible roster notation versions of the set. Pause the video and determine which of these sets is the same as the one above. 

This one is the correct answer. The initial, pre-filtered set we use is the set of letters A through M. Notice that's not the entire alphabet. Then we filter out everything except the letters that make the predicate, "x is a vowel", true. That leaves us with A, E, and I. 

Try it going the other direction. Here's a set in roster notation. Choose any of the following that would be correct set-builder notation for the same set. 

So there are two correct answers on this one and here they are. Both of these produce the same list of numbers and both are equally correct, although this one is shorter. The other two are not correct and I'll explain why. This one is not correct because the set we start with, prior to the filtering, is wrong --- this is the set of ALL integers. If we started with that set and filtered out all but the ones that are 1 mod 6 we'd pick up not only all the numbers in the roster set but also negative numbers. So that starting set really matters! It has to be stated, and stated correctly. This other one is incorrect because it has the predicate listed first and the set second. This syntax doesn't make sense. If you read it aloud, it says "The set of x mod 6 equal 1 such that x is in the natural numbers." This doesn't make sense in English and also not in math. Correct set builder notation does not list the filtering predicate first --- it can't, because we have to have a set of numbers to filter first. So be mindful of the syntax you use to write in set builder notation. 

Here's a variation on set-builder notation that can be handy for programming purposes. Sometimes we can write a set in terms not of filters but in terms of computations we perform on elements in a set. For example: this set is also considered to be in set-builder notation but it's different. We're not starting with an initial set and filtering things out, but instead we're stating a computation we're going to perform and then giving the set of elements we'll be using to perform it. In this case we want the set of all squares of elements from the natural numbers. This is basically a FOR loop. It means loop through all the elements in this set after the colon, and perform this process on them. 

Here's a summary of the differences between those two versions of set-builder notation. One kind is a filtering process, so we list the initial set and then the filtering conditions stated as a predicate. The second kind is a looping process, so we list the computation we perform and then the initial set we're looping over. Both are considered set-builder notation because we are literally building a set using some kind of a rule. One rule involves filtering and the other involves looping. 


So in this video you learned about roster notation and set builder notation and the differences between the two, and got some practice switching the expression of a set from one notation to another. Good job! In the next video we'll get a little more practice with this from the standpoint of deciding whether an object belongs to a given set or not. 

## 3.3 

- Reminder of notation for element of/not an element of
- Example: Roster notation 
    - Set is all natural numbers 10 mod 11 
    - Three examples of what's in the set
    - Three examples of what isn't 
- Example: Set builder notation {x in N : x**2 = 100}
- Another example: { x**3 : x in {0,1,2,3}}
- Weird example in roster notation: Mixed elements {1, {1,2}, 3/4} Which elements are in the set and which are not? 

