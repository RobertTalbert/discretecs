Welcome to the fifth and final video on counting complex arrangements. In the last video we made an important discovery -- that the number of k-element subsets of an n-element set is the same as the number of n-bit strings with weight k. In this video we're going to look at a third counting problem that seems totally unrelated to either of these, but see a familiar face in the results. This is going to lead us to define the all-important notion of the binomial coefficient. We'll end this video explaining what this binomial coefficient is and what it tells us. 

Let's go back to counting the k-element subsets of an n-element set. We know this number is Bnk, which is the same as the number of n-bit strings with weight k. If n is 5, this table here allows us to actually say what some of these numbers are -- B5,0 and B55 are 1 (which we also stated earlier when talking about bit strings), B5,1 and B54 are both 5, and B52 and B53 are both 10. 

Now let's look at something that on the surface appears completely different -- taking the algebraic expression x+y and raising it to the nth power. Here's what we get when n is 0, 1, 2, and 3 once we expand with algebra and simplify. Some things to notice here: 

First, the exponents on the individual terms add up to the power we're raising this to. For example in the last line the exponents always add up to 3. Second, each term has a number multiplied to it that we call the "coefficient". For example the coefficient on the x^2y term in the last line is 3. The coefficient o the x^3 term is 1 although we don't write it explicitly. 

Watch what happens as we take the powers higher. Let's look at (x+y)^5. when fully expanded it looks like this. Now, check out the coefficients on the terms. The coefficient on the x^5 and y^5 terms are 1 and although we don't usually write these, I've added them so you can see them. The coefficients on the x^4y and xy^4 terms are 5 and the coefficients on the x^2y^3 and 2^3y^2 terms are 10. 

Do you notice anything familiar? You should! These coefficients are exactly the number B50, B51, B52, and so on through B55 that we used to count k-element subsets and bit strings of weight k! Can this possibly be a coincidence, that the coefficient on the x^k term of (x+y)^n is Bnk? 

Let's see if we can understand this in a special case we haven't seen yet, namely (x+y)^10. Let C10,3 be the coefficient on the x^3 term in this expansion, and in general let Cnk be the coefficient on the x^k term in the expansion of (x+y)^n. 

Since the exponents on x and y have to add up to 10, the term is actually x^3 y^7. You can think of this coefficient as the number of x^3y^7's we would have in the final answer. Now (x+y)^10 is just 10 copies of (x+y) multiplied together so one way to expand (x+y)^10 is to first expand (x+y)^9 and then multiply the result by x+y. When you do, you're multiplying this huge thing by x, then by y, then adding the results. Where would one of the x^3y^7 terms come from? Well, it would either come from an x^2y^7 term in (x+y)^9 that was multiplied by x; or it would come from an x^3y^6 term that was multiplied by y. And it can't come from both. So the number of ways to get an x^3y^7 term the first way is C9,2 and the number of ways to get it from the second way is C9,3. 

Therefore C10,3 = C9,3 + C92. It's the same recurrence relation that we used to find n-bit strings of weight k. You can wrk out, althoguh we won't prove it here, that this relationship Cnk = Cn-1, k + Cn-1,k-1 holds in general

Furthermore the boundary conditions are the same --- Cnn = 1 because the coefficient on x^n in this expansion is always 1, similarly Cn0 is always 1. 

 -- So since the coefficients obey the exact same rules as Bnk, and they have the same boundary conditions, they are in fact the same numbers. 

So this number Bnk is counting a LOT of different things. It counts the number of k-element subsets of an n element set; the number of n-bit strings with weight k; and it gives us the coefficient on the x^k term in the expansion of (x+y)^n. Because of its centrality and versatility, we're going to give it a special name and notatio. 

We are going to now call this number the binomial coefficient, since we just saw that it gives us the coefficient on a term when we raise the binomial x+y to a power. We use this notation here, like a fraction but without the fraction bar, with n on top of k enclosed in parentheses. When we can't type it in nice looking notation like this, for example in Python, we just write binom(n,k). 

So the binomial coefficient counts all the items we have already seen in terms of subsets, bit strings, and coefficients. In general -- the binomial coefficient counts the number of ways to select k objects from a group of n objects. That's just another way of referrign to subsets. So sometimes we say that binomial coefficient of n and k is "n choose k" 

We also know from our earlier work that n choose k satisfies an important recursive property: namely that n choose k equals n-1 choose k plus n-1 choose k-1. Remember we got this by thinking about n-bit strings of weight k and where they come from. We also know some explicit values of n choose k, namely in the situation where k is n or 0, n choose k is 1. 

What we don't have yet is an explicit closed-form formula for n choose k, but that's coming soon, and it'll require us to go back and think about how k-element subsets of an n-element set were formed. For now, what's important isnt' so much how to compute n choose k, but rather these takeaways

First, n choose k is the solution to three different counting problems. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc4NDE1Mjg2NywtMTk0MjY2MDU2NCw0OT
gzMjAwODAsLTI1ODY1MjI1NiwtNzEyNDE0NjA4LC04MzUzNTM5
OTBdfQ==
-->