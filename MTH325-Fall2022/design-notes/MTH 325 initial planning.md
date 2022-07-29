# MTH 325 Planning 

## Step 0

+ Who
    - There are 24 students in Section 03 and 14 students in Section 04 as of 2022-07-27
    - The students in MTH 325 are primarily CS majors
        - Section 03: All CS except for one music (!) major; mostly jr/sr
        - Section 04: All CS so far, 8/14 are sophomores which is unusual
    - A number of repeat customers from 225
    - Typically a bunch of these students have taken CIS 263 (algorithms) so there's some overlap with graph theory
    - They've all had MTH 225 so they have a decent understanding of what discrete math is, but might need a refresher 
    - Goals -- IDK but many are fairly far along in their careers and close to graduation. Probably means they don't want a lot of hassle, and are taking some advanced classes, projects, internships, etc. 
    - Stakeholders: 
        - School of CIS, esp senior level courses 
        - Graduate schools into which they are going
        - Employers 
    - About me
        - Coming back into F2F teaching after a while online
        - Doubling down on teaching and research, not so much on leadership 
        - So I am curious to try out new stuff, but also I am aware of not overloading myself since I want to focus less on work 
        - Plenty of experience with the 225-325 sequence but my first time back with 325 since 2017 and first time teaching since the redesign that puts proof in the first 1/4 of the course 
+ What
    - Topic areas: Proof -> Graphs -> Relations -> Trees. 
    - Some overarching narratives
        - Using various flavors of graph structures to model and analyze relationships 
        - Reasoning about algorithms for graphs and related structures -- drawing conclusions about these without writing code 
        - Many have already seen the material from the CS and coding side; we are now looking at the same material from the theoretical/math POV. 
        - Learning how to reason about discrete structures independently of code, learning how to think like mathematicians
        - Computational thinking applied to graph structures 
    - Proof is introduced and practiced early, but most of what we learn is woven in through the course. 
    - Creative control: Basically I have total control over the course as long as it vaguely resembles the SOR. 
+ When
    - Classes start on Aug 29, end on Friday Dec 9. 
    - From today: 33 days away. 
    - 41 meeting days not counting planned absences 
    - Planned absences: 
        - Maybe Wed 9/7 and Friday 9/9 (Apple HQ trip) 
        - Friday 10/7 for LHE conference
        - Wed 11/2 for EdSpaces conference 
    - For a total of between 37 and 39 meetings (maybe get a sub for the later ones). 
    - 15 weeks not counting Fall Break or Thanksgiving. 
    - We meet MWF. Section 03 is 12-12:50 and Section 04 is 2-2:50. 
    - Note: Need to make sure there won't be any issues with UAS/ECS
+ Where
    - Both sections meet in D2329 for the time being but I am requesting a move to an ALC 
    - It's F2F but I might try live-streaming the meetings so I can record them, and they're available for those who can't make it
+ Why
    - This course exists... well, I'm not sure why since there's so much overlap with CIS 263 and others. But in my view: It exists to help CS people think like mathematicians about structures and systems that underly the code they write. Physics:Architecture :: MTH325:CS. 
    - I am teaching the course because I like it, I like working with CS majors, because it was avaialble on a good schedule, and because I'm making a larger shift in my teaching to focus on engineering and CS courses, less so on theoretical math and math ed courses. 
    - I am excited to get back to MTH 325 because I've always liked it, and it's been a while since I did it. Feel like I have learned a lot in the last five years in terms of structuring the course and managing the various innovations I employ. 


## Step 1

## Overarching course objectives

