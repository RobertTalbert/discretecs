# MTH 325 Guided Practice 7.3b: Inverse Functions

## Overview

In the last lesson we looked at _compositions_ of functions, where we take two (or more) functions that have "compatible" domains and codomains and chain them together into a larger function. This lesson looks at a related issue: Is it possible to take a function and chain it to another so that the resulting composition is the _identity_ function, that is, the function that does nothing to the input? The second function in this case would "cancel out" the effects of the first one, making it an _inverse_ for the first function. In this lesson we first look at what it means for two functions to be _equal_ and then find some conditions under which the inverse of a function must exist, and we'll also think about what inverses of functions must look like. 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ Determine whether two functions are equal. 
+ State the definition of the _identity function_. 
+ Given two functions, determine if one is an inverse for the other. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Determine whether a function has an inverse or not; if it does, find images of points under the inverse. 

## Learning resources 

To gain proficiency in the learning objectives, use the following resources. You may include other resources if you wish, in addition to or in replacement of the following. 

__Textbook__: In _ADS_ section 7.3, read the definition of _equality of functions_ (at the beginning) and then read from the subsection on "Identity Function" to the end. In particular, the _Mathematica Note_ is a useful example (even though we do not know the language _Mathematica_). 

__Video__: No videos this time. 

## Exercises

The following exercises are to be done _during_ and _following_ your reading and viewing of the resources. Work these out on paper and then enter the responses into the appropriate submission form (see Submission Instructions) by the deadline. You will receive a mark of __Pass__ if each item response shows a good-faith effort to be right and is submitted prior to the deadline. 

1. Consider the following two functions: $f: \mathbb{Z} \rightarrow \mathbb{R}$ given by $f(x) = x^2$, and $g: \mathbb{R} \rightarrow \mathbb{R}$ given by $g(x) = x^2$. Are these two functions equal? State your answer and explain your reasoning briefly. 
2. Consider the functions $h: \mathbb{R} \rightarrow \mathbb{R}$ given by $h(x) =  x^3 + 5$ and $k: \mathbb{R} \rightarrow \mathbb{R}$ given by $k(x) = \sqrt[3]{x-5}$. Find a formula for the compositions $h \circ k$ and $k \circ h$. What does this mean about the functions $h$ and $k$? 
3. Inverse functions are important in computer science because they "undo" operations that functions (i.e., programs) do. Below are three functions that  operate on _strings_ (that is, sequences of characters like `helloworld` or `ajs93ja++fZZ`). That is, they are fuctions from the set of all possible strings to itself. For each of these, determine if the function is injective, surjective, both, or neither; if the function has an inverse; and if so, what would that inverse function do. At the submission form there are three subquestions for each of these functions. 

+ `firstthree` -- Takes a string and returns the first three characters in the string. Example: `firstthree('HelloWORLD872')` returns `Hel`.
+ `lowercase` -- Takes a string and converts it to all lowercase. Characters in the string that are not letters or which were already in lowercase are left alone. Example: `lowercase('HelloWORLD872')` returns `helloworld872`. 
+ `switchcase` --  Takes a string and converts all lowercase characters to uppercase and vice versa. Characters in the string that are not letters are left alone. Example: `switchcase('HelloWORLD872')` returns `hELLOworld872`. 

## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1NXlzeh](http://bit.ly/1NXlzeh)