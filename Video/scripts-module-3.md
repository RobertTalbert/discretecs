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

Now that we've learned about sets and taken a good look at set membership, we can introduce two ways of comparing sets in terms of the elements that they have in common. 

Let's suppose we have a set consisting of the names of all the students enrolled in a discrete math class. The professor for that class might need to send a message out, not to the entire class but just to the first-year students to remind them to go see their advisors. The group of interest is a portion, but not all of the names in the class. Every person in that group is in the class; but we only want to send the message to them, not to everyone. In that case what we are using is called a **subset** of the set of all names of students in the class. This group of first-year students isn't the only subset of the class; we could send messages to all the graduating seniors; or all the students whose first names begin with a "G"; or all the students who were sitting together at a table on Monday. 

Generally speaking, if A and B are sets, then A is a **subset of B** if every element of A is also an element of B. We use this notation, which looks a little like "less than or equal to" except it's rounded, to indicate A is a subset of B. So for example {1,2,3} is a subset of {1,2,3,4}. And so is {2,4}. And even the set {1,2,3,4} itself is a subset of {1,2,3,4} because every element of the set on the left is an element of the set on the right. This means that *every set is a subset of itself*. 

Another example would be the natural numbers, which are a subset of the integers because every natural number is an integer; and the integers are a subset of the real numbers because every integer can be located on the number line. That chain of subset relations means that the natural numbers are a subset of the real numbers too. The real numbers can have finite subsets as well, for example the set {pi, square root of 2} is a 2-element subset of the real numbers. 

On the other hand, the set {1,5} is NOT a subset of {1,2,3,4} because *not every* element in {1,5} is an element of {1, 2, 3, 4}. We can see that 5, although it's an element of {1,5} is not an element of {1,2,3,4}. 

Now you try it. Here's a set {M,A,T,H,E,I,C,S} (the different letters used in the word "mathematics"). Which of the following sets are subsets of this? Take a moment and identify them then come back. 

Here are your correct answers. The first two sets {A}, and {A,M} are subsets because every element in each one is also an element in the set we started with. {A,G} is not, because the letter G is not found in the original set. And the last one is the same as the original set, and we've alread explained that every set is a subset of itself. 

You might have noticed that we can think about subsets using quantifiers, which we learned in Module 2. The definition of subset says that A is a subset of B if every element of A is also an element of B. IN quantifier language that would say that for all x in A, x is in B. This helps us think about what it means for a set NOT to be a subset of somethign else. The negation of for all x in A, x in B is the statement there exists an x in A such that x is not in B. That's why {A,G} was not a subset of {M,A,T,H,E,I,C,S} --- because there exists an element in {A,G} (namely G) that is not in {M,A,T,H,E,I,C,S}. 

Here's another question for you: Is the empty set a subset of {M,A,T,H,E,I,C,S}? Pause the video and think about this, and come back when you've decided yes or no. 

This one takes some careful reasoning. We can think of subsets in terms of conditional statements. The statement "for all x in A, x is in B" can be rephrased as the conditional statement "if x is in A then x is in B." So look at the proposition "the empty set is a subset of {M,A,T,H,E,I,C,S}". As a conditional statement this would say "if x is in the empty set, then x is in {M,A,T,H,E,I,C,S}". Well, the empty set is empty, so the hypothesis of that statement "x is in the empty set" is always false. And when the hypothesis of a conditional statement is false, the conditional statement itself is true. So believe it or not, "if x is in the empty set, then x is in {M,A,T,H,E,I,C,S}" is true, and therefore the empty set is a subset of this set. In fact by this reasoning, the empty is a subset of **every** set. 

In addition to subset relations, we can talk about whether two sets are "equal". Two sets are equal if they contain exactly the same elements, like {1,2,3} and {3,2,1}. These are equal sets because they have the same elements --- the ordering doesn't make them different. But it can be hard to tell sometimes if two sets have the same elements. For example, is the set {1,-1} equal to the set {x in R : x**2 = 1}? One is a finite set and the other is in set-builder notation --- it's hard to tell if the two sets have the same elements just by looking. So we will say that the set A and the set B are equal if A is a subset of B *and* B is a subset of A. 

For example, A = {1,-1} is equal to the set B = {x in R : x**2 = 1}. Here's an explanation. First, A is a subset of B because if x is in A, then x is either 1 or -1. And in each case, x^2  = 1, therefore x passes the filter given by the predicate in the second set, and x is in B. That makes A a subset of B. Likewise if y is in B, then y^2 is 1, and a little algebra shows that y^2 - 1 = 0, so (y+1)(y-1) = 0, which means either y = 1 or y = -1. Therefore the y that was in B, is also in A. That makes B a subset of A. Since they are subsets of each other, they're equal. 

In this video you learned what it means for a set to be a subset of another set, and what it means for two sets to be equal. Those are basic tools for comparing sets. See you in the next video. 



## 3.5 

- Power set: Set consisting of all subsets
  - Example: P({1,2}) 
  - Example: P({a,b,c})
  - Example: P(empty)
- Cardinality: "Size" of a set 
  - If finite: Number of elements 
  - Examples
  - If infinite: It's complicated 2Z, Z

This video is going to touch on two quick concepts related to sets that will pave the way for some of the other work we will do with them in future videos. Here's the first concept. 

In the last video we talked at length about subsets of a set. For example we saw that {1,2,3} is a subset of {1,2,3,4} and so is {2,4}, so is {1,2,3,4} itself, and so is even the empty set. It might make you wonder, what are all the subsets of {1,2,3,4} and how many are there? It's sometimes useful to think about all the possible subsets of a given set, so let's do that with this example. 

