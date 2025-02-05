# Answers/Solutions for Application/Analysis Homework 3

## Practice Exercises

To check your work on these exercises, please use the technological tools we've introduced in class and contact me (Talbert) with any questions you have. If you submitted work, I will look at it and give feedback on the PDF you submitted (check Blackboard for this). 

The [truth table generator website](https://web.stanford.edu/class/cs103/tools/truth-table-tool/) can be used for all of these practice exercises this time. 

## Multiple Choice items 

1. D
2. D
3. Both B and D are correct
4. C
5. C

## Problems to Solve

1. [Click here](https://shottr.cc/s/1z89/SCR-20250205-i92p.png) (or [here](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/assignments/AA-HW2-key.md)) for the truth table  for $P \leftrightarrow Q$. The truth tables for the others, with intermediate columns shown, are below and notice that the final columns in each are the same as for $P \leftrightarrow Q$. 

| $P$ | $Q$ | $\neg P$ | $\neg Q$ | $(\neg P) \leftrightarrow (\neg Q)$ | 
| --- | --- | ------- | -------- | ------------ | 
| T | T | F | F | T |
| T | F | F | T | F |
| F | T | T | T | F |
| F | F | T | T | T |


| $P$ | $Q$ | $P \wedge Q$ | $\neg P$ | $\neg Q$ | $(\neg P) \wedge (\neg Q)$ | $(P \wedge Q) \vee ((\neg P) \wedge (\neg Q))$ |
| --- | --- | ------------ | -------- | -------- | -------------------------- | ---------------------------------------------- |
| T   | T   | T            | F        | F        | F                          | T                                              |
| T   | F   | F            | F        | T        | F                          | F                                              |
| F   | T   | F            | T        | F        | F                          | F                                              |
| F   | F   | F            | T        | T        | T                          | T                                              |


2. Truth tables for each logical argument are shown below with intermediate columns if needed. The columns with the premises in them are marked with a check mark (✓) and the column with the conclusion in it is marked with a star (☆). Check to see that whenever the premises are all true, the conclusion is also true. Sample English versions of each are shown in italics. 

Disjunctive syllogism: *I am taking either MTH 225 or CIS 263. I am not taking CIS 263. Therefore I am taking MTH 225.* 

| $p$ | $q$ ☆ | $p \vee q$ ✓ | $\neg p$ ✓ |
| --- | ----- | ------------ | ---------- |
| T   | T     | T            | F          |
| T   | F     | T            | F          |
| F   | T     | T            | T          |
| F   | F     | F            | T          |

Addition: *I am taking MTH 225. Therefore I am either taking MTH 225 or MTH 325.* 

| $p$ ✓ | $q$ | $p \vee q$ ☆ |
| ----- | --- | ------------ |
| T     | T   | T            |
| T     | F   | T            |
| F     | T   | T            |
| F     | F   | F            |

Simplification: *I am taking both MTH 225 and CIS 163. Therefore I am taking CIS 163.* 

| $p$ ☆ | $q$ | $p \wedge q$ ✓ |
| ----- | --- | -------------- |
| T     | T   | T              |
| T     | F   | F              |
| F     | T   | F              |
| F     | F   | F              |

Resolution: *Either I am taking MTH 225 or I am taking MTH 325. Also, either I am not taking MTH 225 or I am taking CIS 263. Therefore I am either taking MTH 325 or MTH 263.* 

| $p$ | $q$ | $r$ | $p \vee q$ ✓ | $\neg p$ | $(\neg p) \vee r$ ✓ | $q \vee r$ ☆ |
| --- | --- | --- | ------------ | -------- | ------------------- | ------------ |
| T   | T   | T   | T            | F        | T                   | T            |
| T   | F   | T   | T            | F        | T                   | T            |
| F   | T   | T   | T            | T        | T                   | T            |
| F   | F   | T   | F            | T        | T                   | T            |
| T   | T   | F   | T            | F        | F                   | T            |
| T   | F   | F   | T            | F        | F                   | F            |
| F   | T   | F   | T            | T        | T                   | T            |
| F   | F   | F   | F            | T        | T                   | F            |


3. See the previous solution for explanations, except this time rows where the premises are true but the conclusion is false will be marked with an arrow $\Leftarrow$. 

Affirming the conclusion: *If I pass MTH 225, I will be smart. I am smart. Therefore I passed MTH 225.* 

| $p$ ☆ | $q$ ✓ | $p \rightarrow q$ ✓ |              |
| ----- | ----- | ------------------- | ------------ |
| T     | T     | T                   |              |
| T     | F     | F                   |              |
| F     | T     | T                   | $\Leftarrow$ |
| F     | F     | T                   |              |

Denying the hypothesis: *If I pass MTH 225, I will be smart. I didn't pass MTH 225; therefore I am not smart.* 

| $p$ | $q$ | $p \rightarrow q$ ✓ | $\neg p$ ✓ | $\neg q$ ☆ |              |
| --- | --- | ------------------- | ---------- | ---------- | ------------ |
| T   | T   | T                   | F          | F          |              |
| T   | F   | F                   | F          | T          |              |
| F   | T   | T                   | T          | F          | $\Leftarrow$ |
| F   | F   | T                   | T          | T          |              |