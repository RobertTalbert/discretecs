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

All conditional statemnts obey the same rules of truth --- cleaning rooms and getting ice cream are just details. In ANY conditional statement, say "If P, then Q", the truth table would look like this: 

First of all if both the hypothesis and conclusion are true, then the conditional statement is true. If the kids clean their room and we then get ice cream, I've kept my promise. If you speed and then you get a ticket, the law has been enforced properly. And if the hypothesis is true and the conclusion is false then the conditional statement is false. If the kids clean their rooms but I back out of getting them ice cream, I have not kept my promise. If you speed but do not get a ticket, the law has not been enforced properly. 

If the hypothesis is false, then if the conclusion is true OR if the conclusion is false, the conditional statement is still true. If my kids don't clean their rooms, I'm not breaking my promise if I get them ice cream anyway, and I'm also not breaking the promise if I don't. 

So this is what the completed truth table for a conditional statement looks like. Conditional statements in other words are always true except in this one situation where the condition is met but the action doesn't follow. 

In this video we learned a new connective, the if-then construction which makes a conditional statement. YOu learned that the condition is called the hypothesis and the action that follows is the conclusion. You also learned the truth table for a conditional statement and that conditional statements are always true except when the conclusion does not follow from the hypothesis. In the next video we're going to look some more at conditional statements particularly at variations on the basic if-then construction. 

## 2.4