Well, the empty set is a subset of all sets. There are four one-element subsets of {1,2,3,4} and here those are. The number of 2-element subsets takes a little more work to enumerate but you would have {1,2}, {1,3} and {1,4}, then {2,3} and {2,4} --- notice {2,1} is the same as {1,2} and {2,2} is the same as just {2}, and since those are already listed we leave them out. We'd also have {3,4}, and that's all the two-element subsets -- six in all.  Then for the three-element subsets we have {1,2,3}, {1,2,4}, {1,3,4}, ad {2,3,4}. Then finally we have {1,2,3,4} itself. That's all of them and that's 16 in all. 

We mentioned earlier too that sets can contain elements that are also sets, just like boxes can contain other boxes. If we take all 16 of those sets and put them into a set like so, we have formed the set of all subsets of {1,2,3,4}. This is a construction known as the **power set** of {1,2,3,4}. The power set of a set A, is a set whose elements are all the subsets of A. And we use a script or boldface P around the set to denote it. 

For example, the power set of {a,b} is the set, whose elements are the subsets of {a,b}. There are four of those: the empty set, the one-element sets {a} and {b}, and the set {a,b}. YOu try it with the three-element set {x,y,z}. What is the power set of this set? 

You should find there are eight subsets for this set. The empty set is one, then these three one-element sets, then these three two-element sets, then finally the full set itself. The power set is the set containing all of those. 

We can form the power set of any set at all, although we may not be able to list all the elements. For example the power set of the natural numbers contains all possible subsets of the natural numbers, and that's an infinite set. What about the power set of the empty set? Well, there is only one subset of the empty set, and that's the empty set itself. So the power set of the empty set, is the set, containing the empty set. 

We seem to be talking a lot about *size* here, in terms of how many elements a set has. The term **cardinality** refers to how many elements are in a set.  We put absolute value signs around the set to indicate its cardinality The cardinality of {x,y,z} for example is 3. The cardinality of the power set of {x,y,z} is 8. The cardinality of the empty set is 0 because there are no elements at all in the empty set. 

If the set is finite, its cardinality is just the number of elements it has. If the set is infinite, it gets complicated. For now we will just say that an infinite set has infinite cardinality. But again -- it's complicated. 

TO see why it's complicated, look at the set of natural numbers and the set of even natural numbers. IT seems like the set of natural numbers should be twice as big as the set of even natural numbers. But as you can see, we can put the even natural numbers in one-to-one correspondence with the full set of natural numbers, so if you look at it that way, these two sets have the same number of elements. So with infinite sets, we need to be more careful about talking about cardinality. For now, we'll oversimplify things and just say that infinite sets have infinite cardinality. 

So in this video you learn about the power set of a set, which is the set whose elements are all the possible subsets of the given set -- and about the cardinality of a set, which roughly refers to the number of elements it has, although things get weird when the set is infinite. Next up, we'll be learning about forming new sets from old ones by using set operations. 

## 3.6 

- Intersection
- Union
- Difference
- Complement
- Symmetric difference 

In both math and computer science, whenever we learn about a structure, it's useful to then learn how to build new structures out of it. We're going to do that now by looking at five operations we can perform on sets that will create new, related sets that can be used for various purposes. 

As a running example throughout this video, suppose you're in a discrete math class. Let's let U be the set of all students in the class. Also let C be the set of all computer science majors in your class, and F is the set of all first-year students in the class. So C and F are both subsets of U but we don't necessarily know how C and F relate to each other. 

The instructor of the class wants to let all the first-year computer science majors know about the Computer Science club. So she needs to generate a list of all students in the class who are both computer science students and first year students --- all students who are both in the set C and in the set F. This is called the *intersection* of those two sets. In general, the intersection of any two sets A and B is a new set whose elements are those that are elements of A and elements of B. We use an upside-down U symbol like this to represent the intersection of A and B --- it should remind you of the upside down V we use for "and" when studying logic. We'd express the intersection of A and B like this in set-builder notation. In our class, C intersect F would contain these three students since they are in both sets at the same time. 

Later on, the instructor gets a message from the university asking her to remind students about signing up for classes. She decides she needs to especially contact any student that is either a first-year student or a computer science major, since first-year students may need to be reminded about signing up for classes and computer science majors have a complicated set of courses to finish. So this time, she needs students who are either first year or computer science majors, or both. This is called the *union* of those two sets. In general the union of any two sets A and B is a new set whose elements are those that are either elements of A or elements of B or both. We use a U shaped symbol to denote the union, and here's what it would look like in set-builder notation. For our class, C union F would contain these eight students since they are in either C or F, or in some cases both. 

Not all the students in the discrete math class are computer science majors, and the instructor would like to send the first-year students who are not majoring in computer science some information about the computer science major to see if they are interested. Now the instructor needs the students who are first-year students but who are not computer science majors. The set of results is called the *difference* of the two sets. In general, if A and B are sets, then the difference of A and B is written either with a minus sign A-B, or with a backward slash A \ B and it's pronounced "A minus B" either way. This is the set whose elements are those that *are* elements of A *and not* elements of B. In our class, we're looking for students who are first-year students but not computer science majors, so that's F minus C which in this case has three students in it. Notice that unlike with intersection and union, the ordering matters here. C \ F is different -- this would be the set of students who are computer science majors and not first year students. 

