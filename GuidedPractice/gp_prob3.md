# MTH 225 Guided Practice Probability 3: Random variables

## Overview

We've learned about the rules for probability and how uncertain events can be quantified. In this lesson we'll take a look at a further means of quantifying uncertainty through the concept of a _random variable_. This is a function, whose domain is the sample space of an experiment and whose codomain is the set of real numbers -- so it's a function that assigns probabilities to events. Of particular interest to us is a random variable called the _binomial distribution_ which is a way of assigning probabilities to experiments that have two possible outcomes. (Such an experiment, like flipping a coin or guessing on a true/false exam, is called a _Bernoulli trial_.) 

## Learning objectives

__Basic objectives__: Each student is responsible for gaining proficiency with each of these tasks _prior_ to engaging in class discussions, through the use of the learning resources (below) and through the working of exercises (also below). 

+ Determine whether an experiment is or is not a Bernoulli trial. 
+ Given an experiment that is a Bernoulli trial, and given the probability $p$ of "success", write out the binomial distribution $b(k: n,p)$ that gives the probability of $k$ successes in $n$ trials and then calculate the probability of attaining $k$ successes in $n$ trials. 

__Advanced objectives__: The following objectives are the subject of class discussion and further work; they should be mastered by each student _during_ and _following_ class discussions. 

+ Apply the binomial distribution to determine probabilities in applied settings that use Bernoulli trials. 

## Learning resources 

In Section 6.2 of the Rosen _Discrete Mathematics_ text, read starting on page 406 at the subsection "Bernoulli Trials and the Binomial Distribution" and continue through page 413, stopping at the subsection "The Probabilistic Method". Note that most of the second half of this reading are examples that describe applications of the math concepts from the first half and several of those examples are of interest to computer scientists. 

Important notational note: The notation $C(n,k)$ is the same thing as $\binom{n}{k}$. 

You are again encouraged to use [Perusall](http://app.perusall.com) to do your reading, since you can leave comments and questions in the text and help others out as well. Please see previous Guided Practice assignments and Blackboard announcements for instructions. 

Useful video resource: 

+ [The Binomial Distribution](https://www.youtube.com/watch?v=xNLQuuvE9ug) (6:45)


## Exercises

The following exercises are to be done _during_ and _following_ your reading. Work these out on paper and then enter the responses into the appropriate submission form (see Submission Instructions) by the deadline. You will receive a mark of __Pass__ if each item response shows a good-faith effort to be right and is submitted prior to the deadline. 

1. At the submission form is an item that lists a few different kinds of experiments (i.e. random events). Check all of the ones that would be classified as Bernoulli trials. 
2. (Review) Compute the quantity $C(10,6)$ and leave your answer in the blank at the submission form. 
3. The reading defines the binomial distribution to be a function that assigns outcomes of a Bernoulli trial to the probability of that outcome happening. The function accepts three inputs: $k$ (the number of successes in the experiment), $n$ (the number of trials performed), and $p$ the probability of success and its output is $C(n,k)p^k (1-p)^{n-k}$. (The book uses the variable $q$ to represent $1-p$.) Use this formula to find the probability that when a fair coin is flipped 5 times, you will get tails 3 of those times. 
4. Pick one of the applications mentioned in the second half of the reading that caught your attention, and describe how probability is used in the application. 

## Submission instructions

Submit your responses using the form at this link: [http://bit.ly/1M8UKSj](http://bit.ly/1M8UKSj)

Note that although you can provide specific mathematical questions as always on this form, you're encouraged to use Perusall to ask questions because you might get more immediate help from classmates this way. 