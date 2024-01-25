# Checkpoint 2 solutions

## C1 

1. The sun is shining
2. I will go for a walk
3. If I go for a walk, the sun is shining.
4. If I don't go for a walk, the sun is not shining. 
5. If the sun is not shining, I will not go for a walk.
6. The sun is shining, but I am not going for a walk.

### Common mistakes

- **Failing to actually switch the hypothesis and conclusion when forming the converse** but instead just moving the phrase "If the sun is shining" to the second half of the sentence. What you end up with is the statement: *"I will go for a walk if the sun is shining"*. But as we pointed out in class, this is the same proposition as the original statement: The hypothesis and conclusion have not been switched, just merely written in different places. 
- **A similar error to the previous point when forming the contrapositive**: Negating the hypothesis and conclusion but not actually switching their roles, just writing them in a different order. You would end up with the statement *"I will not go for a walk if the sun is not shining."* This is the same as "If the sun is not shining, then I won't go for a walk" but that's the inverse, not the contrapositive. 
- **Including the word "If" in the negation**, giving the phrase: *"If the sun is shining, and I am not going for a walk."* As we discussed in class, the word "if" is not part of the hypothesis and therefore shouldn't be included in the negation -- because it causes this mistake. The resulting verbiage is not actually a semantically or grammatically correct sentence because it sets up an if-then statement but never tells you what the conclusion is. 
- **Writing the negation as a conditional statement**: For example *"If the sun is shining, then I will not go for a walk."* The negation of $P \rightarrow Q$ is $P \wedge (\neg Q)$ so the negation must be a conjunction, not another conditional statement. 
- **Writing the negation as a conjunction but negating the wrong part**: That is, writing $Q \wedge (\neg P)$ instead of $P \wedge (\neg Q)$. In English, that mistake would read as "I am going for a walk but the sun is not shining." 

---

## C2

1. The predicate is: "The number $n^3 + 2n$ is a multiple of $3$."
2. $n = 0$.
3. If $n = 0$, then $n^3 + 2n = 0^3 + 2 \cdot 0 = 0$. This is a multiple of $3$ (namely, $0 = 3\cdot 0$) so the base case holds.
4. Assume that for some positive integer $k$, the number $k^3 + 2k$ is a multiple of $3$. 
5. Prove that $(k+1)^3 + 2(k+1)$ is a multiple of $3$. 

---

## C3 

1. (a) False 

   (b) False

   (c) False 

   (d) True

   (e) True 

2. (a) $\lbrace 1, 2, 4, 8, 16, 32, 64, \dots \rbrace$

   (b) $\lbrace 0,1,2,3 \rbrace$

   (c) Could be interpreted as incorrect syntax; or if viewed as a Boolean function, results in the set $\lbrace True, False \rbrace$. 



---

## C4

1. $\lbrace 3,4,5\rbrace$
2. $\lbrace 1,2,3,4,5,6,7\rbrace$
3. $\lbrace 6,7\rbrace$
4. $\lbrace 0,1,3,4,5\rbrace$
5. $10$
6. $\lbrace \emptyset, \lbrace 0\rbrace, \lbrace 1\rbrace, \lbrace 0,1\rbrace\rbrace$

---

## C5

1. There are $10$ choices for each digit and $26$ choices for the letter. The choices are independent, so the total count is $10^3 \cdot 26 = 26000$. 
2. Under these conditions only the third digit can be freely chosen, with $10$ options; and there are only $5$ choices for the letter. So the total count is $5 \cdot 10 = 50$. 
3. The number of passwords starting with `00` is $10 \cdot 26 = 260$. The number of passwords ending in a vowel is $10^3 \cdot 5 = 5000$. The number of passwords that satisfy both requirements is $50$ (found in step 2). So the total count is $260 + 5000 - 50 = 5210$ by the Principle of Inclusion and Exclusion. 

---

## C6

1. (a) $5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1= 120$. 

   (b) $\displaystyle{\binom{20}{17} = \frac{20!}{17! \cdot 3!} = \frac{20 \cdot 19 \cdot 18}{3\cdot 2 \cdot 1} = 1140}$. 

2. (a) There are $8$ choices for who to put first in line, then $7$ for second in line, and so on until there are $2$ choices for the next-to-last person and then $1$ choice for the last person. So the total count is $8! = 40320$. 

   (b) This is asking for a unordered selection of 3 items from a set consisting of 8 items. That count is given by the binomial coefficient: $\displaystyle{\binom{8}{3} = 56}$. 


---

## S1 

1. $3283$
2. $1067$
3. $1010111$
4. `1001 1110`

## S2 

1. `0111010`
2. `01010`
3. `0100111000`
4. `1000` with remainder `100`