The instructor of the discrete math class decides it would be good to send that information about being a computer science major to *all* students who are not currently majoring in computer science, not just the first year students. So she needs a list of all students who are *not* majoring in computer science regardless of what year they are in. This is called the *complement* of a set. In general, if A is a set, then its complement is a new set whose elements are those that are *not* in A. We use a bar over the name of the set to denote its complement. In our class, the instructor needs the complement of C, the set of all students not majoring in computer science. That's this set of seven students. Notice that in order to find the complement, we needed to know what the entire set of students in the class was. We called that set U, and the set of all elements we are considering in any given situation is sometimes called the *universe*. So notice that the complement of A is just the difference U minus A; and the difference A minus B is the intersection of A and the complement of B -- the set of all elements that are in A and not in B. 

Back to our discrete math class, it turns out that the computer science department has its own message to send out about class registration to all first-year computer science majors. So the instructor of the class didn't need to send the information to those students. She needed to send it to students who are either computer science majors, or first-year students, *but not both*. The set of student in that situation is called the *symmetric difference* of two sets. In general, if A and B are two sets then the symmetric difference of the two, which we notate with a triangle symbol, is the union of A and B minus the intersection of A and B --- the set whose elements are either in A or B, but not in both. In our class, the instructor would need the symmetric difference of C and F, which would be this set. 

Now you try it. Let A be the set {1,2,3,4,5}, B the set {3,4,5,6,7}, and C the set {1,2,8}. Assume that the universe in this case is the set {1,2,..., 10}. Pause the video and write out the following sets in roster notation: A intersect B, B intersect C, A union C, A minus B, A symmetric difference B, and finally A intersect the complement of B union C. 

So A intersect B is the set of elements in both A and B, and that's the set {3,4,5}. 
B intersect C is the set of elements in both B and C but there are no elements in both, so that set is empty. Whenever two sets have an empty intersection, we say those sets are disjoint. 
A union C is the set of elements in either A or C or both, so that's {1,2,3,4,5,8}. A set union is a little like merging the two sets and removing duplicates. 
A minus B is the set of elements that are in A but not in B. Well, A consists of 1, 2, 3, 4, 5 and 3,4,5 are in B, so we throw our 3, 4, 5 and are left with {1,2}. A minus B is like a filtering process where we start with A and filter out the things that are in B. 

A symmetric difference B is A union B, which is {1,2,3,4,5,6,7}, minus A intersect B which is 3,4,5. Filtering out those three elements leaves us with {1,2,6,7}. 

Now for the last one, we build the set piece by piece using order of operations. B union C is the set {1,2,3,4,5,6,7,8}. The complement of this is everything in the universe set that isn't in B union C, so that's {9,10}. Then A intersect with this set is empty, since those two sets have no elements in common. 

In this video we introduced five set operations: intersection, union, difference, complement, and symmetric difference and saw how these can be used to combine sets in different ways for different purposes. In the next video we'll discuss a sixth operation called the cartesian product of two sets that produces a very different kind of result. 



## 3.7 

- Ordered pairs in algebra 
- Ordered pairs in computer science and information management -- names/G numbers
- Cartesian product 
  - Definition
  - Example: R X R
  - Example: Students x G-numbers
  - Example: {1,2,3} x {a,b}
  - You try it 
- Order matters because they are ORDERED pairs 

In the last video we saw a number of operations we can perform on sets to produce new sets that fit different kinds of real situations. In this video we're going to introduce another set operation that's similar to these, but it's different and needs a little more explanation.

Let's go back to our fictitious discrete math class. Suppose the class has met a total of 10 times and instructor wants to look at attedance at class meetings. So she creates a spreadsheet with the names of students in one column and the number of days they have attended in the other. This pairs off each student with a number. We can think of these pairs as an ordered pair, like this. Remember that U was the set of all students in the class. And the numbers here could range between 0 and 10 since the class has met 10 times. Let's let A be the set 0, 1, 2, and so on through 10. The set of all possible pairs that the instructor could create, with students in the first slot of each pair and integers 0 through 10 in the second slot, created is called the Cartesian product of U and A. 

In general given any two sets A and B, the Cartesian product of A and B is the set of all ordered pairs that have the first item in the pair coming from A and the second item coming from B. We use a cross, like you might see in primary school to denote multiplication of two numbers, as the notation. 

For example, look at the set {1,2,3} product with the set {a,b}. This is the set of all ordered pairs whose first "coordinate" is in the set 1,2,3 and whose second coordinate is in the set a,b. There are six such pairs and here they are: There are two pairs for each of the three elements of the set {1,2,3} -- (1,a) and (1,b), then (2,a) and (2,b), and finally (3,a) and (3,b). 

In our classroom example, the product of U and {1,2,...,10} is the set of all possible pairings of students and attendance. So there are 11 possible pairs for each student, making this a pretty large set. The pairs that are in the instructors spreadsheet would be a subset of the entire product but not equal to it. 

Now you try it. Write out the set A times B, where A is {x,y} and B is the set {1,2,3,4}. 

You should find there are eight pairs in this product, and here they are --- four pairs for each element of A. Or another way to think about it, you have two pairs for each element of B. 

Notice that unlike in multiplication of real numbers, the order of A and B in A times B matters. In this exmaple you just worked, B times A would be this set -- it's still eight pairs and the ordering of the coordinates is reversed. But these are *ordered* pairs --- (x,1) is not considered to be the same thing as (1,x) so these two sets have the same *number* of elements, but the elements themselves are not the same. 

You've actualy worked with Cartesian products before because you've worked with ordered pairs before. Back in your early algebra classes, you learned how to plot points in a two-dimensional xy-plane and then graph functions using this process. Each point is a pair of numbers, like (4,3) or (-2,-3). So the xy-plane which consists of **all** those points, is the set R times R where R is the set of all real numbers. This is the set consisting of all possible pairs with real numbers in each coordinate. 

