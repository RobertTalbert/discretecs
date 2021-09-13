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

We're using this picture of boxes for this module's videos because boxes are a useful way to think about sets. Sets are just containers. Anything can go in them. Even other boxes can go inside them --- or they can be empty! The ordering of what's inside those boxes doesn't really matter. Sets are an extremely simple concept that's wide open for specialized use, and that makes them the perfect mathematical concept to drive a lot of more complicated computer science concepts of packages and containers. 

The objects in a set are often called *elements* of the set. And for notation, sometimes we often use capital letter variables to represent a set, and we usually use curly braces like these to enclose the elements of a set. For example this set T is the truth set of the predicate P(x) we mentioned earlier whose elements are the integers that are 3 mod 5. And here's a set S with just three elements, the letters a, b, and c. And here's a set R that contains four elements that are a mix of numbers, letters, and even other sets. Just like a box you might get when you buy something might contain other boxes, sets can contain other sets. 

Sets are foundational in computer science because every data structure you will ever use in computer science is based on sets. Python lists and dictionaries for example are not sets (because for example in a Python list, you can have elements duplicated and the order matters) but they behave like sets and use a lot of the same language to describe them. Any time we use one of these data structures, for example when we execute a FOR loop, we are working basically with sets. 

Sets in mathematics, unlike data structures in computer science, can be both finite or infinite. For example here is a finite set whose elements are the letters of the English alphabet. And here is an infinite set whose elements are the positive integers. The three dots indicate a pattern that continues. This set, consisting of all even integers, is infinite in both directions. 

As we said, the objects in a set are called "elements" and if we want to say that a particular object is an element of a set we use this notation here, which looks like an e. This for example says that the number 8 is an element of this set. And this notation here, with a slash mark through the "element of" symbol, is saying that the number 11 is not an element of this set. 

We can even have a set with no elements in it at all. This is called the empty set, sometimes called the "null set", and it's denoted by this symbol here which looks like a 0 with a line through it. If the idea of an empty set seems weird, just go back to the box metaphor --- it's not at all weird to think about a box with nothing in it. And that's what the empty set is. 

Some sets are so commonly used in math and computer science that they have their own notation. The set of integers, including 0 and negative integers, often uses this stylized letter Z to denote it. The Z is the first letter in the German word "Zahlen" which means "to count". Another important set is the set of all integers bigger than or equal to 0. This is called the set of *natural numbers* and it uses this stylized "N" to represent it. Finally the set of all real numbers, any number at all that can be located on the number line including integers, fractions, and numbers like pi and square root of 2 that can't be expressed as fractions, is denoted with an R. You can't list those one by one like integers. 

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

Most the sets we saw in the last video were given like lists. We simply listed the elements of the set, and if there was a pattern we saw that helped us express that list then we used dots to represent it. For example, here's the set of all letters in the English alphabet where we assume that the pattern here in the dots is understood. But they are all lists. 

When we express a set by simply listing its elements inside curly braces, this is called writing the set in **roster notation**. The word "roster" in everyday langauge means a list too, usually of people for example the starting eleven of a football team or the members of a college class. And that's the meaning we adopt here for sets. 

Roster notation is simple but it sometimes can hide information about *why* objects are the elements of a set. For example look at this set. There are dots at the end, but what exactly is the pattern here? We'd like this pattern to be more easily understood by someone reading it. In fact the pattern is that every element of this set is a natural number that is equal to 1 mod 6. It might be clearer just to *say* that. In other words, this is the set of natural numbers that are equal to 1 mod 6. Being explicit about the *membership requirements* here makes it a lot easier to understand this set.

Here's an alternative way to express this set that makes the membership requirements clear. Here's how to read this: The curly braces mean "The set of". Before the colon, we have a variable and we are stating the domain of that variable. So this means "the set of all n in the natural numbers". Then the colon means "such that". Then after the colon there is a predicate: n mod 6 is 1. So in all, this notation reads: The set of all natural numbers n, such that n mod 6 is 1. And that's an economical way of writing the set we started with, that specifies the elements of the set not by listing them but by giving the requirements for membership.

This kind of notation is called **set builder notation**. In set builder notation instead of listing the roster of elements, we *build* the set by stating the rules for membership. What we're doing here is starting with an initial set, all natural numbers, and then using a predicate to filter out all but the elements we want to keep. We first list the variable and its domain, then after the colon we list the predicate that filters out elements. 

