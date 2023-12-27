# MTH 225: Discrete Structures for Computer Science 1

![](mth225-logo.png)

>Let us change our traditional attitude to the construction of programs: Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to human beings what we want a computer to do.
>
>-- Donald Knuth, *Literate Programming*

## About MTH 225 and this syllabus

**Welcome to MTH 225!** I'm Dr. Robert Talbert, the professor for this course. I'm grateful you're here. 

In this course, you will learn **the math that all of computer science is based on**. You'll learn things like how to do arithmetic in binary, how to count the number of ways to deal a five-card poker hand, and how to generate complex data structures using simple rules involving recursion. And more! By studying discrete structures, **you'll gain a superpower to make you an expert learner of any hardware and any software, including those that haven't been invented yet**. As a computer scientist, your ability to learn new things quickly, and use fundamental concepts to model complex ideas, are more valuable than your coding skills. 

**This syllabus contains all the information you need to navigate the course.** The main document will be kept continuously up to date at this link. When you see blue- or purple-underlined text in the syllabus or any other document, it's a clickable link. For example, [click here for a cat video](https://www.youtube.com/watch?v=aFuUidBR1aQ). A PDF version of the syllabus will also be available on Blackboard, but it will not be updated unless there is a major change. 

**This document is meant to be read once, then searched as needed.** If you need to find something, the easiest way is to pull up this  document, hit `Control-F` or `Command-F`, and then do a search for the text you're looking for. 

All course materials for MTH 225 are available on GitHub at https://github.com/RobertTalbert/discretecs. The current version is in the folder `MTH225-Winter2024`. Critically important documents (syllabus, etc.) will also be on Blackboard. 

This course is subject to the GVSU policies listed at http://www.gvsu.edu/coursepolicies/. 

## Key Information

**Professor:** Robert Talbert, Ph.D., Professor of Mathematics. My office is Mackinac Hall C-2-513; my email is [talbertr@gvsu.edu](mailto:talbertr@gvsu.edu); my direct phone is 616-331-8968. 

**Student drop-in hours:** Open drop-in times in MAK C-2-513 are **4:00-5:00pm Monday and Wednesday**. Additional hours are available by appointment by going to http://calendly.com/robert-talbert and selecting a 20-minute time slot from *MTH 225 student appointment*. Appointments are in-person; if you need an online meeting or phone call, please select *20 minute online meeting* or *20 minute phone call* from the Calendly page.

**Meetings:** Section 03 and Section 04 meet Monday/Wednesday/Friday in Mackinac Hall A-2-155. Section 03 meets 11:00-11:50pm and Section 04 meets 12:00-12:50pm. 

**Textbook:** There is no requuired textbook for the course. An optional textbook is *Discrete Mathematics: An Open Introduction* (third edition) by Oscar Levin, available for free online at https://discrete.openmathbooks.org/dmoi3/dmoi.html. 

**Course resources:** We use three main resources instead of a textbook. All three are free, and can be accessed from this syllabus, the Course Page, or Blackboard. It's a good idea to  bookmark all three in your browser.
- **Blackboard**, at http://lms.gvsu.edu 
- The **Course Page**, a Google Doc of notes and links, at http://gvsu.edu/s/2xI (last three characters are 2, lower-case "x", upper-case "I")
- The **Course Vault**, a wiki of articles on class topic, at https://publish.obsidian.md/mth225 


**Contacting the prof:** Email (talbertr@gvsu.edu) is preferred. **Blackboard messaging is turned off for this course; please use email instead.** Be sure to read **my availability/response policy**.