So you've learned what the Cartesian product is, and how to find the Cartesian product of simple sets. In our next video, we'll be shifting gears to focus on the idea of a *function* which, as we just mentioned, is a way of mapping elements of one set onto the elements of another. 


## 3.8

- The idea of assigning values of output to values of input --- the core idea of a computer program
  - Integer -> another integer
  - String -> Integer
  - Two strings -> Boolean
  - **Core concept:** A process that takes input from a set, then assigns it to output in a different set 
- Function
  - A rule that assigns input from one set (the *domain*) to elements of another set (the *codomain*) in such a way that every input is assigned to exactly one output. 
  - Example from Python 
  - Example from math 
- What the last part means 
  - Every input gets assigned to something 
  - No input gets assigned to more than one thing
  - Examples from Python 
- How we notate functions
  - Often lower-case letters to denote the rule
  - $f: A --> B$ means f is the function, the domain is A, and the codomain is B
  - f(x) means the output that we get when x is the input
- Examples
  - f: R -> R by f(x) = x + 1
  - g: {1,2,3} -> {x,y,z} given by a diagram
  - The same g given by a matrix 
  - Python predicate , P: N -> {True, False} (All predicates are just functions from a set into {True, False})
- Non examples
  - Diagram with one thing mapping to two 
  - Diagram with an input not mapping anywhere
  - f: N -> N, f(n) = n/2
- Domain = Set of inputs; codomain = Set that contains outputs, think of it as a data type 
- Range = Set of all actual outputs 
  - Example: diagram, two functions same two sets but one has a different range 


We've learned a lot about sets and how to work with them. One of the purposes of sets is that they are basic data structures -- in fact every data structure you learn about in computer science comes from the idea of a set. But we have data structures not just for holding information but for doing something with it, and that's what we're going to dive into next. 

At the core of computer science is the idea of taking objects from one data structure, and then assigning them to objects in another data structure. For example this short Python program takes natural numbers and assigns them to another integer using a mathematical formula.  This one takes natural numbers and assigns them to strings by duplicating the string "foo" a number of times equal to the input. This Python program takes strings on the other hand and turns them into natural numbers by computing their lengths. This one takes two strings, and assigns a Boolean true or false value according to whether the first string is shorter than the second. 

The idea that threads all of those programs is that they all take input from one set, and then assign it to output in another set. In Python we call these programs *functions*, and in fact that term is taken from a bigger and older term from mathematics that we'll use now as a formal definition. 

Let's define a **function** to be a rule that assigns elements from one set, which we call the *domain* of the function, to elements of another set (the *codomain*) in such a way that every input is assigned to exactly one output.  All of the Python functions we just saw fit this definition. In the first one, the domain and codomain are both the set of natural numbers, and the rule is the mathematical function you see in the code. In the second, the domain is the set of natural numbers and the codomain is the set of all strings. In the third, the domain is the set of strings and the codomain is the set of natural numbers. And in the last one, the domain is the set of pairs of strings and the codomain is the two-element set {True, False}. 

---

Here's a function that isn't in code. The function is called "f". The domain is the set of real numbers, and the codomain is also the set of real numbers. There are many, many possible functions between these two sets so I need to tell you what the particular rule is. The rule I have in mind is that given an input x, we square it and add 1, and that's the output. Here are some examples of this function in use. 

This should remind you of predicates. In fact every predicate is a function, whose codomain is always the set {True, False}. For example earlier we looked at the example of the predicate Q(x) whose domain is the set of integers, and each integer is assigned a true/false value based on the outcome of the statement x % 3 = 0. This is a function from Z to {True, False} and the output is determined by finding x % 3 and seeing if it's equal to 0. 

There's a number of different ways to represent functions, and they're all good as long as we know exactly how to assign elements from the domain to elements of the codomain. Functions given as mathematical formulas do this by telling you how to compute the output. Predicates do this by giving you the logical statement to evaluate. But we can do it in other ways as well. Especially useful if the domain and codomain are finite sets is a simple diagram, which is like a spreadsheet that pairs off the inputs with the outputs. This diagram for example gives a function f from the set {1,2,3,4} to the set {x,y,z,t} such that f(1) = y, f(2) = x, f(3) = z, and f(4) also = z.  Sometimes it's also given as a kind of matrix with big parentheses on the sides. 

In Python basic programs are called "functions" but we can also represent generic functions using dictionaries. The dictionary data structure in Python is set exactly for this kind of purpose, to make an explicit connection between elements of one set and elements of another. Here for example is the function we saw a minute ago, written in dictionary form. We can even use function-like syntax, using square braces instead of parenthesis, to see that f[1] = y, f[2] = x, and so on. 

There's two nuances about functions we need to discuss before moving on. 

First, the definition of a function is that it is a rule that assigns elements in the domain to elements in the codomain in such a way that every input is assigned to exactly one output. What does that phrase at the end mean? Every input is assigned to exactly one output -- this means two things. First it means every input is actually assigned to at least one output --- there can be no input that simply doesn't get assigned, or gets assigned to something that isn't in the codomain. For example, look at the mapping f from the natural numbers to the natural numbers defined by the mathematical formula f(n) = n/2. This looks like a function, but it's not, because if you plug in n = 5, you get 5/2, but that's not in the natural numbers. So this is not a function from N to N because if we define it this way with this particular codomain, the outputs must be natural numbers. If you tweaked the definition to say the codomain is R, the real numbers, then this *is* a function. Or, look at this mapping given by a diagram. This isn't a function because the number 2 has no output at all. 

