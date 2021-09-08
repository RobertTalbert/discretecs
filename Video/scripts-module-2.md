# Scripts for Module 2 videos 

## 2.1

Human beings communicate with each other using language. Computers use languages too, but they don't really look (at least not yet) like human languages. In this next module of videos, we're going to look at the question of how we take our human language and turn it into something that we can use to communicate with machines. This isn't going to be a full course on language design like you might study later. Rather just as in the first module, we're going to take a look at the foundations: To the basics of our language to see what works in EVERY computer programming language you might choose to study or use. 

So what aspects of language ARE usable by computers? Well, keep in mind that computers (as much as we might suspect otherwise) do not actually "think" and cannot process language, really cannot process anything other than bits. But this connection to bits gives us a way to bridge human language with computer operations: We can use the bits to represent the two opposing states of TRUE and FALSE. If computers process bits, they can process truth values --- sometimes called Boolean values in computer languages. A 1 represents TRUE, and a 0 represents FALSE.

So if we restrict human language only to those statements that can be validated as true or false, that's how we can "talk with" computers. The study of reasoning using strict rules of validation of truth, is called logic. So at the foundations of how we work with computers, is not only mathematics as we saw earlier, but also logic. 

Statements that can be validated as true or false, are known as propositions. Although sometimes we'll just call them "Statements". A proposition in other words is a complete thought --- often a complete sentence or mathematical expression --- that has a definite and knowable truth value. Some examples include: 

Lansing is the capital of Michigan. -- This is a complete sentence, and it has a definite and knowable truth value. In fact we know this statement is TRUE. 

Chicago is the capital of Illinois -- Also a complete thought with a definite truth value. It's FALSE, and because we know it's false, it's a proposition. 

5 + 7 = 12 -- Not an English sentence but a complete mathematical thought that has a definite truth value of TRUE. 

7 - 2 = 10 -- Again, a complete thought with a definite truth value, this time FALSE. 

Some non-examples (things that are NOT propositions) include: 

Michigan is a beautiful state. -- This is a complete sentence, but it's an opinion or a judgment call and cannot be objectively evaluated as true or false. I think it's true, but you might not. 

Let's go to Chicago. -- A complete sentence, but this is an imperative not a statement that is true or false. You can agree that you'd like to go to Chicago, but this is different from saying this statement is true. True/false values don't really make sense here. 

Where is the bread? -- Also a complete sentence, but it's a question and questions don't have truth values. 

x + 5 = 12. This is trickier. This is a complete mathematical thought, but we cannot tell if it's true or false because there is not enough information. This statement --- that the left side of x+5 is equal to 12 --- is true for some values of x but false for others. Without knowing which x we are talking about, it's impossible to tell whether this is true or false. So it's not a proposition; eventually we will say that this statement is underdetermined, and we'll call such things predicates. 

Now you try it. Here are some statements, some of which are propositions and some of which are not. Pause the video and identify which ones are which. 

...

So these are the propositions here because they all have definite, knowable truth values. The others are not. This first one is an opinion, not a statement that can be objectively true or false. This one is a question, and since questions don't claim that something is true or  false, they have no truth value. This statement here, x mod 2 equals 0, is underdetermined --- it's true for some values of the variable and false for others, so its truth value depends, which makes it not a proposition. However the last statement is a proposition --- it is true that if x is even, x mod 2 is  0. What makes the difference here is that the variable x is "quantified" --- we are putting a scope around the second part of the statement and claiming that x mod 2 is 0 for ALL even integers. Because we've quantified the variable and not just left it alone, we can evaluate the truth of this statement. we'll talk more about quantification in a later video. 

In this video, you learned about what logic is and why it's important for computer science, what a proposition is, and how to tell the difference between propositions and non-propositions. In the next video, we'll look at some basic ways to build complex logical propositions out of simple ones using connectives. 

## 2.2

In the last video, we introduced the idea of logic as a way for human beings to  communicate with computers. And we defined a proposition as a complete thought that has a definite and knowable truth value. In this video, we're going to look at how we can build complex logical statements out of simple ones using logical connectives. 

Look at this basic recipe for peanut butter cookies. It's a list of instructions on how to combine the ingredients and it ends with, "Bake in a preheated 375 degrees F oven for about 10 minutes or until cookies begin to brown." In some ways this recipe is like an algorithm. It has input, instructions, and a definite ending point. What triggers the ending of the process in this case? It's not one but two possible conditions: either the cookies have baked for 10 minutes or they are turning brown. If I were a robot checking the doneness of those cookies, I'd have to monitor them and the clock and evaluate the truth values of two logical propositions: "Ten minutes have passed", and  "The cookies are turning brown". If either one of those propositions becomes true --- or if both of them are true --- then I stop the cooking process. 

What that last condition in the recipe does, then, is CONNECT two logical propositions with the word "or", making a larger proposition. The word "or" here is an example of a connective -- an English word that connects two smaller propositions to make that larger one. We sometimes say that a proposition that cannot be broken down into a bunch of smaller ones is an "atomic" proposition, and a proposition that isn't atomic --- if it's made up of atomic statements joined by connectives --- is called "molecular". 

There are three basic forms of connectives that do this for us. 

Maybe we need some part of a computer program to activate if, like in this recipe, any one condition from a list of conditions is true. Again as in the recipe we usually use the English word "or" to connect the conditions. A statement created by joining two atomic propositions together with "or" is called a "disjunction". And a disjunction is true, whenever either one or both of the propositions it joins is true. For example: "Either I passed algebra, or I passed C++" is a disjunction. If you passed algebra but didn't pass C++, the disjunction is true because the first proposition is true. You were telling the truth in other words when you claimed that you either passed one class or you passed the other. Same for if you didn't pass algebra but did pass C++. If you passed both, the disjunction is true because if you passed both, then you definitely passed one. That makes our use of "or" into what we call an "inclusive or", so the "or" statement is true if either one OR BOTH of the atomic propositions involved is true. The only way a disjunction can be false is if both statements involved are false. For example if you did not pass either algebra or C++, this statement that you passed one or the other of them is false. 

