# Checkpoint 8 guide

**Note about Skills S1 and S2:**  From now on, these guides will not contain answers or common mistakes for Skills S1 or S2. At this point very few, if any students are reattempting these skills; and if you are attempting them, you can easily check your work with an online calculator. 

## Skill S3

## Skill S4

## Skill S5

## Skill S6

1. $R(1) = 4$, $R(2) = 10$, $R(3) = 20$, $R(4) = 34$. 
2. (There are multiple correct ways to think about the visual pattern; here is one.) In each step of the pattern there is a small column of two flowers that always appears on the right, next to a rectangle that's growing. In step 1, the rectangle is $2 \times 1$. Step 2 can be visualized by taking the rectangle from step 1 and first adding a new column of flowers on the left side whose height is double the step number: 

And then adding a single layer of flowers that's 2 levels tall and has a width equal to one less than the step number: 


The addition of the column adds $2n$ flowers to the picture; the addition of the extra layer on top adds $2(n-1)$. Therefore the recurrence relation would be: 

$$R(n) = R(n-1) + 2n + 2(n-1) \ \text{or} \ R(n) = R(n-1) + 4n -2$$



## Skill S7

1. Not a function (because $o$ maps to two things)
2. Function. Domain = $\lbrace 8,0,9,4,3 \rbrace$. Codomain = $\lbrace 7,0,8,3,6 \rbrace$. Range = $\lbrace 7,8,3\rbrace$. 
3. Not a function (because $4$ maps to two things)
4. Not a function (because $j$ maps to two things)
5. Function. Domain = $\lbrace m,y,n \rbrace$. Codomain = $\lbrace r,g,k,s \rbrace$. Range = $\lbrace g,k,s \rbrace$.
6. Not a function (because $l$ doesn't map to anything) 

## Skill S8

1. This function is a bijection. 
2. This function is neither injective nor surjective. It's not injective because for example, `1011` and `0011` both map to `0011`. It's not surjective because none of the bits that start with a `1`, such as `1111`, can be hit. 
3. This function is injective, but not surjective. It's not surjective because $-1$ has no corresponding input, in fact none of the negative integers do. 

### Common mistakes

- **Stating that the function in item 2 is surjective:** It's not, see above for the reasons. 
- **Stating that the function in item 2 is injective:** It's not, see above for the reasons. 