So every input must actually have an output that belongs to the codomain, but the definition also says that an input maps to *exactly one* output --- it cannot map to two or more outputs. For example, look at this diagram --- that's got the same domain and codomain as before, and it's still not a function because this time the number 1 maps to two different outputs. Just like a computer program, we don't want a situation where one user input leads to two different results. 

The second item is also about the codomain. The domain is the set of all the allowable inputs of a function, but while the codomain has to *contain* all the outputs, some elements in the codomain may not actually *be* outputs. For example look at the function f from the real numbers to the real numbers given by the formula f(x) = x^2 + 1, which we looked at earlier. The codomain is the set of all real numbers, but not every real number will actually be an output of this function. For example 0 is not an output of this function, because x^2 + 1 is always a positive number no matter what the input. And in this finite example, the set {x,y,z,t} was the codomain but not every element of the codomain has something mapping to it. So we'll define the **range** of a function to be the set of all *actual outputs* of the function. That is, in set-builder notation, the range of f: A->B is the set of all points b in the codomain of f, such that f(a) = b for some a in the domain. Again it is the set of all points in the codomain that are actually output by the function. In some cases the range and codomain are the same set; in other cases the range is a subset but not equal. 

The codomain of a function is like the *data type* of the outputs. For example that function f:R -> R given by f(x) = x^2 + 1 has outputs whose data type is real numbers. But not all real numbers are actually produced; the set of real numbers that actually gets produced is the range. In this case if you're wondering, that's the set of all real numbers greater than or equal to 1. Likewise the range of this function is {x,y,z} because those are the actual outputs of this function; t is never output by anything. 

So this video was a deep dive on the central idea of the function. You've learned what a function is, about its domain, codomain and range, how we represent and notate functions, and how a mapping between two sets can fail to be a function. IN the next three videos we'll briefly look at three properties of functions that refer to how it maps points from the domain to the codomain. 


## 3.9

We introduced functions in our last video, which we can think of as a generalization of the idea of a computer program. Functions take in input from one set called the *domain* of the function, and map it to output in another set we call the *codomain* according to some kind of rule. That rule might be a formula, a code snippet, a set of verbal instructions, or a picture. But the mapping takes place so that every element in the domain maps to exactly one element in the codomain. 

So a valid function never takes an input and sends it to two different outputs. But what happens if a mapping does the opposite -- sending two different inputs to the same output? Is this allowed? What happens if it is? That's the subject of this video. 

First, let's be clear that functions *can* send two different inputs to the same output. In fact many functions we use in real life do this. Consider a function from the set of all students at your university to the set of all days of the year, which maps a person to their birthday. This is a valid function because every person has a birthday, and no person has two birthdays. So the function does produce an output for each person, and it doesn't "split" inputs by giving a person two birthdays. But two different people could map to the same birthday, and this doesn't make the function invalid. You might say that this function has "collisions" --- two inputs from the domain that collide in the codomain. 

But not all functions have collisions, for example a similar function that maps students at your university to the set of all student ID numbers at your university. If this function had a collision, it would mean two people have the same student ID, and generally speaking that's bad. 

We'd like to distinguish valid functions that have collisions from those that don't because the existence of collisions has real-world implications, as we just saw. So we are going to say that a function where two different inputs never map to the same output, is **injective**. More formally, we say a function f from A to B is injective if, for all elements x1 and x2 in the domain, if x1 does not equal x2, then f(x1) also does not equal f(x2). This is the formal way of saying there are no collisions -- a pair of distinct inputs must always map to a pair of distinct outputs. 

Let's look at some examples and non-examples. 

The ID number function is, we hope, injective again because if you take any two different people and "plug them in" to this function, you should get two different ID numbers. 

This function given as a table from {1,2,3,4} to the set {x,y,z,t} is injective because you can look at the table and see that no two different elements in {1,2,3,4} map to the same point in {x,y,z,t}. 

The function f from the natural numbers to the natural numbers given by the formula f(n) = 2n is injective. Why is this? This time we can't use a table because both the domain and codomain are infinite. So let's give a rigorous explanation using the definition of "injective". That definition remember says f is inejective if for all x1 and x2 in the domain, if x1 does not equal x2 then f(x1) does not equal f(x2). Note that conditional statement. I'm going to use the contrapositive of that statement, which remember is logically equivalent to the original. The contrapositive would say that for all x1, x2 in the domain, if f(x1) *equals* f(x2), then x1 *equals* x2. So let's pick any two natural numbers from the domain and call then a and b, and suppose f(a) = f(b). Apply the function on both sides to get 2a = 2b. Well, if that equation is true, we can divide off the 2's to get a = b. That shows that the function is injective the definition has been satisfied for a random choice of a and b --- if their outputs are the same, then the inputs must be the same. 

So, proving that a function is injective, is a matter of showing that *all* pairs of different elements in the domain map to different elements in the codomain. Examples won't do --- this is a universal statement that has to be shown for all pairs of points in the domain. 

Now here are some non-examples. The birthday function is a good nonexample because in a group the size of your university's student body, it's nearly 100% likely that you can find two people with the same birthday. 

Here's another function from {1,2,3,4} to {x,y,z,t} that you can see is non-injective because there is a collision --- 1 and 2 map to the same element in the codomain. 

And the mathematical function f from Z to Z given by f(n) = n^2 is not injective because f(-1) and f(1) both map to 1. So, showing a function *is not* injective is a matter of finding an example -- an example of two distinct elements in the domain that map to the same element of the codomain. 

