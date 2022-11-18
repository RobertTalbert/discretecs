**Proposition:** If $G$ and $H$ are isomorphic graphs and $G$ has a Hamiltonian cycle, then $H$ has a Hamiltonian cycle. (That is, the property of having a Hamiltonian cycle is an isomorphism invariant.) 

**Proof:** Suppose $G$ and $H$ are isomorphic and $G$ has a Hamiltonian cycle. Let's say that $G$ has $n$ vertices and that the Hamilton cycle, given as a sequence of vertices, is $v_1, v_2, v_3, \dots, v_n, v_1$. 

Since $G$ and $H$ are isomorphic, there is a bijection $f$ mapping the vertices of $G$ onto the vertices of $H$ in such a way that $(a,b)$ is an edge in $G$ if and only if $(f(a), f(b))$ is an edge in $H$. Because $f$ maps the vertices of $G$ to vertices in $H$, the outputs $f(v_1), f(v_2), \dots, f(v_n)$ are vertices in $H$. We claim that the sequence $f(v_1), f(v_2), \dots, f(v_n), f(v_1)$ is a Hamilton cycle in $H$. There are three things to show: (1) each vertex in this sequence is adjacent to the one before it in the sequence, (2) all vertices in $H$ are visited in this sequence, and (3) no vertex of $H$ is visited more than once in this sequence (except the starting and ending vertex). 

**Adjacency:** Take any two consecutive vertices in the sequence $v_1, v_2, v_3, \dots, v_n, v_1$, and call then $v_i$ and $v_{i+1}$. Then $(v_i, v_{i+1})$ is an edge in $G$. Therefore since $f$ is an isomorphism, $(f(v_i), f(v_{i+1}))$ is an edge in $H$. Therefore any consecutive vertices in the sequence $f(v_1), f(v_2), \dots, f(v_n), f(v_1)$ are adjacent. 

**Every vertex in $H$ is visited:** All the vertices in $G$ appear in the original sequence $v_1, v_2, v_3, \dots, v_n, v_1$. Since $f$ is a bijection, it is injective, and so if two different vertices are plugged into $f$, the outputs will also be different. Therefore all of the vertices $f(v_1), f(v_2), \dots, f(v_n)$ are different. Note that since $G$ and $H$ are isomorphic, we have previously shown they must have the same number of vertices. The graph $G$ has $n$ vertices; there are $n$ vertices in this sequence and they are all different. Therefore the sequence must contain all the vertices of $H$. 

**No vertex in $H$ is visited more than once:** Because there are *exactly* $n$ vertices in the sequence $f(v_1), f(v_2), \dots, f(v_n)$, none of the $n$ vertices of $H$ is duplicated. 

We have shown that $f(v_1), f(v_2), \dots, f(v_n), f(v_1)$ is a sequence of adjacent vertices in $H$ that visits every vertex and no vertex other than the start and end is visited more than once. This makes it a Hamilton cycle, which is what we wanted to prove. 