One of the nice things about logic is that the content of the statements involved doesn't really matter, only the form. The truth value of a molecular statement in other words is always determined only by the truth values of the atomic statements that make it up and the connectives being used, and nothing else. For example, any time you form a disjunction from two statements, the disjunction will be true if one or both of the statements involved is true.

This lets us summarize the conditions where a complex statement will be true and where it will be false in a table, like this. Here, the v-looking symbol is a mathematical symbol used to represent the english word "or". Different symbols represent "or" in different computer languages, for example the double vertical bars || represent "or" in Java and in C++. In Python you just type the word "or". Since this disjunction involves two independent Boolean values each of which is either true or false, it leads to four combinations of true/false values. In each case the truth value of the disjunction is listed in the final column. As we saw, when either one or both of the basic propositions is true, the disjunction is true. When both are false, the disjunction is false. This table is called a TRUTH TABLE and we will be seeing much more of these in a minute and in other videos. 

Sometimes we need a part of a program to activate if ALL of the conditions in a list are true. For example, to take discrete math you might need a passing grade in both algebra AND C++, not just one or the other. We use the word "and" and a symbol that looks like an upside down v to represent this connective, which we call a *conjunction*. In a conjunction of two propositions both propositions must be true in order for the conjunction to be true. That's summed up in the truth table for conjunctions which you see here. The conjunction is false otherwise --- that is, whenever one or both of the atomic statements that make up the conjunction is false. 

Sometimes we need a part of a program to activate if a single proposition is NOT true. THis is a connective called a negation, and we use this symbol to denote it. Negations are different than disjunctions or conjunctions because they only work on one statement --- if you have the statement P, then ~P is its negation. The negation ~P is true when P is false and false when P is true --- it's the logical opposite of the original statement. 

In this video you learned that we form complex logical statements out of atomic statements with connectives. We saw three basic connectives, "or" (disjunction), "and' (conjunction), and "not" (negation). And we learned about the concept of a truth table which allows us to see the truth values of a molecular statement as determined by the truth values of the atomic statements and by the connectives that join them. In the next video we'll look another connective, the conditional or "if-then" statement. See you there. 

# 2.3

In our last video, we saw how to form complex "molecular" propositions by taking small "atomic" propositions and joining them with "connectives". We looked at the connectives AND, OR, and NOT. In this video we'll look at another connective that is a little more complicated but very important. 

Everywhere we turn, we run into situations that connect conditions in a cause-and-effect way. Legal systems are built on these kinds of situations. "If you drive faster than 55 mph, you will get a speeding ticket." Or, "If you steal money, you will go to jail." It's not just in the law that you see these. In your course syllabus you might see statements like "If you miss a deadline, you must ask for an extension." And we make promises all the time, for example I might tell my kids "If you clean your room, then we'll get ice cream." 

All these statements have things in common. They are made up of two conditions, and if the first condition is met, then we expect the second condition to also be met. If the first condition is met but the second one isn't, then we'd consider the entire statement to be faulty, like a broken promise or an unenforced law. The connection between the conditions isn't through a single word like the and and or constructions from the last video, but through "if-then" although we do not always write the word "then". 

This if-then construction is another connective, in other words, that joins two propositions into a larger one. We call these if-then statements _conditional_ statements because if a condition is met, then an action is supposed to be performed. Conditional statements are everywhere in life and in computer science, so we're going to take a very close look at these. 

First, in a conditional statement, the condition to be met -- usually preceded by "if" -- is called the _hypothesis_, and the statement that follows -- often preceded by "then" -- is called the conclusion. Here you can see the hypotheses and conclusions for each of the examples we mentioned earlier. 

A conditional statement is a proposition, meaning that it's a complete thought that has a definite and knowable truth value. So how do we know when a conditional statement is true? This takes some thought, so let's use a simple English example, the promise to my kids of "If you clean your room, then we'll get ice cream." It's helpful to think about when this statement is NOT true. A false conditional statement is like a broken promise. My promise to my kid is false in the situation where they do clean their room, but we do NOT get ice cream. Because in a conditional statement, any time the condition is satisfied, the action must follow. If that ever DOESN'T happen, then the conditional statement is false. 

Obviously my promise to the kids is good in the situation where they do clean their rooms and then we do go get ice cream. But what happens if they don't clean their rooms? Well, my promise says nothing about what we will do if they _don't_ clean their rooms. If they don't clean their rooms and we don't get ice cream, I haven't broken my promise. But if they don't clean their rooms and we do go get ice cream anyway, I still haven't broken my promise. Again my promise only said what will happen if they DO clean their rooms. If they don't, my promise as stated lets me do whatever I want. 

All conditional statemnts obey the same rules of truth --- cleaning rooms and getting ice cream are just details. In ANY conditional statement, say "If P, then Q", -- and by the way, the symbol for this is an arrow that points from the hypothesis to the conclusion -- the truth table would look like this: 

First of all if both the hypothesis and conclusion are true, then the conditional statement is true. If the kids clean their room and we then get ice cream, I've kept my promise. If you speed and then you get a ticket, the law has been enforced properly. And if the hypothesis is true and the conclusion is false then the conditional statement is false. If the kids clean their rooms but I back out of getting them ice cream, I have not kept my promise. If you speed but do not get a ticket, the law has not been enforced properly. 

If the hypothesis is false, then if the conclusion is true OR if the conclusion is false, the conditional statement is still true. If my kids don't clean their rooms, I'm not breaking my promise if I get them ice cream anyway, and I'm also not breaking the promise if I don't. 

So this is what the completed truth table for a conditional statement looks like. Conditional statements in other words are always true except in this one situation where the condition is met but the action doesn't follow. 

In this video we learned a new connective, the if-then construction which makes a conditional statement. YOu learned that the condition is called the hypothesis and the action that follows is the conclusion. You also learned the truth table for a conditional statement and that conditional statements are always true except when the conclusion does not follow from the hypothesis. In the next video we're going to look some more at conditional statements particularly at variations on the basic if-then construction. 

## 2.4

