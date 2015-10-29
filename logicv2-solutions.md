# Answers: Logic version 2

## Logic Level 1

(1a) It is below freezing and it's not snowing. 

(1b) If it's not below freezing, then it's not snowing. 

(2a) [Truth table here.](http://www.wolframalpha.com/input/?i=truth+table+%28p+or+%28not+q%29%29+implies+q) 

(2b) [Truth table here.](http://www.wolframalpha.com/input/?i=truth+table+%28p+or+q%29+implies+%28p+and+q%29) 

(3) Truth table for $(\neg p) \rightarrow q$ [here](http://www.wolframalpha.com/input/?i=truth+table+%28not+p%29+implies+q). This is the same as the basic truth table for $p \vee q$, so the two statements are equivalent. 

(4a) $P(3)$ is true. $P(1)$ is false. 

(4b) We can run through a few values first: 

+ $P(1)$ is false because $1^2$ is not greater than or equal to $2^1$. 
+ $P(2)$ is true because $2^2$ is (greater than or) equal to $2^2$.
+ $P(3)$ is true because $3^2$ is greater than or equal to $2^3$.
+ $P(4)$ is true because $4^2$ is (greater than or) equal to $2^4$.
+ $P(5)$ is false because $5^2$ is not greater than or equal to $2^5$.
+ $P(6)$ is false because $6^2$ is not greater than or equal to $2^6$.

Somewhat informally, from here on out $2^n$ grows faster than $n^2$ because one is exponential and the other is polynomial, so we can expect $P(n)$ to continue to be false from here on. The truth set then is $\{2,3,4\}$. 


(4c) This is a proposition because the variable $x$ has been quantified ($\exists$). So it's now a statement that has a definite truth value regardless of the specific choice of $x$. (In fact the statement is true, because there does exist $x$ such that $P(x)$ is false; see part (a).) 

## Logic Level 2

(1a) Converse: If it is below freezing, then it is snowing outside. Contrapositive: If it is not below freezing, then it is not snowing outside. 

(1b) Converse: If $n$ is odd, then $n$ is a prime number. Contrapositive: If $n$ is even (or "not odd") then $n$ is not a prime number. 

(2) [Truth table here](http://www.wolframalpha.com/input/?i=truth+table+%28%28p+or+q%29+and+%28p+implies+r%29+and+%28q+implies+r%29%29+implies+r). Yes, this is a tautology. 

(3a) This is a true statement because there does indeed exist an $x \in \mathbb{N}$ such that $x^2 > x$, for example $x = 2$. 

(3b) The negation symbolically is $(\forall x)(\neg P(x))$. This would say in English: _For all natural numbers x, $x^2 \leq x$_. 