Here's another example of set-builder notation: The set of all real numbers x such that x**2 = 1. What's this set in roster notation? Well, we start with the entire set of real numbers, which is a huge set. But then we use this predicate to filter out most of them. We are only going to keep the real numbers that make this predicate true. That's just x = 1 and x = -1. So this set in roster notation is the set consisting of 1 and -1. 

And here's another example: The set of all x values from the set {0,1,2,...,6} whose square root is bigger than 2. What's this in roster notation? Start with all the elements of the set {0,1,2,..., 6}. That's 7 numbers. Now apply the predicate to filter out. The numbers that meet the membership requirements, that make the predicate true, are the numbers 5 and 6. So that's our set in roster notation. 

In other words, when we write a set in set-builder notation we are expressing it as the truth set of a predicate, namely the predicate that comes after the colon. What comes before the colon is the initial set before we apply the filter. Then the predicate does the filtering. 

Now you try it. Here's a set in set-builder notation. Just in case you didn't know, a "vowel" in English is one of the letters A, E, I, O, or U. Pause the video and write out this set in roster notation.  

So, the initial, pre-filtered set we use is the set of letters A through M. Notice that's not the entire alphabet. Then we filter out everything except the letters that make the predicate, "x is a vowel", true. That leaves us with A, E, and I. 

Try it going the other direction. Here's a set in roster notation. Choose any of the following that would be correct set-builder notation for the same set. 

So there are two correct answers on this one and here they are. Both of these produce the same list of numbers and both are equally correct, although this one is shorter. The other two are not correct and I'll explain why. This one is not correct because the set we start with, prior to the filtering, is wrong --- this is the set of ALL integers. If we started with that set and filtered out all but the ones that are 3 mod 10 we'd pick up not only all the numbers in the roster set but also negative numbers. So that starting set really matters! It has to be stated, and stated correctly. 

This other one is incorrect because it has the predicate listed first and the set second. This syntax doesn't make sense. If you read it aloud, it says "The set of n mod 10 equal 3 such that n is in the natural numbers." This doesn't make sense in English and also not in math. Correct set builder notation does not list the filtering predicate first --- it can't, because we have to have a set of numbers to filter first. So be mindful of the syntax you use to write in set builder notation. 

Finally, here's a variation on set-builder notation that can be handy for programming purposes. Sometimes we can write a set in terms not of filters but in terms of computations we perform on elements in a set. For example: this set is also considered to be in set-builder notation but it's different. We're not starting with an initial set and filtering things out. Notice the expression before the colon doesn't declare the variable and its domain, like we saw a minutes ago. Instead, it specifies a computation to perform, in this case square, and then gives the variable and its domain. 

What this alternative set-builder notation means, is perform this computation, over all elements of this set. It's still building the set in terms of rules for constructing the elements, so that's why it's considered set-builder notation. But instead of starting with a set and filtering out, we're starting with a computation and stating where to apply it. 

This is basically a FOR loop. It means loop through all the elements in this set after the colon, and perform this process on them. Or in another programming metaphor, instead of using a predicate to filter out elements we are using a computation and mapping the computation over a set. In this case we are mapping the computation of squaring over the entire set of natural numbers, and that gives us this set in roster notation in the end.


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

So far in this module we've learned about sets and the different ways to notate and build sets. We're going to return in this video to the idea of elements and what it means for an object to be an element of a set. This will be very important as we start looking at more advanced operations to perform on sets, so although set membership is a simple idea it's important that we completely master it, regardless of the notation given. The basic question we're going to address in this video, is *how can you tell if an object is an element of a given set?* 

If the set is finite and given in roster notation, it's easy: All the elements are explicitly listed, so you just look to see if the given object is on the list or not. For example in the set {A,B,C,D,E,F}, C is an element of the set and G is not. 

If the set is *infinite* and given in roster notation, then not all elements of the set are listed, nor can they be. So if you are given an object and you're trying to determine if it's in the set, if it's listed then you know that the answer is yes. But if it isn't listed, you have to identify the pattern. For example look at the set S = {10, 21, ...} This is an infinite set and the dots at the end are supposed to indicate a continuing pattern, but what is it? We can clearly see that 21 is an element of the set because it's actually there in the list. But what other numbers are supposed to be included? 

