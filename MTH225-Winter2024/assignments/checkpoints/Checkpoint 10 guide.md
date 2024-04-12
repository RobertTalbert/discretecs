# Checkpoint 10 guide 

## C1

*"You'll hurt your eyes if you look directly at the sun*"

1. You look directly at the sun
2. You hurt your eyes
3. If you hurt your eyes, then you looked directly at the sun
4. If you didn't hurt your eyes, then you didn't look directly at the sun
5. If you didn't look directly at the sun, then you didn't hurt your eyes
6. You looked directly at the sun but didn't hurt your eyes

## C2

"For every integer $n \geq 1$, a set with $n$ elements has $2^n$ subsets"

1. The predicate is "a set with $n$ elements has $2^n$ subsets". 
2. $n = 1$ (The proposition is also true for $n=0$ but $n=1$ us the stated base case)
3. When $n=1$, we are looking at a set with one element, let's just call that $\lbrace x \rbrace$. This set has two ($2^1$) subsets: $\emptyset$, and the set itself $\lbrace x \rbrace$. Therefore the base case holds. 
4. Assume that for some positive integer $k$, a set with $k$ elements has $2^k$ subsets. 
5. Prove that a set with $k+1$ elements has $2^{k+1}$ subsets. 

(Bonus: A completed proof of this is [in the vault](https://publish.obsidian.md/mth225/Recursion+and+Induction/Mathematical+induction).) 

### Common mistakes: 

- **Not providing a complete and correct proof in the base case:** A complete and correct proof of the base case is required. Several responses *stated* that a one-element set has two subsets, but did not explain why. Merely asserting that the base case holds is not enough -- there needs to be an explanation, in the form of a direct demonstration, that proves the base case truly holds when $n=1$. 
- **Assuming in the inductive hypothesis that the predicate is true *for all* values of $k$**: As we've mentioned in class several times and in the class prep videos on this topic, assuming that the predicate holds "for all" values of $k$ is assuming the statement that you intend to prove, which is an invalid form of argumentation. 


## C3

Some explanations have been added; these are not necessary in your solutions. 

1. (a) True
   
   (b) False (The dots $\dots$ indicate that the pattern continues, but the pattern here is powers of 2, and 25 is not one of those)
   
   (c) False (There are no elements in the empty set)
   
   (d) True ([ $\emptyset$ is a subset of every set](https://publish.obsidian.md/mth225/Sets+and+Functions/Empty+set))

   (e) False (For example, $-1 \in \mathbb{Z}$ but $-1 \not \in \mathbb{N}$)

2. (a) $\lbrace 0, 4, 8, 12, 16, 20, \dots \rbrace$

   (b) Incorrect syntax ($2^n$ is a function, not a predicate; If mapping a function over a set, the function must come first -- like in part (a))

   (c) $\lbrace 1, 3, 5, 7, 9 \rbrace$ 

### Common mistakes

- **Having TRUE for 1(b):** See the guide above for an explanation. *However if this was the only thing wrong on the attempt, I counted it as a simple error* on the possibility that you confused squares with powers of 2. Don't do that again please! 


## C4 

1. $\emptyset$
2. $\lbrace u,v,x,y \rbrace$
3. $\lbrace y \rbrace$ 
4. $\lbrace o,p,q,w,x,y,z \rbrace$
5. $\lbrace o,p,q,r,s,t,u,v,w,x,y,z \rbrace$
6. $4$

### Common mistakes

- **Not finding the cardinality of the power set in part 6:** The power set itself is $\lbrace \emptyset, \lbrace x \rbrace, \lbrace y \rbrace, \lbrace x,y \rbrace \rbrace$. But it's asking for the cardinality, note the $| |$ signs. So it's 4. 
- ***Answering "3" for part 6:** The most likely explanation is forgetting that the empty set is a subset of $A$ and has to be included in the list of subsets. 

## C5 

1. License plate problem with six slots to fill, 26 choices for each of the first two slots and 10 choices for each of the remaining four. So the total count is $26^2 \cdot 10^4 = 6760000$. 
2. License plate problem again, with restricted choices: We can only choose a letter for the second slot or digits for the first three of the four number slots. So the total count is $26 \cdot 10^3 = 26000$. 
3. Use the [Principle of Inclusion and Exclusion](https://publish.obsidian.md/mth225/Combinatorics/Principle+of+Inclusion+and+Exclusion): The number of ID's that start with a `Z` is $26 \cdot 10^4 = 260000$. The number of ID's that end in `69` is $26^2 \cdot 10^2 = 67600$. The number of ID's that do both, is $26 \cdot 10^2 = 2600$; these have been double counted and so we need to subtract this from the sum, giving a total count of $260000 + 67600 - 2600 = 325000$. 

### Common mistakes

- **Computing *only* the 2600 in part 3:** 2600 is the number of ID's that satisfy *both* conditions. But we are asked for the number of ID's that satisfy one or the other, or both conditions. This is where the [Principle of Inclusion and Exclusion](https://publish.obsidian.md/mth225/Combinatorics/Principle+of+Inclusion+and+Exclusion) comes in. 



## C6

1. (a) $7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5040$

   (b) $\displaystyle{\binom{500}{495} = \frac{500!}{495! \cdot 5!} = \frac{500 \cdot 499 \cdot 498 \cdot 497 \cdot 496}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}=  255244687600}$

2. (a) License plate problem with four people who could fill the first role, then three who could fill the second, then two for the third role, then just one for the last: $4 \cdot 3 \cdot 2 \cdot 1 = 24$. Or just think of it as the number of ways to permute (rearrange) four people, which we know is $4!$.  

   (b) This is also a license plate problem, basically the same as part (a) only there are more people involved: 20 who could be elected into the first role, then 19 who could fill the second, then 18 for the third role, then 17 for the last: $20 \cdot 19 \cdot 18 \cdot 17 = 116280$. You can also think of this as the permutation $P(20,4) = \frac{20!}{16!}$. 

### Common mistakes

- **Using the binomial coefficient on 2(b)**: In particular computing $\binom{20}{4}$. This number 
($4845$) counts the number of ways to select 4 people from 20, without any other restrictions on the selection. But we *do* have a restriction on the selections: One person has to be president, another vice-president, and so on. Rearranging the people in a given selection produces a different outcome. (As noted in class: If we swapped the President and Vice President of the USA, it would matter!) The binomial coefficient ignores the ordering of the selection. Sometimes that is appropriate, this time it is not. 


**Handling numerical computation issues on 1(b):** Attempting to compute $\binom{500}{495}$ by first computing $500!$ and then $495! \cdot 5!$ will lead to an overflow error because those numbers have 1135 and 1123 digits respectively. So you must simplify the fraction first by canceling factorials. Responses that did not attempt to simplify, or simplified incorrectly, or used the closed formula incorrectly, were Unsuccessful attemtpts. 

But here, even if you do simplify, it turns out that many hand calculators cannot give $\frac{500 \cdot 499 \cdot 498 \cdot 497 \cdot 496}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}$ as an integer -- only in scientific notation. Leaving the answer in scientific notation is not allowed. However on this one Checkpoint, if you left the answer in scientific notation and there were otherwise no errors, I counted it as a "simple" error and the attempt is Successful. 

If this happens again there are simple computational workarounds: 
- *You can simpify term by term*: For example there is a 500 in the numerator and both a 5 and a 2 in the denominator; 500 divided by (5 times 2) is 50. Likewise 496 divided by 4 is 124, and 498 divided by 3 is 166. So the answer would simplify to $50 \cdot 499 \cdot 166 \cdot 497 \cdot 124$ which is correct and something most calculators should handle. 
- *You can recognize that the last two digits of the answer must be "00"* because of the factor of 500 on the numerator. Taking the scientific notation answer from a calculator and dividing by 100 should yield a plain integer. 
- *You can just switch technologies and use a smartphone app*. These are allowed, if the phone is in airplane mode, and the vast majority handle large numbers better than hand calculators. 


---

[Remember it's now our policy](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 



## S4

1. (a) False

   (b) False 

   (c) False (The statement is saying that "All integers have something other than three digits", i.e. "three digit integers do not exist" which is plainly false) 

   (d) False (In fact there are no integers whose squares end in a 3! An explanation is below.)

2. (*Several different correct formulations are possible, here is one*) "At least one of the times I answered this question, it was correct" 

*Bonus explanation for why there is no integer whose square ends in a 3*: When you square an integer you are multiplying it by itself. The ones digit of the result, is the same as  when you take just the ones digit of the original and square that. (Example: The ones digit of $8919234^2$ is the ones digit of $4^2$ which is $6$.) That ones digit can only be one of the integers 0 through 9 and when squared, the only outcomes in the ones digit are 0, 1, 4, 5, 6, or 9.  
 
## S5

- $a_2 = 2a_1 - 3a_0 = 2(6) - 3(3) = 3$
- $a_3 = 2a_2 - 3a_1 = 2(3) - 3(6) = -12$
- $a_4 = 2a_3 - 3a_2 = 2(-12) - 3(3) = -33$
- $a_5 = 2a_4 - 3a_3 = 2(-33) - 3(-12) = -30$
- $a_6 = 2a_5 - 3a_4 = 2(-30) - 3(-33) = 39$


## S6

1. $R(1) = 5$, $R(2) = 7$, $R(3) = 9$
2. The figure in any given step is obtained by taking the figure from the previous step and inserting a single column of two blocks between column 1 (which has three blocks) and column 2. The number of blocks inserted appears to always be 2. So the recurrence relation should be $R(n) = R(n-1) + 2$. 

### Common mistakes: 

- **Giving a numerical, not visual explanation:** As the success criteria state, the explanation has to be based on the visual pattern and not on a guess at a numerical pattern. Computing $R(1) = 5$, $R(2) = 7$,and $R(3) = 9$ and then stating something like "Clearly the pattern is that the outputs go up by two each time" is not a visual explanation, it is a guess at the numerical pattern. 

## S7

1. Function. Domain = $\lbrace b,p,s,q \rbrace$. Codomain = $\lbrace 7,2,9,6,8 \rbrace$. Range = $\lbrace 9,6,8 \rbrace$.   
2. Function. Domain = $\lbrace 2,9 \rbrace$. Codomain = $\lbrace m,t,r,i,v \rbrace$. Range = $\lbrace m,r \rbrace$.
3. Not a function. 
4. Function. Domain = $\lbrace 5,1,3,0 \rbrace$. Codomain = $\lbrace z,i,y,b,j \rbrace$. Range = $\lbrace z,y,b,j \rbrace$.
5. Function. Domain = $\lbrace 3,2,1,6 \rbrace$. Codomain = $\lbrace 8,6,0 \rbrace$. Range = $\lbrace 8,6,0 \rbrace$.
6. Function. Domain = $\lbrace s,g \rbrace$. Codomain = $\lbrace 6,0,2,1 \rbrace$. Range = $\lbrace 0,1 \rbrace$.


## S8

1. Bijection. 
2. The function is not injective because, for example, $f(-1)$ and $f(1)$ are equal to $1$. The function is also not surjective because the square of an integer is always nonnegative, so for example $-2$ will never be output. 
3. The function is injective. (There are no negative numbers this time to cause a collision.) However the function is not surjective because only perfect squares are output, which excludes numbers like $2$. 

## S9

| Part | Type of sequence | Closed formula | Recursive definition | 
| --- | ---- | ---- | --- | 
| 1 | Arithmetic | $a(n) = 4 - 2n$ | $a_0 = 4, a_n = a_{n-1} - 2$ | 
| 2 | Geometric | $a(n) = 5^n$ | $a_0 = 1, a_n = 5a_{n-1}$ | 
| 3 | Neither | n/a | n/a | 
| 4 | Arithmetic | $a(n) = 4 - 0.1n$ | $a_0 = 4, a_n = a_{n-1} - 0.1$ | 


## S10