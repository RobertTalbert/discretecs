# Selections from AEPs 

## AEP 4

### Why $n$ is an integer

The number $n$ is defined as $(ed-1)/M$. Replace $e$ and $d$ with their formulas: 
$$n = \frac{(AM+a)(BM+b) - 1}{M}$$
Now mutliply the top out: 
$$n = \frac{ABM^2 + AbM + aBM + ab  - 1}{M}$$
Now remember that $M = ab - 1$, so we can substitute the last two terms: 
$$n = \frac{ABM^2 + AbM + aBM + M}{M}$$
Every term in the numerator now has a factor of $M$ on it. Factoring this out and then dividing off, we get
$$n = ABM + Ab + aB$$
Since all the individual numbers on the right side are integers and we are just adding and multiplying them, the entire right side -- that is, $n$ -- is an integer. 



### Why Bob always gets the correct plaintext message 

Let $x$ be a number representing a block of plaintext that Alice is going to send. By the specifications of the encryption process, this is an integer greater than or equal to $0$ but less than $n$ (from Bob's public key). She computes $C = (ex) \, \% \, n$ and sends this to Bob. 

Bob takes this and computes $(Cd) \, \% \, n$. We want to show that this number equals $x$. 

Start by substituting $C$ with what it equals: 

$$((ex) \, \% \, n) \cdot d) \, \% \, n$$

Note that reducing an integer mod n twice gives the same result as reducing it mod n once, so we can ignore the `% n` in the first set of parentheses. This means Bob has 

$$((ex) \cdot d) \, \% \, n$$

This is the same as $(edx) \, \% \, n$ because multiplication is commutative and associative (we can ignore the inner parentheses and then multiply in a different order if we want). 

Now note that $n = (ed-1)/M$ by definition in the encryption system. Multiply both sides of this by $M$ and add $1$ to get $ed = Mn + 1$. Now substitute: 

$$(edx) \, \% \, n = ((Mn+1)x) \, \% \, n$$

Multiplying the $x$ through gives $(Mnx + x) \, \% \, n$. Now, the first part of the sum $Mnx$ is a multiple of $m$, so when reduced mod $n$, it becomes $0$. And, $x$ was selected so that it's less than $n$, so $x \, \% \, n = x$. Therefore 
$$((Mn+1)x) \, \% \, n = 0 + x = x$$
Which shows that Bob ends up with $x$, the same number that Alice encrypted. 