Is the number 65 in this set? If you believe that the pattern is that every number in this set is 11 more than the one before it, then yes, 65 is in the set. But here's another pattern that generates 10 and 21 but 65 is not in the set.  

In fact if you write out the first few numbers in a sequence, you can to to the Online Encyclopedia of Integer Sequences and find a whole host of sets of numbers that contain that list. So there are many, many infinite lists of numbers that fit a pattern. Some include 65 and others don't. Determining whether an object is in an infinite set given in roster notation comes down to whether you and I have some consensus on the pattern indicated in the set. This can be misleading! 

That's a very good reason why set-builder notation is usually preferable in these situations. Set builder notation doesn't leave the pattern up to a guess, it starts with the pattern and builds the set around it. So for example in this set, the set of all natural numbers that are 10 mod 11, we can easily see that 65 belongs to this set because we just use the predicate, n mod 11 equals 10, and apply it to the object in question. 65 mod 11 does equal 10, and so 65 is in this set. 33 mod 11 on the other hand is 0, not 10, so it does not belong to this set. 

It's also easy to see that -1 does not belong to this set because although -1 mod 11 is 10, -1 does not belong to the initial set that we are filtering. So if it's not in the initial set, it's not going to belong to any filtered-out version of that set. 

Basic idea here is that in the "filtering" version of set builder notation, an object will belong to that set if it's in the initial pre-filtered set, and if the object also makes the predicate true, that is, if it meets the membership requirements. If it fails either of those two, the object is not in the set. 

Remember there's another form of set-builder notation where we don't start with a set and filter things out but start with a computation and map it over a set. For example { x**3 : x in {0,1,2,3}} is the set we get by taking the elements in {0,1,2,3} and mapping the cube operation over that set. This is a finite set so it's pretty easy just to generate the roster notation for it and see that the elements are 0, 1, 8, and 27. If this were an infinite set, like {x^3 : x in N} then it's a little harder. Is the number 100 in this set, for instance? Well, then we would have to ask: Does there exist a natural number whose cube is 100? Is there a natural number x I could plug in to the operation I am mapping that gives me 100? So it involves working backwards. In this case, while x^3 = 100 does actually have a solution, the solution is not a natural number and so the answer is that 100 does not belong to the set. 

What about a set that is just a random collection of objects? Like for example this set. [0, 1/2, {1,2,3}, "hello", emoji] What are the elements of this set? It's given in roster notation so we can list them: the numbers 0 and 1/2, the set {1,2,3}, the string "hello", and an emoji. That's *five* elements. It's easy to see that 0 and 1/2 are elements of this set and for example 5 is not. But it also gets a little weird. For example 2 is NOT an element of this set. Although we see the number 2 "in" the set, it's not one of the elements. On the other hand the set {1,2,3} is a element of this set. We can have sets whose elements are other sets --- back to the box metaphor, we can have boxes whose contents are other boxes. The string "hello" is also an element of this set but the substring "he" is not because that substring is not in the list of elements. The takeaway here is that just because we see an object inside a set somewhere does not mean that that object is actually an element of the set. The roster notation of this random looking set tells you exactly what is an element and what is not. 

In this video we dug deeper into the idea of what an "element" of a set looks like and how to determine if an object is an element of a set or not. It can be trickier than it appears at first, but in roster notation we take the list of elements literally to determine membership, and in set-builder notation we use the rules for building the set to guide us. 

In the next video, we're going to use these concepts to discuss the concept of a subset, and to determine whether two sets are equal. 

## 3.4

- Subset: Every element in A is also an element of B
  - Example: {1,2,3} subset {1,2,3,4}, so is {2,4}, so is {1,2,3,4}
  - Example: N subset Z
  - Example: Vowels subset all letters
  - Non example: {1,5} not a subset of {1,2,3,4} 
  - Practice -- pick the subsets
  - Subsets using quantifiers (for all x in A, x in B --- negation is exists x in A x not in B)
  - The empty set is a subset of every set "If x in A, then x in B" 
- Equality: Two sets contain exactly the same elements 
  - Example: {1,2,3} and {3,2,1}
  - Nonexample: 
  - A subset B and B subset A

Now that 


## 3.5 

- Power set: Set consisting of all subsets
  - Example: P({1,2}) 
  - Example: P({a,b,c})
  - Example: P(empty)
- Cardinality: "Size" of a set 
  - If finite: Number of elements 
  - Examples
  - If infinite: It's complicated 2Z, Z