In the previous video we introduced conditional statements, often in the form "If A, then B" where A and B are propositions. This makes a new proposition, which is true in all cases except when the condition, or hypothesis, is met but the conclusion does not follow. Conditional statements are so common that it's worthwhile to look at some variations on this idea, which we'll do now. 

There are three statements that commonly get formed from a conditional statement. Let's start with a basic conditional statement, "If P, then Q". 

First, we have the _converse_ of this statement which is "If Q, then P". The converse of a conditional statement in other words is the statement you get when you switch the hypothesis and conclusion. For example if the original statement is "If it's raining, then it's cloudy" then the converse is "If it's cloudy, then it's raining". 

Next we have the _contrapositive_ of the statement which states "If not Q, then not P." The contrapositive is like the converse except we not only switch the hypothesis and conclusion but also negate each of them. If the original statement is "If it's raining, then it's cloudy" then the contrapositive is "If it's not cloudy, then it's not raining". 

Finally we have a lesser-known variation called the _inverse_ of the statement which goes "If not P then not Q". The inverse is like the contrapositive except we do not switch the hypothesis and conclusion, just negate each one. If the original statement is "If it's raining, then it's cloudy" then the inverse is "If it's not raining, then it's not cloudy". 

Practice this for a minute using the example from the last video: "If you clean your room, then we'll get ice cream." Pause the video and write out the converse, contrapositive, and inverse of this statement. 

And here are the results! 

So, why bother with these? Mostly it's because the precise structure of these conditional statements is important, and the truth value can change if we change the structure. Look at the example of "If it's raining, then it's cloudy". This seems like a true conditional statement based on our experiences. What about the truth values of the others? 

The converse says "If it's cloudy, then it's raining". This is definitely NOT always the case, because it can be cloudy without it raining. Ask anybody who lives in England. So the converse of a statement is not the same thing as the original statement -- they can have opposite truth values. So you have to be careful to situate the hypothesis and conclusion propertly and not pretend they are interchangeable. 

The contrapositive says "If it's not cloudy, then it's not raining". Now this seems true as well. Does this mean that a statement and its contrapositive say the same thing in different ways? We can't tell based on one example, but we'll be looking at that question in another video soon. 

The inverse says "If it's not raining then it's not cloudy" This seems false, in fact it sounds almost like the converse. So first of all the inverse, like the converse, does not have the same truth value as the original --- so again, beware of the structure. But also, actually if you look at it, the inverse is what you get when you form the contrapositive of the converse. So in one way of thinking about it, we don't need to talk about the inverse, just converse and contrapositive. And it makes it all the more important that we think carefully about this contrapositive idea and whether taking a statement and forming its contrapositive is just rephrasing the original conditional statement in a superficially different way. 

In this video, you learned about three logical constructions related to a conditional statement: the converse, the contrapositive, and the inverse. ANd you learned that the converse and inverse can sometimes have different truth values than the original, while the contrapositive seems like it might be just a rephrasing of the original. We need something more solid about that last point, so in the next video we're going to come back to the idea of a truth table to help us know when two statements might be logically equivalent. 

# 2.5

So far in this module, we've been looking at logical propositions, and focusing on how we can combine simple atomic propositions using connectives to form more complex propositions. In this video we're going to return to the question of how to know when a complex or "molecular" proposition is true or false, and we'll use the results to answer another question from the last video about how to know if two superficially different propositions are logically the same. 

Just to remind you, in logic we deal with statements that have definite and knowable truth values. Complex statements which we've called "molecular" are built up out of simple or "atomic" statements joined by logical connectives like and, or, or if-then. Remember that one of the basic rules of logic is that the truth value of a complex statement is determined only by the truth values of the simple statements that make it up and the types of connectives used -- and nothing else. 

The precise rules for how to find the truth values of these complex statements are spelled out in what we called the truth tables for the connectives. A truth table for a molecular statement is a table that lists all the combinations of the truth values of the atomic statements involved, and then for each of those combinations there is listed the truth value of the molecular statement. 

Here's a basic example that we saw earlier, for the conjunction or "AND" connective. This connective joins two statements, P and Q. Each of those two statements has two truth values, true or false. This gives rise to four possible combinations of truth values, which we'll list in separate rows. The conjunction produces a TRUE statement when both the inputs are true, and FALSE otherwise. This is just a summary of how the word "AND" works in our usual language. So this truth table tells you the conditions under which the conjunction is true, as determined by the truth values of the two statements involved. 

What's powerful about truth tables is that the content of the atomic statements doesn't really matter --- any two statements joined by "and" will have the same truth table. This allows us to perform one of the basic conceptual leaps of computer science -- ABSTRACTION. This means that we can ignore the details of this construction and focus only on its general structure. 

We also saw truth tables for disjunction or "or", as well as a truth table for conditional statements or "if-then". In each of those situations, the connective still operates on two input statements, and the final statement's truth value is determined by the truth values of the inputs. 

We also saw a truth table for negation, or "not". This one was different than the others because it only works on ONE statement. But the truth value of the result is still dependent on the truth value of the input. 

Computers handle many logical operations like these four using what's called a logic gate. This is often a piece of hardware that's the building block for an entire circuit that processes logical values using bits, 0 for false and 1 for true, in the form of electrical signals. For us, logic gates are a handy way to visualize what's happening in a truth table. 

Here's a diagram that represents a logic gate for "and". The connective is the shape that looks like a circuit, and it has two inputs A and B. Each of these is a Boolean value, either true or false, or 1 or 0, and the output is Z. This truth table here is a binary version of the truth table you saw earlier. Down below it is the logic gate diagram for "or". And here's one for NOT. 

In fact you can search and find a host of logic gate diagrams for all sorts of connectives many of which we haven't seen here. You might notice there isn't one for "if-then". Why is that? You'll have to stay tuned to the next video for that. 

One very important use of truth tables is to give us a rigorous answer to the question of whether two propositions are "logically the same" even though they may look different. This came up in the last video when we noticed that a conditional statement and its converse can sometimes have opposite truth values, while the statement and its contrapositive appear to be "the same". 

We say that two propositions are "logically equivalent" if they have the same final truth value in each possible combination of truth values of the simple, atomic statements that make them up. This means essentially that the two statements are "logically the same" even though they may be phrased differently. 

