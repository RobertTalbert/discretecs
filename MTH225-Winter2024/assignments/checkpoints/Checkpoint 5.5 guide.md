# Checkpoint 5.5 guide

## C1

Original statement: *If the rug is dirty, then it should be vacuumed.* 

1. The rug is dirty
2. The rug should be vacuumed
3. If the rug needs to be vacuumed, then it's dirty.
4. If the rug doesn't need to be vacuumed, then it isn't dirty.
5. If the rug is not dirty, then it shouldn't be vacuumed.
6. The rug is dirty but it does not need to be vacuumed. 

### Common mistakes

- **Forming the converse by reversing the order of the sentence but without changing the hypothesis and conclusion:** This would look like "*The rug should be vacuumed if it's dirty.*" Note the word "if" here: What follows the word "if" is the hypothesis of the statement, no matter where it is located. And it's the same hypothesis as the initial statement; the logic of the conditional statement hasn't changed, so this isn't the converse. 
- **Forming the negation incorrectly:** The negation of $P \rightarrow Q$ is $P \wedge (\neg Q)$ (that is, " $P$ and not $Q$"). In particular the negation of this statement **is not** another if-then statement. 

## C2

Proposition: For every integer $n \geq 1$, the number $3^n - 1$ is a multiple of $2$.

1. The predicate $P(n)$ is " $3^n - 1$ is a multiple of $2$.".
2. $n=1$
3. Suppose $n=1$. Then $3^n - 1 = 3^1 - 1 = 3 - 1 = 2$. This is a multiple of $2$ (since $2= 2 \times 1$) so the base case holds. 
4. Assume that for some integer $k>1$, $3^k - 1$ is a multiple of $2$.
5. Prove that $3^{k+1} - 1$ is a multiple of $2$.

### Common mistakes

- **Including the universal quantifier when stating the predicate:** That is, stating that the predicate is the entire statement "For every integer $n \geq 1$, the number $3^n - 1$ is a multiple of $2$." Including the "for every..." quantifier is incorrect because if you quantify the predicate, the result is not a predicate any more. And note that the success criteria specifically state that the quantifier is not to be included, for that reason. 
- **Not putting the word "assume" in the inductive hypothesis:** The inductive hypothesis is important because it is an *assumption* that we make to begin an argument. You want to be clear to your reader that you are making an assumption; leaving the word "assume" off, makes this very unclear. 
- **Using "for all" instead of "for some" in the inductive hypothesis:** That is, stating "Assume that for *every* integer $k>1$, $3^k - 1$ is a multiple of $2$." We discussed in class why this is incorrect -- it amounts to assuming the very statement that you are proving. 