However notice if we used a different domain, for example f mapping the natural numbers to the integers, this function *would* be injective. Because if N were the domain and not Z, suppose I had two natural numbers a and b such that f(a) = f(b). Then applying the function gives me a^2 = b^2, which gives a^2 - b^2 = 0, which means (a+b)(a-b) = 0. This means either a+b = 0 or a - b = 0. The first equation gives a = -b. That's only possible if both a and b are both 0 themselves because a and b are natural numbers and not just any integer. And the second equation says a = b. In either case, a and b are equal to each other so the function is injective if you use N as the domain. 

In this video you've learned about injective functions, what the definition is and also the contrapositive of the definition, seen a bunch of examples of injective functions and some that are not injective, and seen examples of how to argue that a function is injective and how to argue that it's not injective. In the next video, we'll look at a similar property for functions involving situations where the codomain and range are equal. 

## 3.10

In the last video, we moved from discussion what a function is, to how it behaves. We introduced the idea of an injective function to describe functions that map elements so that there are no "collisions". This video is going to introduce a similar idea, focusing on the codomain. 

Earlier we distinguished between the *codomain* of a function and its *range*. The codomain is a set that *contains* the outputs of a function while the range is the set of *actual* outputs of a function. As this diagram shows, sometimes the range of a function is smaller than, and not equal to, its codomain. You can think of the codomain of a function as the *data type* of its outputs while the range is list of actual outputs. The outputs must belong to the codomain, they must be of a data type belonging to this set, but not every point in the codomain may actually get output. 

But sometimes the range and codomain are equal, like you see in this diagram. Here, every element of the codomain that *can* be "hit" by the mapping, *is* hit by the mapping. This function is not injective because you can see a collision here. But it does have the property that the codomain and range are equal sets. 

These functions where the codomain and range are equal sets, we will call **surjective**. More formally, if f: A -> B is a function (note B is the codomain), then f is surjective if the following double-quantified statement is true: For every point b in the codomain, there exist a point a in the domain such that f(a) = b. 

So this function from the previous slide is surjective, because if you loop through each of the four points in the codomain, you can always find at least one (sometimes more than one) point in the domain that maps to it. But the function from two slides ago, is *not* surjective, because not all of the points in the codomain have at least one element of the domain mapping to them. As you can see these two points have no elements mapping to them. 

Here are some more examples of functions that are surjective and some that are not surjective. 

Here are two functions, one called f and the other g, both from the set {1,2,3,4} to the set {x,y,z,t}. The first one f is surjective because again, every point in the codomain has at least one point in the domain mapping to it. The entire codomain is "covered" by this function. In fact that's where the word "surjective" comes from, it uses the French word "sur" which means "on top of". So a surjective function puts outputs "on top of" the entire codomain and doesn't leave any out. The function on the right on the other hand uses the same domain and codomain but a different rule of assignment, and this one is not surjective because there's a point in the codomain that does not have anything mapping onto it. The codomain is not "covered". 

Predicates are functions whose codomain is the set of Boolean values {True, False}. The predicate P on the left has a domain equal to the set of natural numbers and assigns truth values using the statement "n is even". This predicate, thought of as a function, is surjective because for each of the two values in the codomain True and False, there's at least one input that maps to it. In fact there are infinitely many inputs that map to each point in the codomain, namely all the evens map to True and all the odds map to False. The predicate Q on the right on the other hand also has a domain equal to the natural numbes but the rule of assignment is different -- it uses the statement "2n+1" is odd. This statement is true for all natural numbers, so the only element of the codomain that's "hit" by this function is the value "True". Nothing maps to "False". That makes this function not surjective. So one application of surjectivity is that it's a way of describing a predicate that is always true, or one that is always false but does not have both true and false values. 

What happens if the codomain is an infinite set? Let's take a look. This function f has a domain and a codomain equal to the set of real numbers and it's defined by a formula, f(x) = x**2 + 1. This function is NOT surjective because not all points in the codomain, which is the entire set of real numbers, has something mapping to it. In particular, nothing maps to 0 because x^2 is always bigger than or equal to 0 and so x^2 + 1 is strictly bigger than 0. So 0 is never hit, and so are a lot of other real numbers. Actually we can visually see this if we use a graphing calculator. Graphing this function shows that there are a lot of points on the y-axis that have no point of reference on the graph, so that's a visual cue that the function is not surjective. 

But the function g from the real numbers to the real numbers given by the formula g(x) = 2x + 3 *is* surjective. To explain this, we need to explain why every point in the codomain has at least one element of the domain mapping to it. Since that's a universal statement, an example won't constitute a complete explanation. But, it doesn't hurt to play with some examples first. Let's suppose I picked 2 out of the codomain. What maps to it? Well, it would have to be a real number x such that 2x + 3 = 2. When you phrase it like that, I think I can find that x value. Solving this equation gives me 2x = -1 and so x = -1/2. That's the point in the domain that maps to 2. 

That's just one example and it's not a convincing explanation, but I think I can use this example to make a convincing explanation that does not have any specific values used. Pick any point out of the codomain and just call it "b". Can I find a point that maps to b? Well, it would have to be a real number x in the domain such that f(x) = b. But the formula for f tells me this would mean 2x + 3 = b. I can now solve that equation and get 2x = b-3 and so x = (b-3)/2. So given *any* b from the codomain, I've shown a generic process for finding the value in the domain that maps to it. That makes this function surjective. 

In this video you've learned about surjective functions and how they are defined, seen several examples of surjective and non-surjective functions, and looked at how to show in a convincing way why a function is or is not surjective. In our next video, we'll look at functions that have different combinations of being injective and being surjective. 