We can use truth tables to know when two statements are logically equivalent and when they aren't. Let's look at if P, then Q. Here is its truth table. Now, let's set up a truth table for its converse, If q then p. 

To set up the truth table, we list the atomic statements in columns like this. I'll keep the ordering the same here with the column for P to the left of the one for Q. Now create a row for each combination of the truth values of the atomic statements. Since there are two of those, there are four truth combinations and I'll keep them in the same order as the first truth table. Then I'll make one column for the final proposition. 

Now, in each row, let's use the connective to determine the truth value of the final result. The statement we're working with here is If Q then P. Very importantly here, remember that a conditional statement is true in all cases except when the hypothesis is true but the conclusion is false. It doesn't matter what the hypothesis or conclusion *are*. In this case the hypothesis is Q and the conclusion is P. So go one row at a time and determine the truth value. In the first row, P and Q are both true. So the hypothesis, Q, is true and the conclusion Q is also true. That makes the entire conditional statement true. In the second row. P is true and Q is false. This means the hypothesis of the conditional statement is false, and the conclusion is true. Remember that in such a case, the entire conditional statement is true. 

Let's stop for a moment. The hard part of this process is that we have to think about how the proposition is put together in each row, and not just copy from an existing truth table. You might have wanted to put FALSE in this second row because in the truth table for if P then Q, this was FALSE. But this isn't if P then Q, it's if Q then P. So here we have to remember that Q is not the conclusion, it's the hypothesis. 

Now you take a moment to fill in the last two rows of the truth table. Pause the video and then come back for a debriefing. 

So in the third row, we have P false and Q true. In the conditional statement, this means that the hypothesis is true and the conclusion is false. That's the one situation where the conditional statement is FALSE so that's what we put here. Then finally in the last row, we have both statements false, in particular the hypothesis is false which remember makes the entire statement true. 

Now pull back and look at both truth tables. We see here that the original conditional statement and its converse are NOT the same truth value in all the same situations. In particular here when P is true and Q is false, if P then Q is false but if Q then P is true. So that means the conditional statement and its converse are NOT logically equivalent. 

What about the contrapositive? We caught a glimpse in the last video that maybe a conditional statement and its contrapositive might be logically equivalent. Are they? What does the truth table for the contrapositive look like? Stick around to the next video to find out. 

# 2.6 

In the last video we learned about truth tables and how they can be used to determine if two statements are logically equivalent. In this video we're going to extend that idea to think about how to construct a truth table for a proposition that has a more complicated structure than just a basic connective. 

We ended that video wondering about If P, then Q and its contrapositive which is If not Q  then not P. Let's build a truth table for that contrapositive and see if it's really logically equivalent to the original. Making this truth table is going to be harder this time because more is happening in the contrapositive than just switching the hypothesis and conclusion. There are two intermediate steps: First we negate the hypothesis and then we negate the conclusion and then we switch them. In order to keep careful track of what's happening, in the truth table for the contrapositive I'm going to create columns for the atomic statements P and Q, and a column for the final proposition if not Q then not P, but I am also going to create two other columns, one for each of the intermediate steps, negating P and negating Q. 

Just as in the last video, I'll make one row for each of the combinations of truth values of the inputs. I'll put these in the same order as we did then. Next, rather than look directly at the final proposition, I'll do the intermediate steps first. In the column for not P, I'm just looking at the truth value for P and putting down its opposite. And then I'll do the same in the column for not Q. 

And now I'm looking at the contrapositive. This has "not Q" as the hypothesis and "not P" as the conclusion. Remembering that a conditional statement is true in all cases except where the hypothesis (which this time is "not Q") is true but the conclusion (which is "not P" this time) is false, I can see that the final proposition is false in this row, where again not Q is true but not P is false. In all other rows, either the hypothesis is false (as in rows 1 and 3) or both hypothesis and conclusion are true (in row 4) so those result in TRUE. 

Now looking back at the truth table for If P then Q, I can see that the outputs are the same in each possible combination of truth values. That means every conditional statement is logically equivalent to its contrapositive. 

So, making a truth table for a complex proposition is a little like doing an arithmetic calculation with a lot of parentheses and operations. In this calculation here for example, we'd use natural order of operations to do the computations in parentheses first, then exponents, then multiplication, and finally the addition. We build up the computation from the lowest level gradually to the highest level. Similarly when making a truth table for a proposition with a lot of parts, we work from the lowest level and gradually assemble the entire proposition, using separate columns in the truth table to keep track of the intermediate steps. 

Let's look at another example: (not P) or Q. Let's set up the rows and columns of the truth table. First there's two columns for the input variables P and Q. Now building from the lowest level up, I'll need a column for "not P", then a column for the final statement (not P) or Q. Pause the video here and see if you can fill in the rest of the truth table. 

We put in four rows for the combinations of truth values of two variables, like so. We fill in the truth table from the lowest level first. That's "not P", which is just the opposite of whatever truth value P has. Now to get that last column, we remember that a disjunction is true when one or both of the parts is true. That means we should put false here, in row 2, and true everywhere else. So here's the final result. 

If that looks familiar, then you're paying attention, because this is the same truth table as if P, then Q. That means that If P then Q is logically equivalent to (Not P) or Q. And that's why when we looked at logic gates earlier, we didn't see one for a conditional statement --- it's because we didn't need one. We can just chain together the logic gate for NOT with the logic gate for OR. 

Now let's look at one more example. You might have wondered in the last example whether the parentheses around "not P" were necessary. Well, if you leave them off, you get this, which might be interpreted as not (P or Q), that is the negation of the entire statement "P or Q". Is that statement logically equivalent to (not P) or Q? Pause the video and make a truth table for not (P or Q) and find out. 

To set up the truth table, as always we'll include two columns for the input variables. This time there's still an intermediate step, but it's to form P or Q first. Then the final step is to negate the statement P or Q. As before, there are two inputs so that's four combinations of truth values, and we'll put those in as we've been doing. Now let's work from the bottom up. First look at P or Q. This will have a FALSE here, in row 4, and TRUE elsewhere. Now in the final column, we are negating all that, so we simply flip the truth values to get False, False, False, True. That's a complete and correct truth table. And you'll notice it's definitely not the same as the truth table for (not P) or Q, so those two statements are not logically equivalent. Which tells us that parentheses do matter here. 