**Course calendar:** The official course calendar is in **Google Calendar** [at this link](https://calendar.google.com/calendar/embed?src=5da852835eebf4c3ee076f95e7aa2b063dd56b06144a579037ecf8365394d6cc%40group.calendar.google.com&ctz=America%2FDetroit). It is also linked on the [Class Page](https://docs.google.com/document/d/1OVmgR7H6U3wOlUDk2rCr9iVRVET9PqlxYGF05Mb84Xw/edit?usp=sharing) and embedded at the end of this syllabus, although some web formats do not display it correctly. *The calendar on Blackboard will not show all dated items* so please use it only as a supplement to the Google Calendar. In case of an apparent date conflict, the Google Calendar is correct. 

**Definition of "week":** In our course, a "week" is defined to begin at 12:01am ET on Monday and end at 11:59pm ET the following Sunday. 

**Technology:** Please plan on bringing a laptop or tablet (laptop preferred) to class each day for group work. It's highly recommended to have access to a high-speed internet connection for work outside of class. You will need access to a basic handheld calculator for Checkpoint assessments in class. There is no preferred model of device. Please review the Class Technology Policy for acceptable use. 

## What you will learn 

MTH 225 is the first of a two-semester sequence on the mathematical foundations of computer science. In MTH 225, you'll be learning about: 

- **How computers represent and work with (whole) numbers**: Representing integers (whole numbers) in binary, octal, and hexadecimal; binary arithmetic; two's complement notation for negative integers; the Division Algorithm and modular arithmetic. 
- **How computers "decide" what to do in a program**: Logical propositions, conditional statements, truth tables, predicates, and quantification. 
- **How computers package and transform collections of data**: Set notation and representation, set operations, functions. 
- **How to count complex arrangements of things**: The Additive and Multiplicative counting principles, the binomial coefficient, permutations, dots-and-dividers counting methods; using computational thinking to solve combinatorics problems. 
- **How to form abstract general observations about things and explain why they are true, *without* using a computer**: The Principle of Mathematical Induction and proof by induction.

A common thread through all of these is **recursion**, which is the concept of computing or building something using smaller versions of itself. Recursion is a powerful tool in computer science and mathematics, and it links together almost all the specific topics we will encounter in the course. 

### Skills and Mega-Skills 

There are 16 **Skills** in the course that are highlighted for you to learn. These are specific, concrete actions that you should be able to perform with skill and fluency by the end of the course. Six of these are designated as **Core Skills** which means that **every student must master these to pass the course**. The remaining 10 skills are **Supplemental Skills**, and while mastering these is not required to pass the course, the more you master, the higher your grade is. More on that in the *"How you will be evaluated and graded"* section. All 16 Skills are listed in Appendix A. 

We will also focus daily on four **Mega-Skills** that go beyond the content, and which you'll be using for the remainder of your careers regardless of the direction it takes: 

- **Bulls*it detection**: Being able to look at a program, problem solution, or explanation -- especially those you create -- and find and fix errors and misconceptions in it. 
- **Deliberate practice**: Practicing a skill, not mindlessly but with focused attention and a goal of improving performance. 
- **Explaining things to another human**: Taking a complex idea and making it make sense to a normal, non-expert human being through a clear, correct, and complete verbal explanation. 
- **Solving hard problems**: Taking a problem that is more than just a simple exercise, and applying structured reasoning, creative strategies, and tenacious persistence to make progress. 

The four Mega-Skills are not directly part of your course grade but will be the focus of many activities that are, and will be frequently referenced in class. 

### Official learning objectives

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


## How to succeed 

All important learning experiences you've ever had, or will have, are the result of a **feedback loop**: You try something, then you get feedback on your attempt, then you think about and make sense of the feedback, then you use the feedback in another attempt. And this loop continues until the thing you are trying meets a standard of quality.

(Image) 

Being successful in MTH 225 means two things: **Mastering the basic skills of discrete mathematics** and **successfully applying those basic skills to hard problems**. The way to become good at these two things, is by **engaging with the activities and the feedback loops in the course** that are set up for you. And this engagement involves a number of simple actions and behaviors that you will need to show consistently: 

- **Attending class**, and not only being physically present but **mentally engaged and participatory** in class activities.
- **Blocking off daily times** for working on the class outside of class meetings.
- **Mindful practice on basic skills** during those daily work times. 
- **Careful understanding of feedback** on your work so that you can incorporate it into later attempts intelligently. 
- **Consistent submission of attempts** on class work, described later. 
- **Asking questions about math** in drop-in hours, class meetings, or emails. 

Successful MTH 225 students have this in common: They all engage in these behaviors and do these actions consistently, every day throughout the course. Unsuccessful students typically fail to be consistent in one or more of these. **The common denominator is focus and consistency** -- you do not have to be a "math genius" to do well in MTH 225! You just have to **consistently engage with the feedback loops** that are there for you. 

**I want you to be successful in this class.** I am personally invested in each student mastering all of the important topics and learning objectives listed in the previous section, and in your growth as a learner. I will challenge and support you, and if you engage with the learning activities and the feedback you receive, you will learn a lot and have a great experience. 

## The work you will do 

In MTH 225 the activities and assignments are all designed intentionally to give you practice along three axes: **basic skills**, **applications and extensions** of those skills, and **engagement in the course**. 

(Image) 

### Skills and Checkpoints

Sixteen (16) **Skills** are highlighted from among the topics you will learn in the course. Six (6) of these are designated as **Core Skills**, and mastery of these six is required for passing the course. The remaining ten (10) are **Supplemental Skills** and while their mastery is not required to pass the course, your course grade will go up the more of the Supplemental skills you master. All 16 Skills are found in Appendix A. 

To master a Skill, you will need to provide a **successful demonstration** of your competence on that Skill. The primary way to do this is through **Checkpoints**: timed quizzes given regularly in the class. Typically, Checkpoints are given every other week, although they will become more frequent near the end of the course. Checkpoints will contain short exercises for you to complete, with each exercise focusing on a single Skill. **Checkpoints always contain new versions of all six Core Skills** as well as **new versions of any Supplemental Skill that had previously appeared**, so they are "cumulative" and if you don't have a successful attempt on an exercise on a Checkpoint, you can try again multiple times later. 

Completing an exercise for a Skill is considered a "successful demonstration" if your work meets the standards that are explained in the **success criteria** for that exercise. The success criteria will always be listed on the Checkpoint following the exercise so you'll always know what you need to do to have a successful attempt. The Standards for Student Work document also contains a listing of the success criteria for each exercises for all 16 Skills. 

**Mastering a Skill requires two (2) separate successful demonstrations**. The way mastering a Skill will work for most students is that you will do successful work on an exercise one week; then do it again in a later week. This way, you will space out your attempts on a skill and retain the information better than if it were just "one and done". 

Alterative methods for demonstrating skill, for example oral exams in drop-in hours, may be added later in the course if it appears you'd benefit from it. 

### Challenge Problems 

To give you practice and assessment on applying and extending the basic skills, you'll complete several **Challenge Problems** during the course. These are hard problems based on the basic skills learned in class. They may involve tricky computation, explaining complex processes to another person, explaining why code works, proving a mathematical statement, or something similar. In any case **they will not be basic homework-style problems but something complex that requires multiple Mega-Skills.** 

Challenge Problems are all located in the Challenge Problem document (click the link to access). That document will have new problems added throughout the semester. 


### Engagement with the course

To really learn and succeed in MTH 225, you will need to become involved in the course through preparing for class, attending class, being actively involved in class activities, engaging in deliberate practice outside of class, and more. **Disengagement with the class is by far the main reason students fail.** "Smart" students who are disengaged usually end up repeating the course; conversely students who might still be working on their math skills but who stay engaged with the class usually do quite well. 

Activities that require mindful engagement with the course are given **engagement credits**. Satisfactory completion of an activity that has engagement credit value will add those credits to a running total. Recurring activities that earn engagement credits include: 

- **Class Prep**: Activities that you complete -- involving watching videos, doing some reading, and completing some exercises -- to prepare for an upcoming class meeting. **Each Class Prep is worth 2 engagement credits.** 
- **Class attendance**: Attendance will be taken at each class meeting, and being in the class for at least 40 minutes will earn you **1 engagement credit**. 

Additionally, you'll be given a **Startup Assignment** during the first week of the semester that will have engagement credit value. Throughout the semester there will be opportunities to earn more engagement credits through practice homework sets, completing surveys, and other means. 

## How you will be evaluated and graded

### Overview of how grading works in MTH 225 

Grading in MTH 225 is different from what you might have experienced, because it's based on **feedback loops** as described earlier. In MTH 225: 

- **Almost none of your assignments have point values**. Only the final exam and engagement-credit items have point values. Therefore there is **no partial credit and no averaging**. 
- Instead, assignments have **standards** which are descriptions of what constitutes "acceptable" work. These are given in detail in the document [Standards for Student Work] which you can find at the link and on Blackboard. When you submit an assignment, I will read it carefully and compare it with the standards, and simply determine whether it meets the standards or not. Typically your work is marked either **Success** or **Retry** depending on whether it meets the standards or not. 
- After I evaluate your work, in most cases you will receive **detailed feedback** that will tell you whether your work meets the standards, and if not, the feedback will tell you what was missing and how you might go about fixing it. 
- Then, on most items, you will have the chance to **retry** the assignment if needed, get more feedback, and repeat this **feedback loop** until the work meets our standards. 
- Your course grade is not based on point totals or averages (because there are no point values). Instead, the course grade is based on **how many important learning tasks you've successfully accomplished** by the end of the semester, using a simple table that's given below. 

Therefore grades in MTH 225 are based not on your ability to do good work at a single point in time, but rather on your ability to **eventually learn the material** by acting on feedback from previous attempts. 

This process, using standards and feedback loops rather than points and averages, is how evaluation of work happens in most situations outside of college. In your future jobs, for example, you'll be reviewed regularly by your manager; it's not a "one and done" situation where you get a point score and then the process is over. Instead, in a real job, you get feedback and coaching on how to improve, and then you act on the feedback and show the boss that you have improved. 

Those are the main concepts; the details are in the rest of the syllabus. Most students need a week or two to adapt to this system, but then everything is fine. I encourage you to ask questions at any time so I can help you. 

### How items are graded and recorded on Blackboard 

Your common, recurring assignments are graded and then recorded on Blackboard as follows: 

| Assignment | How it's graded | What's recorded in the gradebook | 
| ---- | ---- | --- | 
| Skill exercises on Checkpoints | Overall correctness | Nothing, see below |
| Skills | n/a, see below | 0, 1, or 2 |  
| Challenge Problems | Completeness, overall correctness, writing, and presentation | *Success* or *Retry* | 
| Engagement credit items | Completeness and effort | Engagement credit value | 

**How Checkpoints and Skills work:** You will work out individual Skill exercises separately, and each attempt on a Skill is graded *Success* or *Retry*, depending on whether or not the work meets the success criteria. You'll get each attempt back, with feedback to prepare for your next attempt if needed. **The individual attempts are not recorded on Blackboard**. Instead, **each Skill has its own gradebook entry that reads 0, 1, or 2 indicating the number of successful attempts that have been made so far.** Once a skill reaches "2", you have mastered that skill and no further demonstrations are necessary. 

**Engagement Credit total:** Individual items that receive engagement credits will be visible in the Blackboard gradebook along with the number of credits you received on it. Additionally, there is an entry for the running total of Engagement Credits you've earned so far in the course, so you can track your progress. 

**Final exam:** In addition to the regular assignments, we will have a final exam consisting of two main parts: A comprehensive exam focusing on main concepts and big ideas; and a final Checkpoint for anyone who needs one more attempt on a Skill. 

### How your course grade is determined 

Your course grade is assigned using the table below. It shows the *minimum* requirements for the "base grades" of A, B, C, and D. Plus/minus modifiers are applied using the rules below the table. **To earn a grade in the course, you need to meet or exceed *all* the requirements for that grade.**

| Grade | CORE skills mastered | SUPPLEMENTAL skills mastered | Challenge Problems | Engagement Credits |
| :-----: | :--------------------: | :----------------------------: | :------------------: | :------------------: |
| A     |  6                    |                 8             |      10              |       90             |
| B     |  6                   |                   4           |        6            |         80           |
| C     |  6                    |               2               |       2             |        70            |
| D      | 3                    |                0              |        0            |        50            |

A grade of "F" is given if not all of the requirements for a "D" are met. 

There should be at least 100 engagement credits possible in the course, possibly significantly more. If it appears by the middle of the term that we will fall short of that 100 minimum, the numbers in the last column above may be updated. 

**Plus/minus grades:** A "plus" is added to a base grade if you meet all the requirements for the base grade, and then earn an 85% or higher on the final exam. A "minus" is added to a base grade if either (1) you meet all the requirements for the base grade *except* for engagement credits, or (2) you meet all the requirements for the base grade but then earn a 50% or lower on the final exam. (Therefore the only effect the final exam has on your grade is modification up or down by a "half letter".) If the criteria for both plus *and* minus grades are met, then the modifiers cancel out, and you retain just the base grade without modification. Please note, GVSU does not award grades of A+ or D-. 

**Grade assignments in borderline cases:** Please note that *all* requirements for a base grade must be met, and exceeding the requirements in one column will not offset failing to meet the requirements in another. However, if you end the semester having come close to completing all the requirements for a base grade, I will look at your case individually and take the full scope of your work in the class into account, and assign a grade based on my professional judgment and in consultation with you. You may be assigned a course grade higher than what the syllabus indicates if I believe it's warranted; you will never be assigned a course grade lower than what the syllabus indicates. 





## How to revise and retry your assignments 

## Using technology 

- How we use tech
- Tech skill expectations
- Tech support 

## Academic integrity

- General academic integrity policy 
- AI policy 

## How to get help

MTH 225 can be a challenging course, because the topics might be unfamiliar, and you'll be asked to think about doing mathematics in a way that you probably haven't been asked in your high school courses. You will almost certainly find yourself lost, stuck, or confused on *something* in this course at some point. **This is normal and not a cause for alarm.** 

When you get confused or stuck, try to get yourself unstuck first by thinking through your work. But then **ask questions and seek out help as soon as you need it.** You can do this in several ways: 

* **Participate actively in class** since most class activities are designed to align with major topics and assignments. 
* **Attend drop-in hours and ask questions there.** You can use the in-person drop-in hours (no appointment needed) or [schedule](https://calendly.com/robert-talbert/) an online meeting or an in-person meeting at other times if drop-in hours don't work for you. 
* **Work with a classmate** as long as you're staying within bounds on academic integrity above. 

**Math Tutoring Center:** GVSU’s Math Tutoring Center offers both in-person and online drop-in tutoring this semester.  You can access the most up-to-date information at http://gvsu.edu/tutoring/math/.  There you will find our current hours, information on how to access online tutoring with Discord Voice and a schedule of when you can find tutors to help with your specific course.  Bring questions to any center about using technology (calculator or Desmos), on methods and concepts, or on specific problems.  All Math Center tutoring is FREE, so stop by early and often.  

## Other Course Policies 

**Instructor availability and responses:** I strive to respond promptly to all student emails. However, please note that **I do not typically check email between 6:00pm and 6:00am on weekdays, and I do not check it at all on weekends** in order to prioritize time for family and rest. If you send a message on a weekday (Monday-Friday) before 3:00pm ET and you need a response, you will get a response *the same day*. Emails received after 3:00pm ET Monday-Thursday will get a response *the following day*. Emails received after 3:00pm ET on Fridays will get a response *the following Monday* at latest. Please plan ahead with this policy in mind! 

**Attendance:** Consistent attendance is critical for success in MTH 225, and you are expected to attend each class meeting unless it is physically impossible. Attendance will be recorded and assigned engagement credits (1 credit per class meeting). Since you have many opportunities to earn engagement credits, there are no makeups or allowances for medical and other situations. Students who do not attend class consistently will be contacted to discuss their situations further. If you have a life situation that makes consistent attendance difficult, please bring it to my attention immediately so we can discuss your options. 

**Announcements:** Announcements will be posted every Sunday morning on Blackboard in a single "announcement drop". Supplemental announcements may be sent in the case of time-sensitive items that can't wait until Sunday. Each student is responsible for reading announcements carefully and maintaining awareness of their contents. 

**Late work and makeups:**

**Remote instruction:** https://www.gvsu.edu/provost/guidelines-for-course-delivery-in-the-event-of-253.htm

**Disability Support Resources:** If you have special needs because of learning, physical or other disabilities, it is your responsibility to contact Disability Support Resources (DSR) at (616)331-2490 or http://www.gvsu.edu/dsr/. DSR will help you arrange accommodations. Then, speak with me in person about making those accommodations and ensure that they are consistent with your arrangements with DSR.

**Basic needs:** If you have difficulty affording groceries or accessing sufficient food to eat every day, or if you lack a safe and stable place to live, I encourage you to visit [Replenish](https://www.gvsu.edu/replenish/), a food resource for GVSU students. If you are comfortable doing so, please speak with me about your circumstances so that I can advocate for you and to connect you with other campus resources.

**Gender identity and expression:** If, for purposes of gender identity and expression, your official name (in Banner) does not match your preferred name, your name can be updated in Blackboard. Please contact the registrar's office to submit this request. The registrar's office will contact the Blackboard administrator to make the change and will also contact your professors to inform them that your name in Banner will not match the name in Blackboard.

**Classroom and campus safety**: 



The professor reserves the right to adjust this syllabus as needed and will notify you of any changes through Blackboard announcements. 


## About the instructor 

I'm Robert Talbert, the professor for this course. I'm a Professor of Mathematics and also work in the president's office. This is my 31st year of teaching overall. I have a Ph.D. in Mathematics from [Vanderbilt University](http://vanderbilt.edu) and a B.S. degree from [Tennessee Tech University](http://www.tntech.edu). 

I was, at best, a thoroughly mediocre math student in school until my senior year of high school, when I had a teacher for Calculus who stopped trying to cram things into my head and instead showed me the basics -- and then backed off, and let me work things out on my own (with support if I got stuck). Basically, this is how I teach today. 

After a two-year excursion as a Psychology major in college, I changed my major to math after a late-night dare from my roommate (long story) and, to my great surprise, I fell in love with the subject. I ended up getting a Ph.D. working in an obscure area at the intersection of abstract algebra and geometry, and I also discovered I loved teaching math to college students. So I went on to spend 14 years teaching in [small liberal arts colleges](http://franklincollege.edu) before coming to GVSU in 2011.

Now, I teach computer scientists and engineers how to think like mathematicians; I do research on how to make college teaching better; and I have an appointment as "Senior Faculty Fellow for Learning Futures", in which I coordinate research and development projects to make your learning experience better here. When nobody is looking, I'm working on my data science skills including learning the languages R and Julia. 

I live in Allendale with my family. I'm an avid bass guitar player, currently playing in the Grand Rapids and Muskegon areas with the bands [Taproom Fix](https://www.facebook.com/TaproomFixBand/) and Elleven. I also love the outdoors and get out to run, bicycle, or hike when I can. You can read more about what I'm thinking and doing at my website, [rtalbert.org](https://rtalbert.org), or at my "other blog" [Grading for Growth](https://gradingforgrowth.com) about alternative grading practices which I co-author with my GVSU colleague Prof. David Clark. I'm also on Twitter at [@RobertTalbert](http://twitter.com/RobertTalbert) and on [LinkedIn](https://www.linkedin.com/in/roberttalbert/). I will accept any connection request on LinkedIn from a student! 

## Appendices

### Appendix A: MTH 225 Skills 

Each Skill requires **two (2) successful demonstrations of competency in order to "master" the skill, typically through Checkpoint problems. 

**CORE** Skills: 

- **C1**: I can identify the hypothesis and conclusion of a conditional statement and state its converse, contrapositive, inverse, and negation.
- **C2**: Given a statement to prove using mathematical induction, I can state the framework of a proof. (Identify the predicate, identify and prove the base case, state the inductive hypothesis, and state what needs to be proven in the inductive step)
- **C3**: I can use set-theoretic notation correctly and convert a set from set-builder notation to roster notation and vice versa. 
- **C4**: I can find the intersection, union, difference, symmetric difference, power set, cardinality, cartesian product, and complement of sets.
- **C5**: I can apply the Additive and Multiplicative Principles and the Principle of Inclusion/Exclusion to formulate and solve basic combinatorics problems.
- **C6**: I can compute factorials and binomial coefficients, and apply these concepts to solve basic combinatorics problems involving permutations, selections, and distributions. 

**SUPPLEMENTAL** Skills: 

- **S1**: I can convert a positive integer from base 10 to base 2, 8, and 16 and vice versa and represent a negative integer in base 2 using two's complement notation.
- **S2**: I can add, subtract, multiply, and divide positive integers in base 2.
- **S3**: I can construct truth tables for propositions involving two or three atomic propositions and use truth tables to determine if two propositions are logically equivalent.
- **S4**: I can determine the truth value of a predicate at a specific input, the truth value of a quantified predicate, and the negation of a quantified predicate. 
- **S5**: I can determine elements of a recursively-defined sequence using a recurrence relation. 
- **S6**: I can derive a recurrence relation for a recursive visual pattern, number sequence, or other sequence of objects. 
- **S7**: I can determine if a mapping is a function; identify the domain, range, and codomain of a function; and determine the image of a specific input in one function or a composition of functions. 
- **S8**: I can determine if a function is injective, surjective, or bijective. 
- **S9**: I can determine if a sequence of numbers is arithmetic or geometric and derive both closed-form and recursive formulas for them.
- **S10**: I can use the characteristic root method to find a closed-form solution for a first- or second-order linear homogeneous recurrence relation. 

### Appendix B: Schedule of Skill coverage on Checkpoints

### Appendix C: Course Calendar 
