Welcome to the fifth and final video on counting complex arrangements. In the last video we made an important discovery -- that the number of k-element subsets of an n-element set is the same as the number of n-bit strings with weight k. In this video we're going to look at a third counting problem that seems totally unrelated to either of these, but see a familiar face in the results. This is going to lead us to define the all-important notion of the binomial coefficient. We'll end this video explaining what this binomial coefficient is and what it tells us. 

Let's go back to counting the k-element subsets of an n-element set. We know this number is Bnk, which is the same as the number of n-bit strings with weight k. If n is 5, this table here allows us to actually say what some of these numbers are -- B5,0 and B55 are 1 (which we also stated earlier when talking about bit strings), B5,1 and B54 are both 5, and B52 and B53 are both 10. 

Now let's look at something that on the surface appears completely different -- taking the algebraic expression x+y and raising it to the nth power. Here's what we get when n is 0, 1, 2, and 3 once we expand with algebra and simplify. Some things to notice here: 

First, the exponents on the individual terms add up to the power we're raising this to. For example in the last line the exponents always add up to 3. Second, each term has a number multiplied to it that we call the "coefficient". For example the coefficient on the x^2y term in the last line is 3. The coefficient o the x^3 term is 1 although we don't write it explicitly. 

Watch what happens as we take the powers higher. Let's look at (x+y)^5. when fully expanded it looks like this. Now, check out the coefficients on the terms. The coefficient on the x^5 and y^5 terms are 1 and although we don't usually write these, I've added them so you can see them. The coefficients on the x^4y and xy^4 terms are 5 and the coefficients on the x^2y^3 and 2^3y^2 terms are 10. 

Do you notice anything familiar? You should! These coefficients are exactly the number B50, B51, B52, and so on through B55 that we used to count k-element subsets and bit strings of weight k! Can this possibly be a coincidence, that the coefficient on the x^k term of (x+y)^n is Bnk? 

Let's see if we can understand this in a special case we haven't seen yet, namely (x+y)^10. Let C10,3 be the coefficient on the x^3 term in this expansion. Since the exponents on x and y have to add up to 10, the term is actually x^3 y^7. You can think of this coefficient as the number of x^3y^7's we would have in t 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgzMDQ1NDc0NiwtMjU4NjUyMjU2LC03MT
I0MTQ2MDgsLTgzNTM1Mzk5MF19
-->