In this video and in the last one, you learned how to make a truth table for a logical proposition with two atomic inputs, even when there are intermediate steps involved, and how to use those truth tables to determine logical equivalence of propositions. The next video is one more look at truth tables, and we'll raise the level of complexity to look at propositions with multiple intermediate steps as well as those with three and even four input variables. 


- Contrapositive
- General principle of building multi-step truth tables
- Example
- Example

# 2.7

We've been looking at truth tables as a way to tell when a complex, molecular statement is true based on the truth values of the inputs. In the last video we saw how to make a truth table for a proposition that has intermediate steps. In this video, we'll wrap up our initial discussion of truth tables to look at two-variable statements that have multiple intermediate steps, and statements that have three variables. 

Let's begin by looking at the proposition "If (P or not Q), then ((not P) and Q)". This proposition has a bit more complexity than some of the others here and it's not obvious at all when this statement should be true. So let's make a truth table for it. 

We'll begin as we normally do, by setting up one column for each of the input variables. Then let's go ahead and make a row for every combination of the truth values of those inputs. Since there are two inputs, there will be four combinations and I'm going to put those here in the same order as we have been doing. 

Now, just like when we looked at the contrapositive in the last video, we need to build up the main proposition from the bottom up, like we would do an arithmetic computation with a lot of nested calculations. We'll make one column for each "level" of the statement. Looking from left to right in the main proposition, I can see that we'll need a column for "not Q". I'll also need a column for "not P" and I could make that column now, but instead I'm going to continue building up this first part, the hypothesis of the main proposition by creating a column for "P or not Q". 

Again the order in which we set up these columns strictly speaking doesn't matter, but it can make a difference in how well your brain can keep track of the process, and I find it easier to finish up each part of the main proposition in turn. 

So now that the hypothesis of the main proposition is present, let's work on the conclusion. We need a column for not P, and we need a column for "(not P) and Q". And then finally we need a column for the main proposition. 

Let's now fill in each of those columns one at a time. The column for not Q is easy since it's just the opposite of whatever truth value appears in Q. Similarly, not P is the opposite of P. 

Now, for "P or not Q", we have a disjunction. A disjunction is true whenever one or both of the statements involved is true, and false otherwise. The two statements involved are P, and "not Q" so look at those. Given the information in those two columns, which we already built, we should have TRUE in rows 1, 2, and 4 and FALSE in row 3. 

Now let's do the column for "(not P) and Q". This is a conjunction, which we know is true whenever both statements involved are true and false otherwise. The statements involved are "not P", and "Q" so look at those columns. They are both true in row 3, otherwise at least one of them is false. So we have TRUE in row 3 and FALSE elsewhere. 

Finally we're ready to fill in the column for the main proposition. This is a conditional statement, and remember, these are true in every situation except where the hypothesis is true and the conclusion is false. The hypothesis in this case is "P or not Q". The conclusion is "(not P) and Q". In row 1, the hypothesis is true and the conclusion is false, so put FALSE in the last column. The same is true for rows 2 and 4. In row 3, the hypothesis is false  and in that case we have a TRUE conditional statement. 

So there's a complete and correct truth table for this proposition. It's not in principle any different than the others, it just required more care in building up the table. 

But now let's look at something different the statement "If (P and not Q), then R". What's different about this is that there are *three*  atomic statements involved here, not just two. How does that change the truth table? Let's dive in and see. 

We are still going to need a column for each of the atomic variables here, so one thing that's different is that there are three of those this time. Now, what we need is one row for each of the combinations of truth values of these statements. How many rows should there be? Let's think about it. If we only looked at P and Q and ignored R for the time being, there would be four -- namely these four. 

Adding R into the mix here *doubles* the number of rows we need. There is one copy of these four rows needed for the case when R is true, and another four rows needed when R is false. That's a total of eight rows. That will be the case whenever we have three atomic variables, again because we need four rows for two variables and then two copies of those four rows, one for each truth value of the new variable. In fact there's a general principle here: Adding a new variable doubles the number of rows needed in the truth table. If we had a statement with four variables, we'd need 16 rows --- one copy of these eight rows for when the new variable is true, a second copy for when the new variable is false. 

Now that we have the eight rows needed, we can start putting the proposition together just like usual. Pause the video and try to set up the columns we'll need, and if you're feeling adventurous, go ahead and try to complete the table you get! 

It looks like we'll need a column for not Q, a column for (P and not Q), and then a column for the main proposition. Let's build it up one piece at a time. Not Q is just the opposite of Q. "P and (not Q)" is a conjunction, true whenever both statements involved are true so that we should have TRUE in rows 2 and 6 and FALSE elsewhere. In the final column, it's a conditional statement which we know is FALSE when the hypothesis is true but the conclusion is false, and this happens in line 6 only. Everywhere else either the hypothesis is false or both statements are true, so there's TRUE there. 

So again in principle making a truth table for statements with three or even more variables isn't any different than simple truth tables, other than the size. We still focus on building up the proposition in a modular way and using the table to keep track. 

In the next video, we'll look at something different, the concept of a predicate. 

## 2.8 

In all of the earlier videos in this module, we've been looking at propositions -- complete statements that have a definite and knowable truth value. We've seen lots of examples of propositions and learned how to work with them. In this video we're going to re-introduce an earlier example of something that *wasn't* a proposition. 

Here's that example: x + 5 = 12 . This is a kind of statement, namely it's an assertion that the expression on the left side of the equals sign is actually equal to the expression on the right. So it's a complete thought; but it doesn't have a definite truth value as is because of that variable "x". Whether this statement x+5 = 12 is true or not depends on the value of that variable. If x = 10 for instance, then the statement x + 5 = 12 is false. But if x = 7, the statement is true. 

