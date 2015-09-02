# MTH 325 Guided Practice 7.3a: Compositions of Functions

## Overview

We've learned about functions as well as what it means to be an _injective_ or _surjective_ function. We continue this thread by looking at _operations_ on functions, starting with _composition_ in the next lesson. We've met the idea of composition before when we talked about composing two _relations_ together -- we look for "common elements" that relate elements in one set with elements in another. Composition of functions is similar in that it looks at "chaining" two functions together to accomplish multiple tasks. Of particular interest to us is how composition works; how composition affects injectivity and surjectivity; and what composition looks like in computer science. 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ Given two functions, determine whether their composition can be formed. If it can be, then find images of points under the composition. (Includes the use of correct composition notation.)
+ Find the power of a function. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Draw conclusions about injectivity and surjectivity of compositions based on knowledge of injectivity/surjectivity of the functions involved. 

## Learning resources 

To gain proficiency in the learning objectives, use the following resources. You may include other resources if you wish, in addition to or in replacement of the following. 

__Textbook__: In _ADS_, read Section 7.3, just the portion starting at "Composition" and continuing through the definition of "Powers of Functions". Make sure to read actively, working through examples and activities as you go. 

__Video__: Watch the following videos:

+ [Composition of functions](https://youtu.be/S4AEZElTPDo) (8:00)

## Exercises

The following exercises are to be done _during_ and _following_ your reading and viewing of the resources. Work these out on paper and then enter the responses into the appropriate submission form (see Submission Instructions) by the deadline. You will receive a mark of __Pass__ if each item response shows a good-faith effort to be right and is submitted prior to the deadline. 

1. Consider the functions $f: \mathbb{R} \rightarrow \mathbb{R}$ and $g: \mathbb{R} \rightarrow \mathbb{R}$ given by the formulas $f(x) = \sqrt{x}$ and $g(x) = \lfloor x \rfloor$. Calculate $(f \circ g)(10)$ and $(g \circ f)(10)$. Give your answer in the submission form and be sure to label which is which. Are they equal? Is composition of functions "commutative" (like multiplication and addition are commutative, i.e. the operation can be done in any order)?
2. Function composition is especially useful in programming because we can create small, single-purpose functions (in the form of programs) and then chain them together via composition to create more complex code. Consider the following functions (borrowed from the language [Haskell](https://www.haskell.org/)) that operate on lists of integers. Assume that lists are nonempty. 

+ `max`: Takes a list and returns the largest element in the list. 
+ `prod`: Takes a list and returns the product of the elements in the list. 
+ `head`: Takes a list and returns the first element of the list. 
+ `init`: Takes a list and returns all the elements of the list except the last one.
+ `len`: Takes a list and returns its length. Example: `len([4,5,6])` returns the number 3. 
+ `reverse`: Takes a list and returns a new list that is the original list written in reverse order. 
<!-- >`last`: Takes a list and returns the last lement of the list. 
>`tail`: Takes a list and returns a new list consisting of all elements except the head. For example, `tail([4,5,6])` returns the list `[5,6]`. 
>`min`: Takes a list and returns the smallest element in the list.  -->

Let `gpList = [3, 6, 8, 1, 2]`. Calculate the compositions (`len` $\circ$ `reverse`)(`gpList`) and (`reverse` $\circ$ `init`)(`gpList`). Be sure to say which is which. 

3. At the submission form, there are several compositions of the functions given in question 2. Not all of these compositions make sense, though, because some cannot be computed. Check all the compositions that _can_ be computed. Since we can't use the $\circ$ symbol on the submission form, we will substitute the period (`.`) to denote composition. For example `max . prod` means `max` $\circ$ `prod`. 
4. There's no reason we have to stop at composing just two functions. We could compose as many as we like to make highly sophisticated code. Consider the function `sort` which takes a list and sorts its elements from smallest to largest. (For example `sort([3, 6, 8, 1, 2])` returns `[1,2,3,6,8]`.) Explain in English what the following multi-part composite function does: 

> `init` $\circ$ `reverse` $\circ$ `init` $\circ$ `sort`


## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1VuXZrl](http://bit.ly/1VuXZrl)