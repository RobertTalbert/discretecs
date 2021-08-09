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

What that last condition in the recipe does, then, is CONNECT two logical propositions with the word "or", making a larger proposition. Each of the smaller statements is a proposition, and joining them with "or" makes another, larger proposition. We sometimes say that a proposition that cannot be broken down into a bunch of smaller ones is an "atomic" proposition, and a proposition that isn't atomic --- if it's made up of atomic statements joined by connectives --- is called "molecular". 

We frequently work with complex logical propositions that control the flow of information through a computer program. There are three basic forms of connectives that do this for us. 

Maybe we need some part of a computer program to activate if, like this recipe, any one condition from a list of conditions is true. We often see this use the English word "or". A statement created by joining two atomic propositions together with "or" is called a "disjunction". And a disjunction is true, whenever either one or both of the propositions it joins is true. For example: "Either I passed algebra, or I passed C++" is a disjunction. If you passed algebra but didn't pass C++, the disjunction is true because the first proposition is true. Same for if you didn't pass algebra but did pass C++. If you passed both, the disjunction is true because you passed one of these classes if you passed both. That makes our use of "or" into what we call an "inclusive or", so the "or" statement is true if either one OR BOTH of the atomic propositions involved is true. The only way a disjunction can be false is if both statements involved are false. For example if you did not pass either algebra or C++, this statement that you passed one or the other of them is false. 

One of the nice things about logic is that the content of the statements involved doesn't really matter, it's only the form. Any time you form a disjunction from two statements, the disjunction will be true if one or both of the statements involved is true. It doesn't matter what the statements *say*. So we sometimes just use a variable to represent the statements and then this v shaped symbol to represent "or". With those symbols, we can sum up how the disjunction works in this table. If either P or Q or both are true, then P v Q is true. Otherwise if both P and Q are false, P v Q is false. This is called a truth table and we will be using these a lot to understand propositions' truth values later. 

Sometimes we need a part of a program to activate if ALL of the conditions in a list are true. For example, to take discrete math you might need a passing grade in both algebra AND C++, not just one or the other. We use the word "and" and a symbol that looks like an upside down v to represent this connective, which we call a *conjunction*. In a conjunction of two propositions both propositions must be true in order for the conjunction to be true. That's summed up in the truth table for conjunctions which you see here. The conjunction is false otherwise --- that is, whenever one or both of the atomic statements that make up the conjunction is false. 

Sometimes we need a part of a program to activate if a single proposition is NOT true. THis is a connective called a negation, and we use this symbol to denote it. Negations are different than disjunctions or conjunctions because they only work on one statement --- if you have the statement P, then ~P is its negation. The negation ~P is true when P is false and false when P is true --- it's the logical opposite of the original statement. 

In this video you learned that we form complex logical statements out of atomic statements with connectives. We saw three basic connectives, "or" (disjunction), "and' (conjunction), and "not" (negation). And we learned about the concept of a truth table which allows us to see the truth values of a molecular statement as determined by the truth values of the atomic statements and by the connectives that join them. In the next video we'll look another connective, the conditional or "if-then" statement. See you there. 