Course objectives from the [syllabus of record](https://www.gvsu.edu/cms4/asset/9A420BCF-BA9E-0845-91754145EA82C51F/sor_descriptions_objectives__topics_for_faculty_updated_12-11-19.pdf)

1. Compute basic information about graphs, relations, and trees.
2. Solve theoretical and applied problems involving applications of basic concepts of graphs, relations, and trees.
3. Formulate computational problems in terms of graphs, relations, and trees.
4. Construct a logical framework for a proof using mathematical induction, direct proof, proof by contraposition, or proof by contradiction.
5. Analyze the structure and validity of a mathematical proof.
6. Employ effective problem-solving skills in solving computational problems.
7. Explain methods and solutions of computational problems in a clear way to a specified target audience.
8. Demonstrate fluency in applying algorithms in the formulation and solutions of mathematical problems.
9. Assess one's own work in mathematical problem solving and apply feedback to make improvements to one's own work.


## Subdivision of the course into modules 

- Module 0: Startup and review. This is just getting set up and fluent in course tools; *maybe* Python; and a quick review of what happened in MTH 225. 
- Module 1: Proof
- Module 2: Graphs
- Module 3: Relations (*edit: Updated to **Digraphs and Relations***)
- Module 4: Trees

## First pass at assessment level objectives 

[Lesson level objectives are here](https://github.com/RobertTalbert/discretecs/blob/c46a0c4634f883e16040ae380489d69b875ffa87/MTH325-Fall2022/design-notes/Lesson%20level%20objectives%20for%20MTH%20325.md). 


### Proof

+ Given a statement to be proven with mathematical induction, I can state and prove the base case, I can state the inductive hypothesis, and I can state what needs to be proved after assuming the inductive hypothesis. 
+ Given a statement to be proven using a direct proof, I can identify the assumptions to be made and the statements to be proven.
+ Given a statement to be proven using contrapositive, I can identify the assumptions to be made and the statements to be proven.
+ Given a statement to be proven using contradiction, I can identify the assumptions to be made.

Additionally: Thinking of a Proof Portfolio -- do along the lines of MTH 350 but smaller 

### Graphs

+ Determine information about a graph at the local and global level 
  + Includes: Degree of a vertex, number of vertices and edges, ... what else? 
+ Determine whether two graphs are isomorphic; if they are, give an explicit isomorphism
+ Give a proper vertex coloring of a graph and a proper edge coloring of a graph.  Determine the graph’s chromatic number and chromatic index.
+ I can determine whether a graph has an Euler path or Euler circuit, and whether a graph has a Hamiltonian path or cycle.
+ I can determine whether a description of a graph (list of vertex and edge sets, degree sequence, a drawing, or list of properties) represents a tree. 
+ I can construct a spanning tree for a (connected) graph, and I can construct a minimal spanning tree for a weighted graph using Prim's Algorithm and Kruskal's Algorithm.

### Digraphs and Relations

+ I can give examples of relations on a set that have combinations of the properties of reflexivity, symmetry, antisymmetry, and transitivity.
+ I can compute the composition of two relations (and determine when a composition cannot be computed) and raise a relation on a set to a positive integer power.
+ I can sketch the transitive closure of a digraph. I can explain whether a digraph is weakly connected and/or strongly connected. 
+ I can determine when a relation is an equivalence relation. I can determine the equivalence class for an element and determine whether two elements belong to the same equivalence class. 
+ I can determine when a set with a relation is a poset. I can draw the Hasse diagram of a poset. I can identify maximal/minimal elements and/or greatest/least elements, if they exist.


### Trees 

+ Given a list with a total ordering, I can construct the binary search tree.
+ I can list the vertices of a tree in the order they are visited using the preorder, inorder, and postorder traversals.

## Step 2

High level outline of the class and its components. 

**Focus of the course:** MTH 325 is an even mix of content/skills and concept/processes. There is a fair amount of straight-up skills that students need to learn and terminology, etc. But the point of view from which we do it, is fairly conceptual. The inclusion of proof skews this a little more toward the conceptual than MTH 225. 

**Types of assessments:**

- Proof assignments, where students have to write proofs and then submit them for peer review. (So it's based on both writing proofs and peer reviewing others'.)
  - Maybe a portfolio that is assembled from a variety of proof problems that I assign. Ungraded. Every so often we have days set aside for peer review of works in progress. Students pick which ones to review and include in their portfolios. More types of proof = Better. More proofs = Better. More peer reviews = Better. 
- Application problems, where basic stuff gets applied to real situations. 
  - Maybe it's just one portfolio and students are tasked with doing a mix of proof and applications. 
- Daily Prep, getting first contact with new info and generating data and examples that we can then use in class meetings
  - Won't have time to do videos all the time, so mostly this is like "look at these definitions, now look at the examples and tell me something about them"?
- Learning Target quizzes, where students demonstrate skill on the basic skills stuff
  - I don't want too many of these. Maybe only require one successful demo for "Pass"? 


Additionally, give practice problems each week over the skills based stuff so that students can practice. This is not graded or taken into account for a grade, though if WeBWorK does something decent I'll use it. 

**General approach to grading:** There's an SBG flavor here with the Learning Target quizzes. Maybe call these "Basic Skill Standards" to make that clear. Also an ungrading flavor with the portfolio(s). Can see the course grade determined like this: 

- You earn a base grade by virtue of number of BSS met and number of Daily Preps completed. 
- Then you make a case at the end of the semester for anything higher than that, using your portfolio. As long as the portfolio meets a baseline standard (one proof + one application?) and the base grade is a C, a C is guaranteed. Then you can argue for something higher based on the portfolio. 