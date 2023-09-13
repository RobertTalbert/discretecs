# Basic connectives and negating conditional statements

## MTH 225, 2023-09-13

In Monday's class we practiced with the four basic **connectives** that join simple "atomic" propositions into more complex "molecular" ones: 

- Negation ("not"), which is notated $\neg P$ 
- Conjunction ("and"), notated $P \wedge Q$ 
- Disjunction ("or"), notated $P \vee Q$ 
- Implication ("if-then"), notated $P \rightarrow Q$ also known as a *conditional statement*. 

**The truth value of these statements is determined by the truth values of the atomic statements that make them up.** For example, a conjunction ("and") is true if the two statements involved are both true, and false otherwise. One way to understand this is to make a *table* that has all the possible truth values of the two statements involved in two separate columns, and then a third column showing the result for $P \wedge Q$: 

|  $P$  |  $Q$  | $P \wedge Q$ |
| :---: | :---: | :----------: |
| True  | True  |     True     |
| True  | False |    False     |
| False | True  |    False     |
| False | False |    False     |

This is known as a **truth table** for $P \wedge Q$. Truth tables will be the main focus of Friday's class, but they are useful for understanding basic connectives today. 

**Quick activity:** Fill in the final column in each of the following three truth tables for the other basic connectives. Try to do it from memory and your own understanding of how the connectives work, rather than just looking them up. 

*Negation* (notice, just one atomic statement is involved so only two rows): 

|  $P$  | $\neg P$ |
| :---: | :------: |
| True  |          |
| False |          |

*Disjunction*: 

|  $P$  |  $Q$  | $P \vee Q$ |
| :---: | :---: | :--------: |
| True  | True  |            |
| True  | False |            |
| False | True  |            |
| False | False |            |

*Implication*: 

|  $P$  |  $Q$  | $P \rightarrow Q$ |
| :---: | :---: | :---------------: |
| True  | True  |                   |
| True  | False |                   |
| False | True  |                   |
| False | False |                   |

Fill in the ???'s on this important statement: 

> The conditional statement $P \rightarrow Q$ is false only when $P$ is ??? and $Q$ is ???. Otherwise the conditional statement is ???. 

---

**Negations of conditional statements:** Negating a conditional statement means giving a proposition whose truth values are exactly opposite those of the original conditional statement. So, because $P \rightarrow Q$ is false when $P$ is true and $Q$ is false and is true otherwise, the negation of $P \rightarrow Q$ would need to be a statement that is *true* when $P$ is true and $Q$ is false and is *false* otherwise. 

Here's an excerpt from the course vault entry on "Conditional Statements": 

> The negation of a conditional statement is *not* another conditional statement, rather it is the proposition $P \wedge (\neg Q)$. 

1. State the negations of the following conditional statements: 

   (a) If it's raining outside, then it's cloudy. 

   (b) If I earn a 100% on my final exam, I will get an A in the class. 

Remember: Your negations should be "and" statements and *should not* have "if-then" language in them because the negation of a conditional statement is not another conditional statement. 

2. What's the one condition under which $P \rightarrow Q$ is false? What is the relationship between this condition and the proposition $P \wedge (\neg Q)$? 