We're going to call a complete statement whose truth value depends on the value of one or more particular variables a **predicate**. Predicates are different from propositions. While both predicates and propositions have truth values, the truth value of a proposition can be known just from the proposition itself without any outside input, while the truth value of a predicate depends on outside input. Propositions have only one truth value, while in general the truth value of a predicate will be True for some inputs and False for others -- it depends. 

For notation, while we often use letters like P, Q, or R to represent proposition, we affix a variable in parentheses to the letter for a predicate. For example, could write this to mean "the predicate P with variable x, is the statement that x+5 = 12". We pronounce that first part "P of x". The allowable inputs for a variable in a predicate is called the *domain* of the predicate. For example for P(x) here, the domain could be all real numbers. But here's another predicate: Q(x) is the statement x % 3 = 0 , and for this predicate not all real numbers might make sense; instead the domain is the set of integers because that's the only thing we can apply the modulus operator to. 

Some predicates might have even smaller domains, for example this predicate B(x) = "Prof X has a beard". Apparently "x" represents not a number but a faculty member now, and since there are a lot of faculty members out there, we might just explicitly state the domain for example by saying the domain is the set of all mathematics professors at your university. 

More formally we would say that a predicate is a function, whose domain is a given set and whose codomain is the set {TRUE, FALSE}. This is using some language we have not defined yet, but we'll be doing that in the next module. It just means that a predicate is like a machine that accepts inputs from a given collection, performs some kind of process, and produces outputs of either TRUE or FALSE.

Predicates are extremely important and useful in computer science, not least because they themselves are like tiny computer programs with an input of a certain type, and which output either TRUE or FALSE. Here for example is a Python version of our first predicate. You plug in a real number for x, then go through a process to return either TRUE or FALSE. 

Let's look at some more examples of predicates. 

S(x) = the length of x is 7

where x is a string, and the domain is the set of all possible strings. Again it's helpful to think of this like a little computer program, like this, where you plug in a string and get out either TRUE or FALSE. The predicate itself does not have a truth value until something is plugged in. For example S("Mathematics") is FALSE because the length of that string is 11. But S("Algebra") is TRUE because the length of Algebra is 7. 

Another example: P(x) = x**2 >= 0 where x is the set of all integers. P(x) will be TRUE whenever x**2 >= 0 and FALSE otherwise. So P(2) is true, for instance because 2**2 is 4 and that's bigger than 0. P(10) is also true because 10**2 is 100 and that's bigger than 0... in fact P(x) is *always* true for any input because squaring an integer always returns a result that is nonnegative. 

And another example: P(s) = "the length of s is negative" where the domain is all possible strings. Well, this predicate is never true, because there's no such thing as a string with a negative length. 

Generally speaking we can have predicates that are *sometimes but not always* true, predicates that are *always* true, and predicates that are *never* true. When we talk about *how often* a predicate is true, this is referred to as **quantifying** the predicate. Our next video is going to be all about that idea. 

We can even have predicates with more than one variable, like this: P(x,y) = "xy > 0". This requires knowledge of *two* variables to be able to determine truth. P(2,3) for example is TRUE because 2*3 is 6 which is bigger than 0. But P(-4, 5) is FALSE because -4*5 is -20 which is not bigger than 0. 

Now you give it a try, from a bit of a different angle. Here's a predicate: P(n) = (3n+1) % 4 = 0. Pause the video now and find as many values of n as you can that make this predicate true. Come back when you're ready. 

I've actually written a Python function here to help me find these. The predicate is here in this first block --- it just implements the process of returning TRUE if 3n+1 mod 4 is 0 and FALSE otherwise. Down below, I'm going to run a quick loop to go through the integers 1 through 30 to see which values make the statement true, and maybe I'll see a pattern. It looks like 1, 5, 9, 13, 17, 21... I believe I'm seeing a pattern here that whenever n is itself congruent to 1 mod 4, this predicate will be true. I'll test that out with some integers outside the range I showed you --- for example a negative integer, like -3. That's congruent to 1 mod 4, and sure enough my predicate is true. Or 400001 is 1 mod 4, and that also gives true. So while I can't literally list all of these values, I can put them together in one place and indicate the pattern like so. 

This collection, consisting of all the variable values that make the predicate true, is called the **truth set** of the predicate. For example for P(x) = x+5 = 12, the truth set is just the single number 7. For P(x) = x**2 >= 0, the truth set is the entire domain, the set of integers. For S(x) = the length of x is 7, the truth set is the collection of all strings that have length 7. 

You've learned a lot in this video: The differences between a predicate and proposition, the domain of a predicate, and the truth set of a predicate. In the next video, we'll come back to the idea of quantifying a predicate that we mentioned earlier --- that's taking a predicate and turning it into a proposition by making an assertion about how often the predicate is true. 

## 2.9

In the last video, we learned about predicates, which are like propositions but whose truth value depends on the value of an input variable. We mentioned briefly that there's a way of turning a predicate into a proposition with a definite, fixed truth value by making a secondary statement about how often the predicate is true. Let's dig into that concept some more. 

So here's the proposition we first saw in the last video: P(x) is the statement x+5 = 12 where the domain is the set of all real numbers. This again is a predicate not a proposition. This statement is neither true nor false as it is, because it has an undetermined variable in it. But let's form a new statement that's related to it: The statement "P(x) is true for all values of x". Now this statement is definitely FALSE because we know for a fact that P(x) is not *always* true. That is, we know that x+5 is not *always* equal to 12. In fact P(x) is only true for one and only one value of x, namely x = 7. So the statement "P(x) is true for all values of x" is definitely, knowably false. That makes it a proposition, not a predicate. 

Here's another secondary statement we could make from the original predicate: "P(x) is true for at least one value of x". Another way to say this is that P(x) is *sometimes* true. Now that statement is definitely TRUE because there *is* at least one value of x that makes P(x) true, and we even know what it is -- x = 7. 

So again, predicates by themselves don't have enough information to know whether they are true or false. We sometimes say that they are underdetermined because the variable prevents us from knowing the truth value. But when we make a secondary statement about *how often* the predicate is true --- for example "this predicate is always true" or "this predicate is sometimes true" --- these statements are propositions with truth values. We call this process **quantifying** the predicate. 

