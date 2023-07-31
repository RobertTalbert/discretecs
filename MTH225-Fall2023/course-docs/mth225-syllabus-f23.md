# MTH 225: Discrete Structures for Computer Science 1

![](mth225-banner.jpg)

>Let us change our traditional attitude to the construction of programs: Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to human beings what we want a computer to do.
>-- Donald Knuth, *Literate Programming*

## About MTH 225 and this syllabus

**Welcome to MTH 225!** I'm Dr. Robert Talbert, the professor of this course. I'm grateful you're here. 

In this course, you will learn **the math that all of computer science is based on**. You'll learn things like how to do arithmetic in binary, how to count the number of ways to deal a five-card poker hand, and how to generate complex data structures using simple rules involving recursion. And more! By studying discrete structures, **you'll gain a superpower to make you an expert learner** of any hardware and any software, including those that haven't been invented yet. As a computer scientist, your ability to learn new things quickly, and use fundamental concepts to model complex ideas, are more valuable than your coding skills. 

**This syllabus contains all the information you need to navigate the course.** The main document will be kept continuously up to date at this link. When you see blue- or purple-underlined text in the syllabus or any other document, it's a clickable link. For example, [click here for a cat video](https://www.youtube.com/watch?v=aFuUidBR1aQ). A PDF version of the syllabus will also be available on Blackboard in the *Syllabus and Calendar* area, but it will not be updated unless there is a major change. 

**This document is meant to be read once, then searched as needed.** If you need to find something, the easiest way is to pull up this  document, hit `Control-F` and then do a search for the text you're looking for. 

All course materials for MTH 225 are available on GitHub at https://github.com/RobertTalbert/discretecs. Critically important documents (syllabus, etc.) will also be on Blackboard. 

## Key Information

**Meetings:** Section 03 and Section 04 meet Monday/Wednesday/Friday in Mackinac Hall B-1-110. Section 03 meets 12:00-12:50pm and Section 04 meets 2:00-2:50pm. 

**Student drop-in hours:** TBD

**Blackboard, Class Page, and Class Vault:** Our main course portal is on Blackboard, which you can access at http://lms.gvsu.edu. Please note that we are using *Blackboard Ultra*, a major update to Blackboard which has significant differences from previous versions. If you need a tutorial on how to navigate Blackboard Ultra, **LINK NEEDED**. We use two other electronic resources for the class: the **Class Page** (click here to access **LINK NEEDED**) which is a Google Doc showing notes and resources for class meetings; and the **Class Vault** ([click here to access](https://publish.obsidian.md/mth225) which serves as our primary textbook. All of these are linked together, so you don't need to remember them all. 