## 3.11

We've learned about injective functions --- a function between two sets that has no collisions -- and surjective functions -- which are functions between two sets where all points in the codomain are "covered" by the mapping and no points are left uncovered. We're now going to look at what happens when you start combining these two properties. 

Think back to several videos ago when we were talking about cardinality of sets. We had this example explaining why it was hard to talk about the cardinality of infinite sets because it can be counterintuitive. In that example I argued that the natural numbers and the even numbers in one way of thinking about it had the same number of elements, even though the evens are clearly a subset of the entire set of natural numbers, because I was able to construct a one-to-one correspondence between the entire set of natural numbers and the set of just the evens. Because every even number pairs up with exactly one natural number, that seems to say that these two sets "have the same number of elements" even though we can't put an actual numerical value on the number of elements because they're both infinite. So these one-to-one correspondences are a way to express the fact that two sets have the same cardinality even if computing the number of elements in the set is impossible. 

Looking at this one-to-one correspondence now, you might notice a few things. First, this correspondence is a function from the set of natural numbers to the set of even natural numbers. Every natural number has an output, and no natural number gets split off into two different outputs. Not only that, this function is injective --- it would take a little more careful argumentation to prove it, but the diagram should convince you that there are no collisions here. And finally, this function is not only injective, it's also surjective because every point in the codomain, the set of all even natural numbers, does have something mapping to it -- namely the natural number that's half of the even number. So this is a function that is both injective and surjective and that's what makes it a useful counting tool. 

These kinds of functions are so useful for practical purposes in fact that we give them a special name. We call them **bijective**. A bijective function f from A to B, sometimes just called a "bijection", in other words is just a function that is both injective and surjective. The function we just saw from N to the even natural numbers given by f(n) = 2n is bijective. But as always let's look at some examples and non examples. 


This mapping from the set {1,2,3,4} to the set {x,y,z,t} is a valid function -- every input has an output, and only one output not two -- and it's surjective because every point in the codomain has something in the domain mapping to it. And it's injective because there are no collisions --- every pair of distinct or different points in the domain map to distinct or different points in the codomain. Since the function is surjective and injective, it's bijective. 

Notice any two sets that are connected by a bijective function have to have the same number of elements. But the converse isn't true -- just because a function goes between two sets with the same number of elements, it doesn't make the function bijective. Here for example here are two other functions between the sets {1,2,3,4} and {x,y,z,t} neither of which are bijections. The first one, g, maps everything in the domain to "x". THis is a massive collision so the function is not injective, and since it's not injective, it can't be bijective. The second one, h, is not surjective because nothing maps to the point "y". Since it's not surjective, it's not bijective. You probably see that neither of these two functions is either injective *or* surjective. Is it possible to have a function that is one but not the other, either injective but not surjective or surjective but not injective? 

The answer to that question is definitely yes. A good example is the birthday function we looked at earlier, mapping the set of all students at your university to all the days in the year. Assuming your student body is more than 365 students, two things 100% likely: That for each day of the year, there will be at least one student who was born on that day, which makes the birthday function surjective. But also, there will be two students who have the same birthday, which makes the function not injective. And therefore not bijective. 

On the other hand, some functions can be injective but not surjective and here's a simple example: Look at the function g from the natural numbers to the integers that does nothing but send the input to itself. So g(1) = 1, g(2) = 2, and so on. This is pretty clearly injective, since two different inputs will go to different outputs always because the outputs are the inputs. But this function is not surjective because there are elements in the codomain like -1, -2, -3 that are never hit. So that may look like a one-to-one correspondence but it's not a bijective function. 

Again, one of the major applications of bijective functions is that they are tools for counting things. Here's an example that will be really important for us later. Look at the set A of all eight-bit strings that have exactly 3 "1" bits. For example 11100000 and 01011000 are elements of that set. Now look at the set B of all eight-bit strings that have exactly 5 "1" bits, like 00011111 or 11001101. It's not obvious how many elements are in each of these sets. We'll be solving that problem later. But I *can* show you that these two sets have the same number of elements, the same "cardinality", without actually counting the number of elements in them. I can do this by setting up a bijective function from one set to the other. And here's how that works. 

Let f be the function from A (the set of 8-bit strings with 3 "1"s) to B (the set of 8-bit strings with 5 "1"s) defined like this: Given an input, which is an 8-bit string, the output is the 8-bit string I get by flipping all the bits --- 1 to 0 and 0 to 1. For example 11100000 would map to 00011111. Now this is a valid function because every input does have an output, and the output actually belongs to the codomain because if I start with a string with exactly 3 1's, that means I have 5 0's, and so the output will be a string with 3 0's and 5 1's. And also, no input string gets split off into two outputs. 

Moreover this function is injective, because if I take two different inputs, they are different because they have a different bit in at least once place, and that bit will be different in the output once I flip it. And also, this function is surjective. Because if I pick a string from the codomain, to find the input that maps to it, I just change all the bits and this will give me an 8-bit string with 3 1's that will map back to the codomain string I started with. 

So this bit-flipping function is a bijection between the sets. And that means that there are exactly the same number of 8-bit strings with 3 1s as there are 8-bit strings with 5 1s --- even though we still don't know how many those are. 

In this video we learned about bijective functions or bijections, which are functions that are both injective and surjective, and we learned that they are used for showing that two sets have the same cardinality even when we don't know how exactly to count the number of elements in those sets. Our next video is the last one in this module where we'll look at some special functions of use to computer science and see what properties they have. 




