# How to make your own practice exercises 

## Use the standard sources first: 

* [Your textbook](https://discrete.openmathbooks.org/dmoi4.html): Find the relevant section for the item you need to practice and use the interactive exercises found there. 
* Practice exercises from [Application/Analysis Homework](https://docs.google.com/document/d/1pCxYpwLsHa9ciZv4zrtCH2P3aEM6g6Za2onQsOJCung/edit?tab=t.0#heading=h.6eprh0moo8kg)
* [WeBWorK](https://webwork-math.gvsu.edu/webwork2/) sets 
* Past Learning Target Exams 

Also review the [Standards for Student Work document](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md), especially [this section](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md#standards-for-learning-targets) which details what you will be asked to do on each Learning Target and what constitutes "Success" on each. 

A lot of these practice activities involve "generating a positive integer" or pair of integers. You can do this yourself, or [use a random number generator](https://www.random.org/integers/). 


## Learning Target 1 

Generate two positive integers $a$ and $b$. Then: 

- Do long division to find the quotient and remainder. [Check work with this calculator](https://www.calculatorsoup.com/calculators/math/longdivision.php). 
- Run the Euclidean Algorithm to find the GCD. [Check work with this calculator](https://www.calculatorsoup.com/calculators/math/gcf-euclids-algorithm.php). 

Then generate several pairs of integers $a$ and $b$ and compute `a % b`. Check your work with Python or some other calculator. 

## Learning Target 2

Generate a positive integer in base 10. Then convert it to bases 2, 8, and 16 using the base conversion algorithm by hand. [Check your work here](https://www.rapidtables.com/convert/number/base-converter.html). 

To go the other direction, take your results from the first step and convert them back to base 10. You should get the number you started with. Or, generate a random integer and use the calculator linked above to convert it to base 2, 8, or 16 and then convert that number back to base 10. 

## Learning Target 3 

Generate several binary (base 2) integers. For addition, the integers should be 6-10 bits. For multplication and division, one of them should be 6-8 bits and the other 2-3 bits. Then perform addition, subtraction, multiplication, and division. [Check your work here](https://www.calculator.net/binary-calculator.html). 

## Learning Target 4 

Make up a conditional statement in English: *If* (condition), *then* (conclusion). Then write the converse, contrapositive, and negation of the statement. Use an AI tool to check your work: Prompt the AI with the original statement and ask it to provide the converse, contrapositive, and negation.

## Learning Target 5 

Make up, or look up, a logical proposition in symbolic form, using either two variables or three. Then write the truth table by hand. [Then check your work here](https://web.stanford.edu/class/cs103/tools/truth-table-tool/). Remember to show all the intermediate columns, which this tool does not do. 

## Learning Target 6 

Make up, or look up, an example of a predicate with 1-3 variables in it. Then add some quantifiers to it and identify the free and bound variables. Then prompt an AI with your quantified predicate and check your work. [Here is an example of a chat session with ChatGPT that shows how this might go](https://chatgpt.com/share/67d83c79-c9e8-8005-b589-891982535de4). 

For the other parts of this Learning Target: Create a predicate with one variable and quantify it with both universal and existential quantifiers. The resulting expression is a logical proposition; determine its truth value. You'll need to specify the domain of the predicate; when in doubt use the set of natural numbers. Check your work with an AI tool. [Here is an example](https://chatgpt.com/share/67d83e17-57e4-8005-a107-0db2ffadb4d8). 


## Learning Target 7 

Create a rule of deduction by searching one up, or just making your own by listing 2-3 premises and a conclusion. Determine whether the rule is valid or invalid by using a truth table. [Then check your work here](https://web.stanford.edu/class/cs103/tools/truth-table-tool/). Note, you will need to know the basic concept of how to tell if a rule of deduction is valid or invalid using a truth table. 

For the other part of this Learning Target: Create two logical propositions with 2 or 3 variables, either searching some up or making them up from scratch. Use a truth table to determine if they are logically equivalent. [Then check your work here](https://web.stanford.edu/class/cs103/tools/truth-table-tool/). Note, you will need to know the basic concept of how to tell if two statements are logically equivalent using a truth table.


## Learning Target 8 

Generate or search up some examples of recurrence relations. You can find examples in the class notes and past exams, or searching for "recurrence relation examples", or using an AI tool to make some for you. Then use it to generate the first 5-7 terms of the sequence. Check your work with a calculator, Python, or AI. 

## Learning Target 9 

Search for propositions that are proven by induction. You can find examples in the class notes and past exams, or searching for "proof by induction examples". Then write out the framework: The base case, the inductive hypothesis, and the inductive step. Remember you will be asked to *prove* the base case, not just state it; but you won't be asked to provide a complete proof. Then use an AI tool to check your work, or look for a completed proof and identify the parts of the framework in that proof. [Here is an example of the latter](https://shottr.cc/s/1LX2/SCR-20250317-h1up.png). 

## Learning Target 10 

Write out a set in set-builder notation, then convert it to roster notation. Make sure the syntax of the set-builder notation is correct. You can use an AI tool to check your work, [like this](https://chatgpt.com/share/67d8421e-7678-8005-aa63-0093037e73e1). 

You will also be asked to determine if a particular object is an element of a set or not, or if a particular set is a subset of a set or not. Generate a set and an object, then determine if the object is an element of the set. Generate two sets and determine if one is a subset of the other. Check your work with an AI tool, [like this](https://shottr.cc/s/1mL2/SCR-20250317-haep.png). 


## Learning Target 11

Make up examples of small (10 elements or less) sets and perform the following operations: Union, intersection, set difference, and Cartesian product. Check your work with an AI tool, or Wolfram|Alpha. [Here is an example of how to do this with Wolfram|Alpha](https://www.wolframalpha.com/input?i=%7B1%2C+2%2C+3%2C+4%7D+union+%7B2%2C+3%2C+4%2C+5%7D). 


## Learning Target 12

Make up examples of mappings using this webpage (which is what is used when making up the actual problems on Learning Target exams). Determine whether each one is a function. If a mapping is a function, determine if it is injective, surjective, or bijective. To check your work, the webpage outputs a key (scroll down to see it) that shows which ones are functions. To determine whether a function is injective or bijective, write out the function using function notation first. For example [this function](https://shottr.cc/s/1Fcd/SCR-20250317-hg4p.png) could be written as: $f(4) = 2$, $f(3) = 4$, $f(2) = 0$, $f(9) = 1$, $f(8) = 1$. Then use an AI tool to check your work, [like this](https://chatgpt.com/share/67d84558-ff18-8005-b7fd-5608b6c3b69c). Note, you'll need to specify the codomain.  


## Learning Target 13

The best source of practice problems for this Learning Target is the combinatorics WeBWorK set and your textbook. To find more, do a web search for "basic combinatorics practice problems with solutions". 

## Learning Target 14

To compute binomial coefficients: First memorize the closed formula, $\binom{n}{k} = \frac{n!}{k! (n-k)!}$. Then generate a random pair of integers $n$ and $k$ and compute $\binom{n}{k}$ by hand. Check your work with Python or some other calculator.

To compute the number of permutations of a set: Generate a set of 4-6 elements and compute the number of permutations of the set. Check your work with Python or some other calculator or by actually listing out all the permutations.

## Learning Target 15

Generate, or search up, an integer sequence and use the concepts of the course to determine if it is arithmetic, geometric, or neither. Then generate the first 5-7 terms of the sequence. If it is either arithmetic or geometric, use the concepts discussed in class to write a recurrence relation and a closed formula for the sequence. Check your work by taking your proposed formulas and generating the first 5-7 terms of the sequence, and make sure that they agree with the sequence you started with. 

To get practice just on the formula-making part of this target, create or search up a sequence that you know is arithmetic, or that you know is geometric, and create the recurrence relation and closed formula, and then check work by generating the first 5-7 terms of the sequence and checking that they agree with the sequence you started with.  