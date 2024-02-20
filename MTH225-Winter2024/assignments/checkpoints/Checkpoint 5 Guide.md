# Checkpoint 5 Guide 

## S1

1. $1277$
2. $D9$
3. $1011000110$
4. `1110 0001`

## S2

There were no attempts on Skill S2 this time. If you are using this problem for practice, you can check your work with [an online calculator](https://www.calculator.net/binary-calculator.html).

## S3

| $p$ | $q$ | $r$ | $\neg p$ | $q \rightarrow r$ | $(\neg p) \vee (q \rightarrow r)$ |
| --- | --- | --- | -------- | ----------------- | --------------------------------- |
| T   | T   | T   | F        | T                 | T                                 |
| T   | T   | F   | F        | F                 | F                                 |
| T   | F   | T   | F        | T                 | T                                 |
| T   | F   | F   | F        | T                 | T                                 |
| F   | T   | T   | T        | T                 | T                                 |
| F   | T   | F   | T        | F                 | T                                 |
| F   | F   | T   | T        | T                 | T                                 |
| F   | F   | F   | T        | T                 | T                                 |


| $p$ | $q$ | $r$ | $\neg p$ | $(\neg p) \vee q$ | $((\neg p) \vee q) \rightarrow r$ |
| --- | --- | --- | -------- | ----------------- | --------------------------------- |
| T   | T   | T   | F        | T                 | T                                 |
| T   | T   | F   | F        | T                 | F                                 |
| T   | F   | T   | F        | F                 | T                                 |
| T   | F   | F   | F        | F                 | T                                 |
| F   | T   | T   | T        | T                 | T                                 |
| F   | T   | F   | T        | T                 | F                                 |
| F   | F   | T   | T        | T                 | T                                 |
| F   | F   | F   | T        | T                 | F                                 |

The two statements are NOT logically equivalent.


## S4 

*Note*: Explanations are provided for part 1. These are not required for your work; they're only here for study purposes so you can see why the statements are true or false. 

1. (a) False ($2^7 = 128$) 

  (b) False ($2^3 = 8$)

  (c) False (Counterexample: $x = 7$)

  (d) True (Example: $x = 2$)


2. There exists a February that is not cold. (Or: Some Februaries are not cold.)

## S5

Given: $a_0 = 0, a_1 = 2, a_2 = 2$. 

$a_3 = a_2 + 3a_0 = 2 + 3(0) = 2$
 
$a_4 = a_3 + 3a_1 = 2 + 3(2) = 8$

$a_5 = a_4 + 3a_2 = 8 + 3(2) = 14$

$a_6 = a_5 + 3a_3 = 14 + 3(2) = 20$

$a_7 = a_6 + 3a_4 = 20 + 3(8) = 44$

### Common mistakes

- **Only going back two steps in the recurrence relation instead of three:** The recurrence relation is $a_n = a_{n-1} + 3a_{n-3}$, so three steps back are required. Several only went back two,and computed $a_n = a_{n-1} + 3a_{n-2}$.

## S6

1. $R(1) = 4$, $R(2) = 7$, $R(3) = 10$. 
2. For $n > 1$, $R(n) = R(n-1) + 3$. This is true because in the visual, each step is obtained from taking the previous figure and adding three hexagons on to the right (or left) of the figure. 