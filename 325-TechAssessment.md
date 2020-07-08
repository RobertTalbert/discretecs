# MTH 325: Technological Skill Assessment

## Overview

A large portion of the graded work you do in MTH 325, and a lot of the ungraded work, will use four items of technology that require some training:

+ The __Python__ programming language,
+ The __Jupyter__ notebook environment,
+ The __Markdown__ text formatting system, and
+ The __LaTeX__ (pronounced "LAY-tech") math typesetting system.

__On Monday, January 30, there will be a 50-minute in-class assessment in which you'll be asked to demonstrate that you have a reasonable amount of basic competency with these tools.__ This document describes what you'll be asked to do (and what you need to know), and how to go about learning it.

__Why we are doing this:__ In MTH 325, we use the computer as a tool for thinking about mathematical concepts related to graphs, relations, and trees. Could we learn these concepts without the computer? Yes, but,

1. By using computer tools to work actively with those concepts, they will stick better in your mind and you'll be better able to recall them than if you just heard someone talk about them.
2. By using computer tools, we will be able to work with larger and more realistic structures than if we were doing it by hand.
3. By using tools like Python and Jupyter, you'll be getting exposure to technology you can actually use in your careers once the course is over.

## What you will be asked to do on January 30

During the assessment period on January 30, you will be asked to bring your laptop and do the following:

+ _Create a new Jupyter notebook_ on your computer.
+ Using code cells inside that notebook, _carry out a selection of basic Python coding tasks_, such as constructing a `for` loop and working with a dictionary, taken from a combination of skills listed later on in this document.
+ Using a Markdown cell inside that notebook, _replicate a block of formatted text_ that you'll be given that contains bold and italicized text, bulleted and numbered lists, hyperlinks, headers, and mathematical notation.
+ Once done, you'll be asked to _export that notebook to PDF and HTML formats_ and then _upload_ the original Jupyter notebook, the PDF version, and the HTML version to a special place on our Blackboard site (that will be set up later).

__Note:__ If you do not have access to your own computer, please let me (Prof. Talbert) know as soon as possible so we can make alternate arrangements

## How the assessment will be evaluated

The technology assessment will be evaluated using engagement credits, using the following rubric:

+ _Was the Jupyter notebook created successfully?_ Yes = 1; No = 0.
+ _Was the Python portion of the assessment completed?_ Completed with no errors = 5; Completed with one or two minor errors = 3; Completed with one or two significant errors but with evidence of understanding = 2; Completed with several major errors = 1; Not completed = 0.
+ _Was the Markdown/LaTeX portion of the assessment completed?_ Completed with no errors = 3; Completed with one or two minor errors = 2;  Completed with significant errors = 1; Not completed = 0.
+ _Were the uploads present and correct?_ 1 engagement credit for each format (Jupyter, PDF, HTML) successfully uploaded without formatting errors.

Therefore if you do all of the above successfully, you will earn 12 engagement credits.

For the purposes of grading, **"Not completed" means that at least one of the tasks you are asked to perform was not attempted.** That is, if a student forgets to do a part, or chooses not to do a part, it will count as if the entire portion of the assessment was not attempted. You'll be reminded of this on January 30.

Note that because this is graded with engagement credits, having mistakes, or even missing this assessment entirely, will not have a directly adverse affect on your course grade, because you can always make up engagement credits through other activities. But, this is a golden opportunity to earn a big chunk of engagement credits, and if you're not fluent on these tasks then it will have a negative affect on your work later in the class, particularly on Challenge Problems.


Please note the following rules about this assessment:

+ You will _not_ be able to use notes or internet resources during this assessment. The tasks will be kept very basic, and you are expected to have thorough knowledge of those basics.
+ There are no revisions or retakes available for this assignment.
+ If you miss class that day, you will receive 0 engagement credits on it. Again, this does not hurt your grade directly, but it's a missed opportunity to earn engagement credits. (If you _must_ miss for an emergency, please consult with me.)

## What you will need to know specifically  

Here are the specific competencies that you will need to have learned before this assessment takes place. They are the basic building blocks of all future work we do with our technological tools in the course:

