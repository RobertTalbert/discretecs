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


## C4 

1. $\emptyset$
2. $\lbrace u,v,x,y \rbrace$
3. $\lbrace y \rbrace$ 
4. $\lbrace o,p,q,w,x,y,z \rbrace$
5. $\lbrace o,p,q,r,s,t,u,v,w,x,y,z \rbrace$
6. $4$

## C5 

1. License plate problem with six slots to fill, 26 choices for each of the first two slots and 10 choices for each of the remaining four. So the total count is $26^2 \cdot 10^4 = 6760000$. 
2. License plate problem again, with restricted choices: We can only choose a letter for the second slot or digits for the first three of the four number slots. So the total count is $26 \cdot 10^3 = 26000$. 
3. Use the [Principle of Inclusion and Exclusion](https://publish.obsidian.md/mth225/Combinatorics/Principle+of+Inclusion+and+Exclusion): The number of ID's that start with a `Z` is $26 \cdot 10^4 = 260000$. The number of ID's that end in `69` is $26^2 \cdot 10^2 = 67600$. The number of ID's that do both, is $26 \cdot 10^2 = 260$; these have been double counted and so we need to subtract this from the sum, giving a total count of $260000 + 67600 - 260 = 327340$. 


## C6

1. (a) $7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5040$

   (b) $\displaystyle{\binom{500}{495} = \frac{500!}{495! \cdot 5!} = \frac{500 \cdot 499 \cdot 498 \cdot 497 \cdot 496}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}=  255244687600}$

2. (a) License plate problem with four people who could fill the first role, then three who could fill the second, then two for the third role, then just one for the last: $4 \cdot 3 \cdot 2 \cdot 1 = 24$. 

   (b) This is also a license plate problem, basically the same as part (a) only there are more people involved: 20 who could be elected into the first role, then 19 who could fill the second, then 18 for the third role, then 17 for the last: $20 \cdot 19 \cdot 18 \cdot 17 = 116280$. 



---

[Remember it's now our policy](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2024/assignments/checkpoints/Checkpoint%208%20guide.md) that we are no longer putting solutions for S1 and S2 on the guides. If you attempted these, just check your work using technology.

## S3 



## S4

 
## S5


## S6


## S7

## S8

## S9

## S10