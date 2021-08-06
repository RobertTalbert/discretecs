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

So these are the propositions here because they all have definite, knowable truth values. The others are not. This one is an interjection, this one is a question and neither of these have truth values. This one is not even a complete sentence. And this one, like the x+5=12 above, is underdetermined --- it's true for some values of the variable and false for others, so its truth value depends, which makes it not a proposition. 

In this video, you learned about what logic is and why it's important for computer science, what a proposition is, and how to tell the difference between propositions and non-propositions. In the next video, we'll look at some basic ways to build complex logical propositions out of simple ones using connectives. 