+ Python 3
    * Use the `print` command to print text or variables.
    * Add a comment to Python code.
    * Perform basic arithmetic (`+, -, *, \`)
    * Assign a value to a variable.
    * Concatenate two strings.
    * Create a user-defined function that accepts one or more variables and either `print`s or `return`s output.
    * Use logical operators to combine Booleans.
    * Use `==` to test for Boolean equality.
    * Write `if` and `if-elif-else` statements.
    * Write a Python list.
    * Use a `for` loop to iterate over a list.
    * Use a `while` loop to iterate relative to a condition.
    * Access an element of a list at a specific location using square-bracket notation (for example `a[3]`) and slicing (for example `a[3:7]`).
    * Use the `range` function to generate a list of integers.
    * Append items to a list and find the length of a list.
    * Write a Python dictionary.
    * Access the values associated to a key in a dictionary.
    * Construct a list using a list comprehension.
+ Markdown (text formatting)
    * Apply Markdown syntax to make text __bold__ or _italicized_.
    * Create ordered (numbered) and unordered (bulleted) lists.
    * Put text into a block quote.
    * Insert a code snippet inline and insert code blocks.
    * Create at least three levels of headers.
    * Insert hyperlinks.
+ LaTeX (mathematical notation)
    * Use the dollar signs to format basic mathematical expressions.
    * Insert variables and numbers that have exponents and subscripts.
    * Insert fractions in "vertical" format (for example $\frac{1}{2}$ as opposed to $1/2$).
    * Write sets using set brackets.
    * Insert Greek letters.
+ Jupyter
    * Create a notebook and change the name of the notebook.
    * Insert and delete cells.
    * Change a cell from Code to Markdown and vice versa.
    * Save (download) a Jupyter notebook in HTML, PDF, and `*.ipynb` formats and upload those files to Blackboard.

## How to learn what you need for the assessment

We will use class time on Friday, January 13 as an "install party" to make sure everyone has access to the Python and Jupyter resources they need, either as a download/install using the [Anaconda](https://www.continuum.io/anaconda-overview) platform or in the cloud using [SageMath Cloud](https://cloud.sagemath.com/) (or both), and then play with a basic Jupyter notebook. Also, any "Free Friday" between now and January 30 can also be used during class time to work on these skills.

However, _no other class time will be spent on training_ because different students will have greatly different needs. (Some people have programmed in Python since they were 8 years old, some are brand new to it, etc.) Instead, resources to help you learn have been created or curated, and here they are:

### To learn what you need to know about Python

Work through the free self-paced course on Python at CodeAcademy, which is located at:

>[https://www.codecademy.com/learn/python](https://www.codecademy.com/learn/python)

Note that you will need to create a (free) account at CodeAcademy for this, in order to save your work. You should just be able to log in with Google or another social media account.

The CodeAcademy course is divided into 13 "units", each unit consisting of a number of "lessons". _You do not need to work through all of the units and lessons in that course._ What you need to complete is:

+ **All lessons in Unit 1** ("Python Syntax") **through Unit 9** ("Exam Statistics"); and
+ **In Unit 10** ("Advanced Topics in Python"), **complete the first lesson** (which is also called "Advanced Topics in Python"). _You do not need to complete the other lessons in Unit 10_ ("Introduction to Bitwise Operators", etc.) unless you want to.

Also, note that _you do not need to complete any of the lessons that are designated as "Pro" or "Pro Trial"._ In fact you cannot even access those lessons unless you purchase a CodeAcademy subscription, and you are not required to do that for MTH 325.

__Estimated time to complete:__ The estimated time required to complete the CodeAcademy course is between _10 and 15 hours_. This might be less if you are fluent in Python already; if you are brand-new to programming, it could take more. If you split up the work so you are spending roughly 30-60 minutes per day starting in week 1, you will have no problem completing the course by January 30. __If you have already completed this CodeAcademy course in a past course or for self-learning, then see point #2 below.__

Please note two things about this CodeAcademy course:

1. __Completion of the CodeAcademy course is not required for the assessment__. It is merely a resource that provides, in a systematic and effective way, all the training you need to succeed on the assessment. I have used it before in MTH 225 and MTH 325 with uniformly positive results. However, if you have significant knowledge of Python already, or you have a different resource you want to use to learn, then you do not have to complete this CodeAcademy course. But, you will be responsible for making sure you have gained enough knowledge to succeed.
2. However, **students who complete the units and lessons listed above from the CodeAcademy course and who can provide evidence that they have completed these units and lessons will be exempt from the Python portion of the assessment on January 30** and automatically earn 5 engagement credits regardless of whatever else happens on the assessment. All you will be asked to do on January 30 is create the Jupyter notebook, do the formatted text tasks, and upload your results --- a process which will take significantly less time than if you also had to do the Python portion. Please note that __this evidence must be received by the start of your sections' meeting on January 30__; otherwise you will need to complete that portion of the assessment or receive 0 engagement credits on that portion.

To submit your evidence that you've completed the units and lessons from the CodeAcademy course, you can (1) bring your computer to class or office hours and show me your page or profile at CodeAcademy, or (2) send me a screenshot of your page or profile at CodeAcademy where your name and your progress on the assignment are visible in the same frame.

### To learn what you need to know about Jupyter, Markdown, and LaTeX

There are three tutorial videos on Blackboard in the _Tutorials_ area, in the folder _Prof. Talbert's Jupyter/Markdown/LaTeX tutorials_ folder. Watch all three of those, and work along with them inside your own Jupyter notebook. For further understanding of these tools, there are additional tutorials posted on Blackboard that you can use.


## If you have questions

For how-to questions on any of the above tasks, your best bet is asking those questions on the **#tech** channel on Slack. There, they will be seen not only by me but also your classmates and the students in the other section. If a question needs to remain private, use a direct message on Slack instead, or an office hours visit.

In terms of the academic honesty rules for the course, you can ask questions to each other about the CodeAcademy course that are general in nature, but you must work out specific solutions on your own. However, you can ask anything about Jupyter, Markdown, or LaTeX without worrying about academic integrity. In fact, a robust discussion of questions on these subjects would be valuable to everyone.

For housekeeping questions on the assessment itself or how it will be administered or graded, ask those in the **#tech** channel as well, or if it's private please use a direct message, an email, or an office visit to ask.