To approach computer science from a mathematical point of view we often have to make claims about patterns we see or algorithms we create and then give an explanation. Those claims often come in the form of quantified predicates. For example, in an earlier video we saw an algorithm that converts a base 10 integer to base 2. We did *not*, however, discuss whether this algorithm always works. Doing so, involves working with a quantified predicate. The predicate would say, "This algorithm applied to the integer n produces the correct binary representation". And what we'd want to know, and explain, is whether P(n) is always true. So this notion of quantifying a predicate is really at the heart of computer science in important ways. 

As we saw a moment ago, there's two ways to quantify a predicate. One, like in our example with the algorithm, is to claim that the predicate is always true. When we take a predicate P(x) and make the claim that P(x) is always true, this is called *universal* quantification. We have a special symbol for this that looks like an upside down A, which you can remember because this means "for all" x, P(x) is true. For example, if P(x) is the predicate x+5=12, then "for all x P(x)" is the statement that x+5 = 12 for all real numbers x, and that is a FALSE statement. 

Here are some more examples. Let Q(x) be the predicate x**2 >= 0. "For all x Q(x)" is the claim that x**2 >=0 for every real number x. And that's actually TRUE this time because we know from basic math that squaring a number always produces a result that's bigger than or equal to 0. 

Here's two more. R(x) is the predicate "The length of x is positive" where x is a string, and S(x) is the predicate the absolute value of x is negative where x is a real number. Pause the video and find the truth value of for all x R(x), and for all x S(x). 

So in these examples, both universally quantified statements are FALSE. It's not the case for every string x, the length of x is positive because there is such a thing as a string of length 0, namely the empty string. So for all x R(x) is false because we found what's called a *counterexample* --- a single example that shows us that R(x) is sometimes false, therefore not always true. Likewise for all x S(x) is false, because there's a counterexample there as well: In fact there are many, for example x = 1. The absolute value of 1 is 1, which is not negative, so S(x) is not always true. 

The other form of quantification we have is when we take a predicate and claim that it is *sometimes*, but not necessarily always true. For example if P(x) is x+5=12, then while this predicate is not always true, it is true for at least one value of x. A fancier way of saying this is that *there exists an x* that makes P(x) true. So this form of quantification, where we make a claim about the existence of at least one input value that makes the predicate true, is called *existential quantification*. We use a special symbol for this too, a backwards "E". So this notation means, "there exists at least one x such that P(x) is true". 

We saw that there exists x such that x+5 = 12, is a TRUE statement. (Remember the universally quantified version of that predicate was false.) If Q(x) is x**2 >= 0, then since this predicate is true *for all* x, it's certainly true for at least one x. 

Now you try it with the earlier predicates R(x) and S(x). Are the existentially quantified versions of those predicates true, or are they false? 

There exists x such that R(x), is TRUE this time because it is true that there exists at least one string that has a positive length. For example, the word "logic" has a positive length. But, the statement there exists x such that S(x), is false because there does not exist even one real number whose absolute value is negative. 

Here's a table summarizing what we've found in these examples. 

So in this video, you learned that taking a predicate and quantifying the variable turns it into a proposition with a truth value. And there are two ways to do this, universal or existential each of which has its own notation. You also learned that a counterexample can be used to prove that a universally quantified statement is false. The next video is going to look a little more at this idea of proving quantified statements are false by asking how do we negate a quantified statement. 

## 2.10 

The last video introduced the idea of quantification, which is what happens when we take a predicate, whose truth value can't be determined because of a variable, and then making a claim about whether that predicate is *always* true or *sometimes* true. Since quantified predicates are propositions, we can negate them. And in this video we're going to see how this is done. 

Take a look at the universally quantified predicates from the last video that were false. How did we know they were false? For example, why was "for all strings x, the length of x is positive" false? It was because we found a single example of a string that showed us that *not all* strings have a positive length. That's called a *counterexample* --- an example that proves a universally quantified statement is false. Universally quantified statements can be shown to be false by producing just one counterexample. 

We can phrase this fact using negations. If you take the universally quantified statement "for all x, P(x)" and negate it, it is a claim that P(x) is not universally true, or not *always* true. What does it mean when a statement is not always true? It *doesn't* mean that the statement is always false. For example the statement "All cars are red" is not  true. But this doesn't mean that *no* cars are red --- that no red cars exist. It just means that not all cars are red, or that there are cars that exist and are not read. 

So a when a univerally quantified statement, something of the form "for all x, P(x) is true" is negated, we are saying that P(x) is *sometimes* false. Or put differently, there exists an x that makes negation of P(x) true. We can put that in notation by saying: The negation of "for all x, P(x)" is "there exists an x such that 'not P(x)'". So the negation of a universally quantified predicate is the existentially quantitication of the negation of the predicate. 

Likewise, look at the existentially quantified predicates that are false, like the one you did in the last video, S(x) is the absolute value of x is negative. If we existentially quantify that predicate to get "there exists an x such that the absolute value of x is negative", that's a false statement because we know from basic math than the absolute value of x is never negative --- that is, the absolute value of x is always zero or positive. This sounds like a universal statement, doesn't it? In fact, what we see from this example is that the negation of "there exists an x such that P(x)" is "for all x, not P(x)". So negating an existentially quantified statement gives a universally quantified statement. 

Here's one more example to put it all together. Look at the predicate C(x) where the domain is the set of all countries on Earth, and C(x) says "the first letter of x is B". Pause the video while you do the following: First, write out in English or whatever language you prefer what the statements "for all x C(x)" and "there exists an x such that C(x)" would say in plain language. Then, determine whether those statements are true, or false. Then, write out their negations in plain language and determine whether those are true or false. Come on back here when you are ready. 

The universally quantified statement would say that Every country begins with the letter B. The existentially quantified statement would say that At least one country begins with the letter B. There are other possible ways to say either of these. But when you put it this way, it's clear that "For all x C(x)" is false, again because there are lots of counterexamples possible, for example France. And "There exists x such that C(x)" is true, because there do exist countries beginning with a B, like Belize or Belarus. 

