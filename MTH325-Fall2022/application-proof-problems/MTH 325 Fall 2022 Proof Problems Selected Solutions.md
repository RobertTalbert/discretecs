---
tags: mth325-f22
---

# MTH 325 Fall 2022 Proof Problems Selected Solutions




## Problem 2

*[Click here](https://hackmd.io/QTmHZqZgTiSbSzKO2Vwbfg?both#Problem-2) for the problem itself*

**Proof:** We prove this by induction. The base case is $n=1$. In this case, the function would return `0` because of the first part of the `if` statement. And, we can calculate that $\lfloor \log_2(1) \rfloor = \lfloor 0 \rfloor = 0$. So the base case holds. 

Now suppose that for some positive integer $k$, the function returns $\lfloor \log_2(k) \rfloor$ when we input `k`. Note: This is equivalent to saying that the function returns $\lfloor \log_2(m) \rfloor$ when we input `m` for *any* value of $m$ less than or equal to $k$. We want to show that the function returns  $\lfloor \log_2(k+1) \rfloor$ when we input `k+1`. 

We may assume that $k > 1$ since we already handled the case where $k = 1$. Therefore when given an input of `k+1`, the function will default to the `else` branch of the `if-then` statement and recursively compute `L = r((k+1)//2)`. Now the value of `(k+1) // 2` is an integer that is less than or equal to `k`. Therefore, by the induction hypothesis, `r((k+1)//2)` evaluates to 

$$\left \lfloor \log_2\left( \frac{k+1}{2} \right) \right \rfloor$$

Look at the logarithm expression. By the properties of logarithms, this equals 

$$\log_2 (k+1) - \log_2(2)$$ 

And this equals 

$$\log_2 (k+1) - 1$$ 

Therefore, after the recursive call, the function has set $L$ equal to 

$$L = \left \lfloor \log_2\left( \frac{k+1}{2} \right) \right \rfloor = \lfloor \log_2 (k+1) - 1 \rfloor$$

You can prove (see additional proof problem!) that for any $x$, $\lfloor x - 1 \rfloor = \lfloor x \rfloor - 1$, Therefore 

$$L = \lfloor \log_2 (k+1) \rfloor - 1$$

The Python function returns $L + 1 = \lfloor \log_2 (k+1) \rfloor - 1 + 1 = \lfloor \log_2 (k+1) \rfloor$, which is what we wanted. :black_medium_square: 


## Problem 4

:::info
Prove that, for all positive integers $n$, the number of bits needed to represent $n$ in binary (base 2) is $1 + \lfloor \log_2(n) \rfloor$, that is, the logarithm base 2 of $n$ rounded down to the next lowest integer, plus 1. 
:::

**Proof:** We prove this with induction. The base case is $n=1$. Its binary representation is `1`, so only one bit is needed. And according to the formula, 

$$1 + \lfloor \log_2(1) \rfloor  = 1 +  \lfloor 0 \rfloor = 1$$

The two agree, so the base case holds. 

Now suppose that for some positive integer $k$, the number of bits needed to represent $k$ is $1 + \lfloor \log_2(k) \rfloor$. We want to show that the number of bits needed to represent $k+1$ is $1 + \lfloor \log_2(k+1) \rfloor$. 

Dividing $k+1$ by $2$ results gives a number whose binary representation consists of all the bits in the representation of $k+1$ *except* for the rightmost bit (which will be `0` if $k+1$ is even, and `1` if $k+1$ is odd). So the binary representation of $k+1$ requires a number of bits equal to the number of bits needed to represent $(k+1)/2$, plus one more to cover the rightmost bit. By the induction hypothesis, the first quantity is $1 + \left \lfloor \log_2\left(\frac{k+1}{2}\right)\right \rfloor$. So the total number of bits needed for $k+1$ is: 
$$ 1 + \left \lfloor \log_2\left(\frac{k+1}{2}\right)\right \rfloor + 1$$
This equals 
$$ 1 + \left \lfloor \log_2(k+1) - \log_2(2) \right \rfloor + 1$$
which equals 
$$ 1 + \left \lfloor \log_2(k+1) - 1 \right \rfloor + 1$$
which equals 
$$ 1 + \left \lfloor \log_2(k+1) \right \rfloor -1 + 1 = 1 + \left \lfloor \log_2(k+1) \right \rfloor$$
Which is what we wanted to prove. :black_medium_square: 


## Problem 6

:::info
**Conjecture:** For all positive integers $n$, $Q_n$ has $n \cdot 2^{n-1}$ edges. 
:::


**Proof:** The vertices of $Q_n$ are all the $n$-bit strings, and there are $2^n$ of those (that's a basic fact from MTH 225). Each node is connected to another node if the two differ in exactly one bit. There are $n$ bits available where a node could differ from another, so each node is connected to $n$ others. This means that $\deg(v) = n$ for all vertices $v$. Therefore if we sum up all those degrees, we get: 
$$\sum_{v \in V} n = \underbrace{n+n+n+\cdots+n}_{2^n \ \text{times}} = n \cdot 2^n$$
The Handshaking Lemma says that this sum is twice the number of edges, so the number of edges in $Q_n$ is half of this: 
$$|E| = \frac{n \cdot 2^n}{2} = n \cdot 2^{n-1}.$$
:black_medium_square: 

**Bonus second proof using induction:** The base case is $n=1$. The nodes in the graph $Q_1$ are just `0` and `1` (the strings of length 1) and these are connected by an edge because they differ in exactly one bit. So the number of edges is 1, and we see that $1 \cdot 2^{1-1} = 1 \cdot 2^0 = 1$. 

Now assume that for a positive integer $k$, the number of edges in $Q_k$ is $k \cdot 2^{k-1}$. We want to show that the number of edges in $Q_{k+1}$ is $(k+1) \cdot 2^k$. 

The vertices of $Q_{k+1}$ are all the $(k+1)$-bit strings. Consider the subgraph of $Q_{k+1}$ consisting of all the vertices whose bit strings begin (on the left) with `0` and all the edges connecting those vertices. This graph is isomorphic to $Q_k$ by the function that takes a $(k+1)$-bit string and maps it to its rightmost $k$ bits. Therefore, this subgraph has $k \cdot 2^{k-1}$ edges by the inductive hypothesis. 

Similarly, the induced subgraph whose vertices are the bit strings beginning with a `1` is isomorphic to $Q_k$, and therefore it too has $k \cdot 2^{k-1}$ edges. 

Note that neither of these two subgraphs have any vertices in common, since any vertex from the first must differ from all vertices in the second in the leftmost bit.

Finally, note that there is an edge in $Q_{k+1}$ from every vertex in the first subgraph to a single vertex in the second subgraph, connecting vertices that have the same bitstring except for their leftmost bit. 

The number of edges in each subgraph is $k \cdot 2^{k-1}$, and there are $2^k$ edges *between* the subgraphs --- one per vertex. Therefore the total number of edges in $Q_{k+1}$ is: 



$$k \cdot 2^{k-1} + k \cdot 2^{k-1} + 2^k$$

which equals: 

$$2k \cdot 2^{k-1} + 2^k$$

which equals: $$k \cdot 2^k + 2^k$$ 
which equals $(k+1) \cdot 2^k$, which is what we wanted. :black_medium_square: 


## Problem 14

:::info
Let $Q_n$ be the hypercube graph, and let $H$ be the subgraph whose vertices are the bitstrings whose leftmost bit is `0` and whose edges are all the pre-existing edges between those vertices. Prove that $H$ is isomorphic to $Q_{n-1}$. 
:::

**Proof:** Let $f$ be the function from the set of vertices of $H$ to the vertices of $Q_{k-1}$ that takes a vertex from $H$ and removes the leftmost bit. We want to show that (1) this function is injective, (2) this function is surjective, and that (3) $(a,b)$ is an edge in $H$ if and only if $(f(a), f(b))$ is an edge in $Q_{k-1}$. 

1. *$f$ is injective:*  Let $a$ and $b$ be two different vertices in $H$. We need to show $f(a) \neq f(b)$. Well, since $a$ and $b$ are in $H$ it means that the leftmost bits of each of those is `0`. So, if $a$ and $b$ are different, they must differ in a bit other than the leftmost one. But $f(a)$ and $f(b)$ are the same bitstrings with the left bit removed, so if $a$ and $b$ different some bit besides the leftmost one, they will still differ once the leftmost bit is removed. So $f(a) \neq f(b)$. 

2. *$f$ is surjective:* Let $v \in Q_{k-1}$. We need to show there exists $a \in H$ such that $f(a) = v$. We can easily construct this $a$ by appending `0` onto the left end of the bitstring for $v$. 

3. *$f$ preserves edges:* Suppose $(a,b)$ is an edge in $H$. Then $H$ is an edge in $Q_k$ as well; and this edge exists only if $a$ and $b$ differ in exactly one bit. This bit must not be the leftmost one, since the leftmost bits of $a$ and $b$ are both `0`. So $f(a)$ and $f(b)$ differ by one bit, and hence $(f(a), f(b))$ is an edge in $Q_{k-1}$. Conversely, suppose $(u,v)$ is an edge in $Q_{k-1}$. Then the bitstrings for $u$ and $v$ differ in exactly one bit. Let $a$ be the bitstring obtained by appending `0` on to the left of $u$; likewise let $b$ be the bitstring obtained by appending `0` on to the left of $v$. Then $a,b \in H$ and they differ in exactly one bit, hence $(a,b)$ is an edge in $H$. 
:black_medium_square: 

<!-- ## Problem 16

:::info
For all real numbers $x$, $\lfloor x - 1 \rfloor = \lfloor x \rfloor - 1$. (Here, $\lfloor x \rfloor$ is the "floor function".)
:::

By definition, $\lfloor x-1 \rfloor$ is the greatest integer less than or equal to $x-1$. Therefore $\lfloor x-1 \rfloor + 1$ is the greatest integer less than or equal to $x$. That is,

$$\lfloor x-1 \rfloor + 1 = \lfloor x \rfloor$$

Subtracting $1$ from both sides gives the result we want. :black_medium_square:  -->