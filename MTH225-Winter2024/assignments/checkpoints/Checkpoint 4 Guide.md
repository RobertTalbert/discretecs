# Checkpoint 4 Guide 

## S1

1. $43969$
2. $16D$
3. $110100100$
4. `1011 0011`

## S2

1. `01001011`
2. `010001`
3. `011100110`
4. `01111`, remainder `1`

## S3

## S4 

*Note*: Explanations are provided for part 1. These are not required for your work; they're only here for study purposes so you can see why the statements are true or false. 

1. (a) False (because $9^2 = 81$ which is not greater than 100)

   (b) True (because $9^3 = 729$)

   (c) False (because part (a) is a counterexample)

   (d) True (because there does exist an $x$ such that $x^3$ is not odd, for example $x=2$)

2. *No dogs are poodles*  (Note, this isn't the same as "putting 'not' or 'it is not the case that' in front of the statement. If it's too close for comfort you could also say something like *All dogs are non-poodles*.)

### Common mistakes

- **Stating that "Some dogs are not poodles" as the negation:** The statement "Some dogs are not poodles" is not the negation of "Some dogs are poodles" because both of those statements are true at the same time. 

## S5

*Note*: I actually used, and will continue to use, a less stringent set of success criteria -- namely that if you make an arithmetic mistake and get one of the intermediate results wrong, it counts as a "simple" error as long as the remaining values are computed using the correct recursion rules and the answers are consistent with the mistake. For example if you computed $a_5$ as 180 instead of 169, but then used that mistake to get $a_6 = 2(180) + 70 = 430$ and then $a_7 = 2(430) + 180 = 1040$, the solution is considered "successful" despite the mistake. One such error is allowed. 

- $a_2 = 2a_1 + a_0 = 2 \cdot 5 + 2 = 12$
- $a_3 = 2a_2 + a_1 = 2 \cdot 12 + 5 = 29$ 
- $a_4 = 2a_3 + a_2 = 2 \cdot 29 + 12 = 70$
- $a_5 = 2a_4 + a_3 = 2 \cdot 70 + 29 = 169$  
- $a_6 = 2a_5 + a_4 = 2 \cdot 169 + 70 = 408$
- $a_7 = 2a_6 + a_5 = 2 \cdot 408 + 169 = 985$  


## S6

1. $R(1) = 1$
2. For $n > 1$ the recurrence relation is $R(n) = R(n-1) + n$. That's because what appears to be happening is that in step $n$, we're using the figure from step $n-1$ and then adding a number of footballs to the image equal to the number of the new step -- 2 footballs added in step 2, 3 in step 3 and so on. 

### Common mistakes 

- **On part 2, explaining how the visual pattern works without providing the recurrence relation:** Basically what you see above minus the first sentence. Correct and clear explanations are good (and required here) but there also has to be a recurrence relation -- a precise mathematical equation that relates $R(n)$ to one or more previous values of $R$. 
- **Writing a recurrence relation that produces incorrect results:** For example $R(n) = R(n-1) + (n + 1)$ is a valid recurrence relation (because it's a precise equation that relates $R(n)$ to one or more previous values of $R$) but it does not match the situation. If you use this recurrence relation to generate a few values starting with $R(1) = 1$, then you would get $R(2) = R(1) + 2 + 1 = 1 + 2 + 1 = 4$ which is incorrect because there are three footballs in figure 2, not four. Remember, **always do a BS check on your work** before turning it in to catch errors like this -- in this case an easy way to do it is use the recurrence relation to generate the first 3 values and see if they match the pictures. 