The negation of "for all x C(x)" would be "There exists x such that not C(x)" which in plainer language would be "There exists a country whose name doesn't begin with a B". And that's certainly true, in fact this statement is just saying that it's possible to find a counterexample to the original universal statement. The negation of "there exists an x such that C(x)" is the universal statement "for all x, not C(x)" or in other words, For every on Earth, the name of the country does not begin with a B. That is a false statement, and we know it because that's a universal statement but there's a counterexample -- Belize, or Belarus. This makes sense because the negation of a proposition should have the opposite truth value. The universal statement was false so its negation should be true, and the existential statement was true so its negation should be false. 

You've learned in this video that the negation of a universally quantified statement is an existentially quantified statement using the negation of the original predicate. And likewise, the negation of an existentially quantified statement is an universally quantified statement using the negation of the original predicate. There's just one more topic to touch on here, and that's how quantification works when you have more than one variable. So stick around. 

## 2.11

You've done a lot of work so far with predicates. You've learned what they are and how they related to propositions, how to quantify them, how to negate them, and more! Great job so far. Our last video on this topic is going to expand things out a bit and look at predicates that have two variables instead of one. 

Let's let P(x,y) is the statement x*y is bigger than or equal to 0. To determine the truth value of this, we need the values of not just one but two inputs. For example P(2,3) is true and P(2,-4) is false. We saw in the last two videos that quantifying the variable turns a predicate into a proposition with a definite truth value. Does that work for two-variable predicates? 

Let's suppose we took P(x,y) and quantified the variable x by saying "for all x, P(x,y) is true". Unlike earlier, this is still an underdetermined statement because we've quantified the x variable but the y variable is still unknown. Quantifying the x variable turns a two-variable predicate with variables x,y into a one-variable predicate with variable y. It's still a predicate and unless we do something with the y variable too, we still can't determine its truth value. The general principle here is that for two variable predicates, *both* variables must be quantified before we can say anything definite about truth values. 

Let's keep the universal quantifier here on x. There are two ways to quantify the missing variable y --- universal or existential. If we universally quantify y, we would have this in notation --- for all x and for all y, P(x,y) is true. In plain language this would say that x*y is positive for every possible pair of inputs x and y. Now this statement has a definite truth value, namely FALSE because I can find a counterexample easily, for instance x = 2 and y = -4. So it's not the case that P(x,y) is true "for all" values of x and y. 

But we could also have existentially quantified y, to get this: for all x, there exists a y such that P(x,y) is true. Or in plain language, for every real number x, there is some other real number y such that x*y is positive. That statement also has a definite truth value, namely TRUE. Let's see why. Where you are sitting right now, pick any real number you like. Now no matter what number you picked, one of three things must be true about it: It's either negative, positive or zero. I will now tell you the "y" value that will make xy bigger than or equal to zero. If your "x" was positive, let y = +1. If your x was negative, let y = -1. If your x was zero, let y = 0 as well. In each possibility, x*y is bigger than or equal to 0. So no matter what x you chose, there is a y that makes P(x,y) true. 

What would happen if we had existentially quantified the x earlier instead of universally quantifying it? Well, we'd still need to quantify the y variable to end up with a fully determined proposition and there are two ways to do that. You could have: "There exists an x such that for every y, P(x,y) is true" and you could have "There exists an x such and there exists a y such that P(x,y) is true". Now pause the video and see if you can determine which, if either, of those statements is now true.

"There exists an x such that for every y, P(x,y) is true" is in fact a true statement. The statement is claiming that at least one x exists such that x*y >= 0 no matter what y you choose, and that's true --- can you guess what x it is? It's x = 0. If you choose that x, then xy >= 0 for every single y value. 

"There exists an x such and there exists a y such that P(x,y) is true" is also a true statement because I can certainly find an example of x and y where xy >= 0, for example x = 1 and y = 2. 

So given a two-variable predicate P(x,y) there are at least four possible ways to quantify it: one for each combination of quantification of x and y. Each has its own truth value that it's our job, as mathematicians, to explain why the truth value is true or why it's false. 

I say "at least" four truth values because in fact sometimes the ordering of the variables matters too. For example look at the predicate Q(x,y) is the statement that x*y < 1 where the x values are integers and the y values are nonzero real numbers. Look at the statements for all x there exists a y such that Q(x,y) and there exists a y such that for all x Q(x,y). You might think these statements are equivalent since all we did was change the ordering of the quantifiers. But look at each one. 

The statement for all x there exists a y such that xy < 1 is TRUE, and here's an explanation. Choose any integer x you like. If you chose an x that was zero or negative, set y = 1 and then xy < 1. If you chose an x that was positive, set y = 1/(x+1). Then xy is x/(x+1) and because the denominator is bigger than the numerator, the fraction is less than 1. That explanation, notice, does not depend on specific examples --- it works "for all" x. 

However the statement that there exists a y such that for all x, xy < 1... is a FALSE statement. I will explain why no such y exists. Suppose that we did have a y such that xy < 1 no matter what the x is. This y can't be 0 because 0 isn't in the domain. Given that fact, it's not the case that xy < 1 "for all" values of x, because there's a counterexample: x = 1/y. If x = 1/y, then xy = 1 and that's not less than 1. 

In other words, the order in which we place the quantifiers can sometimes matter! It takes careful mathematical reasoning to see when these statements are true and when they are false. But that's what this whole course is about, so it's good work. 

That brings us to the end of this module on logic. You're learning a lot, so congratulations! Our next module is about two more fundamental mathematical concepts that underlie computer science: The concept of the *set*, which is the model for all data structures in computer science, and the concept of the *function* which is the model for all programs. Pretty big ideas, in other words. See you there. 

https://math.libretexts.org/Courses/Monroe_Community_College/MATH_220_Discrete_Math
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTE3NjE5NzMzLDUyMTA3NjU3MCw1NDIzMD
Q0MTgsLTQ1MjYxMzIyNCwxNDEzMjM0NTA0LC0xOTQwOTMyNzQs
LTIwMTk0ODgxMTksLTE0NTkxMjMwMDcsLTUzMjk5OTY3OV19
-->