## 3.12


Welcome to the final video in this module on sets and functions. You've come a long way and learned a lot since we first introduced the set, 10 videos ago. Take a moment to congratulate yourself! In our final video, we're going to look at five special functions that are really important and useful in computer science. We'll look at their definitions and how they're implement in Python 3, and also look at their properties as functions. 

The first two of these have to do with rounding. Since we work so often with integers, it's helpful to have functions on hand that will take a number that isn't an integer and turn it into one that is. The simplest way to do that is rounding. There's three ways to round, as you know --- rounding off, rounding down, or rounding up. Computer science makes particular use of the last two. The function that implements rounding down is called the FLOOR function. In mathematical notation it uses brackets like this with horizontal pieces on the bottom or on the "floor". The floor function simply takes in a real number as input and outputs the greatest integer that it less than or equal to it -- in other words it rounds down. For example, the floor of 2.9 is 2. The floor of -2.9, is -3 (because -3 is less than -2.9). If you input an integer to begin with, there's nothing to round so it just outputs itself. 

As a function, the domain of the floor function is the set of real numbers and the codomain is the set of integers. This function is *not* injective because there are a lot of collisions --- in fact any two numbers that are in between two integers will map to the same thing, for example the floor of 5.4 and the floor of 5.8 are both 5. But the floor function is *surjective* because if you start with any integer in the codomain, you can find something in the domain that maps to it --- for example the integer itself will map to it. 

A companion to the floor function is the **ceiling** function which rounds up instead of down. The ceiling of x is the smallest integer greater than or equal to x. The mathematical notation is similar to floor, except the horizontal parts on the brackets are at the top or the "ceiling". For example the ceiling of 2.9 is 3 and so is the ceiling of 2.000001. The ceiling function is also a mapping from the real numbers to the integers. The example we just saw shows you that this function, like floor, is not injective but it is surjective for the same reason floor is surjective --- given an integer in the codomain, you can always hit it by plugging in just the integer itself.  Some more examples are ceiling of 3 is 3; the ceiling of 0.9 is 1, and the ceiling of -0.9 is 0. 

The floor and ceiling functions are available in Python but they're not part of the standard library of functions that Python loads by default. To access them, you have to load the math package which is a library of mathematical functions. To do this, enter `import math`; once this library is loaded you do not have to load it again until you restart Python. And then to call the floor function, type math.floor and then the input in parentheses. Ceiling is also in the math library, and it's accessed by math.ceil and then the input in parentheses. Here are some more examples of use. 

Here's a function that we will get to know extremely well in Module 4. It's called the factorial function. This is a function from the natural numbers to the natural numbers, defined like this. We use an exclamation point after the input to denote it, and we define 0! to be 1, and if n is a natural number bigger than 0 we define n! to be the product 1 * 2 * 3 * 4 * and so on up to (n-1) times n. So n! is the product of the natural numbers from 1 to n, unless you're looking at 0! and in that case the output is defined to be 1. For example 5! is 1 * 2 * 3 * 4 * 5 , or 720. 

The factorial function can also be defined recursively, meaning that we can define it by calling the function on smaller versions of itself. Just start with an initial condition 0! = 1 and then define n! to be n times (n-1)!. In that way of thinking about it, 5! is 5 times 4!. But then 4! is 4 times 3!, 3! is 3 times 2!, 2 is 2 times 1! , and 1! is 1 times 0! which is equal to 1. That gives us the product we saw earlier. The recursive definition is extremely important and handy for counting arguments as we'll see. It also helps you to see that the factorial function is strictly increasing --- every time the input increases, the output increases, and that means that the function would have to be injective because different inputs will lead to different outputs. The factorial function is not *surjective* because for example nothing maps to the number 4. 

The factorial function is available in Python, also in the math library by typing math.factorial and then the number. For example here's 5 factorial, and we can easily make a little table of factorial values from 0 through 10. As you can see the factorial function grows extremely fast. We'll be using the factorial function for counting purposes; for example we'll be learning that n! is the number of ways to arrange a list of n distinct objects. (That's why 0! is 1, because there's only one way to arrange an empty list of objects, and that's to do nothing.)

Finally, there are two special functions related to division. One of these you have already seen and that is the modulus function. We use a percent symbol to represent it, and it's a function that takes in a pair of numbers, one an integer and the other a natural number bigger than 0, and returns the remainder obtained when dividing the first number by the second. As a function this means the domain is the cartesian product of the integers with the set of positive natural numbers, and the codomain is the set of all natural numbers. This function is not injective because for example the pair (0,10) and (10,10) both map to 0. But it is surjective, because starting with a natural number in the codomain you can for example plug in that number mod that number + 1 and this produces the number you started with. 

And going along with the mod operator is the DIV function, which does kind of the same thing as mod except it returns the quotient instead of the remainder. There's not really a symbol for this function and many times people just write DIV(a,b) to mean the quotient we get when dividing a by b. For example DIV(100,5) is 20 whereas 100 % 5 is 0. 

In Python you can access those two functions mod and div without loading any libraries. The mod function you know is accessed using the percent symbol. DIV on the other hand is implemented using a double slash like this. This means "integer division" in Python 3. So if you write 15/4 you get this floating point number, but 15 // 4 gives you 3. Important note here, in Python 2, the previous version of the language, the *single* slash denoted integer division. So be mindful which version of Python you are running! 

And that's a wrap for module 3. In module 4, we'll be putting all of our knowledge of sets, functions, and logic to work on solving problems where we are counting complex arrangements of things. It's a lot of fun and I'll see you there. 