**Contacting the prof:** Email (talbertr@gvsu.edu) is preferred. You can schedule a video or phone call outside of office hours through [my Calendly page](https://calendly.com/robert-talbert/). Be sure to read my availability/response policy **LINK NEEDED**

**Course calendar:** The official course calendar is in Google Calendar. **LINK NEEDED**. linked on the [Class Page](https://hackmd.io/@rtalbert235/HyTuIxi4q) and on Blackboard. *In case of a date conflict on assignments or course documents, the Class Calendar is assumed to be correct.* 

**Definition of "week":** In our course, a "week" is defined to begin at 12:01am ET on Monday and end at 11:59pm ET the following Sunday. 

**Course content and videos:** There is no formal textbook for this course. The content for the course is at the Class Vault (https://publish.obsidian.md/mth225). A *optional* additional textbook is [Discrete Mathematics: An Open Introduction](http://discrete.openmathbooks.org/dmoi3/dmoi.html) by Oscar Levin. It's free; just click the link. A PDF copy is available for download [here](http://discrete.openmathbooks.org/pdfs/dmoi3-tablet.pdf). Not all course material is included in this textbook, and we may not follow the exact sequence that this book uses. But you are free to use it as a supplement. A playlist of instructional videos is available on Vimeo at https://vimeo.com/showcase/8667148, and individual videos are embedded in the class vault. 

**Course tools:** We will use [Miro](http://miro.com) (an online whiteboard tool) for class work and other purposes. You will also be using Juypyter notebooks on the [Google Colab platform](https://colab.research.google.com/) throughout the course. You'll receive some training on these tools in the first week of classes. 

**Technology:** For our class, you should have access to a laptop (a tablet is acceptable but not recommended) and a high-speed internet connection. You are *strongly encouraged* to have a device with a touchscreen and stylus input, or an external drawing pad, for handwritten work at an online whiteboard. If technology access is an issue for you, please let me know so we can discuss your options. 

## How to have an good experience in MTH 225

**I want you to be successful in this class.** This is my #1 priority as a professor at GVSU. Everything in MTH 225 is built to lead you toward having a deep learning experience that is also deeply enjoyable. My goal is to challenge you and support you in equal measures, so you'll learn a lot and have a great experience in the process. 

In MTH 225, you can expect:

- A learning environment that challenges you, but also where support is readily available and freely given. 
- Work that is meaningful and not "busy work", and grading practices that prioritize growth and improvement. 
- Transparency and openness in how the course is run, including clear instructions on what you need to do and when, prompt and helpful feedback on your work, and timely replies to messages and questions. 
- Openness to your ideas about the course, with regular solicitations for feedback that are taken seriously through a continuous improvement process. 
- Above all, **respect** -- for you as a learner, as an adult, and as a human. 

Success in MTH 225 is within everyone's reach, but it's not effortless. On your end, your success in the course depends on three things: 

1. **Active engagement during class time**. The best  way to learn anything is to be an active participant in the process. Students who approach the class with a passive mindset typically struggle, and often fail. Those who approach it with an active mindset, on the other hand, often surprise themselves with how much and how well they learn. Make it a priority not to just attend and take notes, but *get involved*. 
2. **Asking questions**. The material in MTH 225 is challenging, and you will almost certainly be lost, confused, and/or stuck at times. **This is not a defect -- it's normal and it means you're doing the course right.** When struggle happens, don't wait for things to make sense on their own: *Ask questions* of me and your classmates and take action to make sense of the material. 
3. **Good management of time, tasks, and information.** Understanding the material won't help you if you procrastinate, skip announcements, or don't use a calendar. All course information will be clearly laid out for you, but it's up to you to import that information into your own lives and act on it. 

If you can commit to these three things, then I have every expectation that you'll succeed in the course, no matter what your math background or perceived math skill is.

## Goals and Structure 

The overall goal of MTH 225 is to **build a solid foundation in the basic theory and tools for the mathematics that computer science is built on**, especially the theory and tools you will need for later coursework such as MTH 325 and CIS 263. 

### Course-level learning objectives:

Upon completion of MTH 225, you will be able to: 

* Represent integers using different number bases, and perform integer arithmetic using different bases and modular arithmetic.
* Formulate, manipulate, and determine the truth of logical expressions using symbolic logic.
* Formulate and solve computational problems using sets and functions.
* Formulate and solve complex counting problems using computational thinking and the tools of combinatorics.
* Evaluate numerical and other sequences using recursion, and solve simple recurrence relations.
* Write clear, correct, and convincing arguments to explain the correctness of a solution using combinatorial proof and mathematical induction.
* Explain the reasoning behind solutions to computational problems clearly to an appropriate audience.
* Apply effective problem-solving skills in solving computational problems.
* Apply computer programming and computational thinking to frame and solve mathematical and computational problems.
* Self-assess your work and apply feedback from others to make improvements in that work.

### Course module structure

The course content is split up into five modules:

- **Module 1: Computer arithmetic**. Representing integers in binary, octal, and hexadecimal; binary arithmetic; two's complement notation for negative integers; the Division Algorithm and modular arithmetic. 
- **Module 2: Logic**. Logical propositions, conditional statements, truth tables, predicates, and quantification. 
- **Module 3: Sets and functions**. Set notation and representation, set operations, functions. 
- **Module 4: Combinatorics**. The Additive and Multiplicative counting principles, the binomial coefficient, permutations, dots-and-dividers counting methods; using computational thinking to solve combinatorics problems. 
- **Module 5: Recursion and induction**. Numerical sequences in closed-formula and recursive forms, solutions to recurrence relations, the Principle of Mathematical Induction and proof by induction. 

The basic skills that you'll learn in the course are encapsulated in a list of **15 Learning Targets**, eight (8) of which are labelled as **CORE** targets and represent the essential skills that every MTH 225 student should possess by the end of the course. You can find that list in Appendix A(link needed), and it's linked elsewhere on our various course sites. 

## MTH 225 Workflow 

Each class meeting has activities for you to do *before*, *during* and *after* the class. For details on specific assignment types, see the next section. 

* **Before class:** You'll be asked to complete a **Class Prep** assignment that will involve you in reading content from [the course vault](https://publish.obsidian.md/mth225/) and watching some of the videos at [our playlist](https://vimeo.com/showcase/8667148). You'll complete a small set of basic questions and exercises on a Google Form. This way, you'll come to class ready to work, and we can skip the lecturing in class unless it's really needed. 
* **During class:** Class meetings will be focused on *answering questions* and *doing active work*, both intended to make it easy for you to make sense of the material and ask questions. Selected portions of your class work will be written up individually and turned in as **Application/Analysis** sets. We'll also use time in class for assessment and for completing other assignments, so that a lot of the "homework" for the class is done during class time. 
* **After class:** In addition to getting started on the next Class Prep, you should expect to spend significant time in between classes doing practice on concepts you don't fully understand yet, and asking questions. There will be occasional **Application and Extension Problems** (AEPs) to work on. 

A typical week in MTH 225 looks like this: 

(visual here)

Sunday - Complete Class Prep for Monday 
Monday - Q&A from Class Prep and active work on more advanced concepts from Class Prep 
Tuesday - Complete Class Prep for Wednesday 
Wednesday -- Q&A from Class Prep and active work on more advanced concepts from Class Prep 
Thursday - Complete Class Prep for Friday 
Friday -- Q&A from Class Prep and active work on more advanced concepts from Class Prep 
Saturday -- Nothing (If you stay current on work during the week you shouls always have Saturday open)

## Assessments and Grades

### Overall approach to grades in MTH 225 

The way grades work in MTH 225 is different from what you might have experienced. In MTH 225: 

- **Almost none of your assignments have point values**. In fact only the final exam is graded with points. Therefore there is **no partial credit and no averaging**. 
- Instead, assignments have **specifications** which are descriptions of what constitutes "acceptable" work. These are given in detail in the document *Standards for Student Work* which you can find on Blackboard in the *Syllabus and Calendar* area. When you submit an assignment, I will read it carefully and compare it with the standards, and simply determine whether it meets the specifications or not. Typically your work is marked either **Success** or **Retry** depending on whether it meets the specifications or not. 
- After I evaluate your work, in most cases you will receive **detailed feedback** that will tell you whether your work meets the standards, and if not, the feedback will tell you what was missing and how you might go about fixing it. 
- Then, on almost every piece of work, you will have the chance to **retry** the assignment if needed, get more feedback, and repeat this **feedback loop** until the work meets our specifications. 
- Your course grade is not based on point totals or averages (because there are no point values). Instead, the course grade is based on **how many important learning tasks you've successfully accomplished** by the end of the semester, using a simple table that's given below. 

Therefore grades in MTH 225 are based not on your ability to do good work at a single point in time, but rather on your ability to **eventually learn the material** by acting on feedback from previous attempts. 

This process, using specifications and feedback loops rather than points and averages, is how evaluation of work happens in most situations outside of college. In your future jobs, for example, you'll be reviewed regularly by your manager; it's not a "one and done" situation where you get a point score and then the process is over. Instead, in a real job, you get feedback and coaching on how to improve, and then you act on the feedback and show the boss that you have improved. 

I've been using this grading method since 2017, originally in MTH 325 and now in all my classes. We do things this way because **learning takes time**, and I believe grading your work based on a single point of data such as a quiz or test and then averaging all of those data is not only inaccurate, but statistically invalid and even unethical. Feedback loops are how all human learning takes place. So this seems like the best way to do grading. 

Those are the main concepts; the details are in the rest of the syllabus. Most students need a week or two to adapt to this system, but then everything is fine. I encourage you to ask questions at any time so I can help you. 

### How you will be assessed 

There are five major kinds of assignments in MTH 225: 

- **Class Prep:** These are done prior to class and will give you the basic knowledge of terms, ideas, and basic concepts that will allow us to jump right into applications when we get to class. They involve reading articles from the class vault (and occasionally watching video), engaging in asking questions about what you read, and answering some simple questions about the content. 
- **Application and Analysis:** In class, we will work in groups on higher-level tasks involving application and analysis of the basics. You'll be responsible for individually completing selections from this work that you start in groups during class, and turning it in to be checked for basic overall correctness. 
- **Skill Quizzes:** Each week (typically) we'll take time in class for a timed quiz over a subset of the 15 Learning Targets found in Appendix A. 
- **Application/Extension Problems (AEPs):** These are longer-form problems that involve deeper applications of the concepts from class, on applications in a variety of domains and in problems whose solutions require computer tools and good technical writing. 

Each of these assignments is graded as follows: 

| Assignment | Basis for grading | What's recorded on Blackboard | 
| :---------: |  :---------: |  :---------: | 
| Class Prep | Completeness and effort only | *Success* or *Incomplete* | 
| Application/Analysis | Completeness and overall correctness | *Success*, *Retry*, or *Incomplete* | 
| Problems on Skill Quizzes | Overall correctness | *Success* or *Retry* | 
| AEPs |  Completeness, overall correctness, writing, and presentation | *Success*, *Retry*, or *Incomplete* | 

[The Standards for Student Work document](link needed) contains details on the quality standards for each kind of assessment in the course. Please read this carefully and review before each submission you make. 

### More about Learning Targets

The 15 Learning Targets given in Appendix A are the core basic skills of MTH 225. They are not the only thing that matters in the course; but part of your job in the course is to **demonstrate skill on as many of these Learning Targets as you can, at some point in the semester.** 

The main way you'll demonstrate skill on Learning Targets is by **working Skill Quiz problems**. Almost every week, we will have a short in-class quiz over a portion of the Learning Targets. Each quiz contains one problem for each Learning Target that is covered, and each problem focuses on just one Learning Target. 