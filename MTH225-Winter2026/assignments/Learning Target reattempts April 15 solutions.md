# MTH 225: Learning Target Reattempts from April 15  – Solution Guide
## 2026-04-15 | Learning Targets 5, 6, 7, 9, 10, 11

*Instructor-facing document. Includes grading notes and common error flags.*

---

## Learning Target 5

> I can construct a correct truth table for a proposition with two or three variables and use truth tables to determine if two such propositions are logically equivalent.

---

**Problem 1.** Truth table for $p \wedge (\neg q)$.

| $p$ | $q$ | $\neg q$ | $p \wedge (\neg q)$ |
|-----|-----|----------|---------------------|
| T   | T   | F        | F                   |
| T   | F   | T        | T                   |
| F   | T   | F        | F                   |
| F   | F   | T        | F                   |

---

**Problem 2.** Truth table for $(p \wedge q) \rightarrow \neg r$.

| $p$ | $q$ | $r$ | $p \wedge q$ | $\neg r$ | $(p \wedge q) \rightarrow \neg r$ |
|-----|-----|-----|--------------|----------|-----------------------------------|
| T   | T   | T   | T            | F        | F                                 |
| T   | T   | F   | T            | T        | T                                 |
| T   | F   | T   | F            | F        | T                                 |
| T   | F   | F   | F            | T        | T                                 |
| F   | T   | T   | F            | F        | T                                 |
| F   | T   | F   | F            | T        | T                                 |
| F   | F   | T   | F            | F        | T                                 |
| F   | F   | F   | F            | T        | T                                 |

---

**Problem 3.** Are $\neg p \vee \neg q$ and $\neg(p \wedge q)$ logically equivalent?

| $p$ | $q$ | $\neg p$ | $\neg q$ | $\neg p \vee \neg q$ | $p \wedge q$ | $\neg(p \wedge q)$ |
|-----|-----|----------|----------|----------------------|--------------|---------------------|
| T   | T   | F        | F        | F                    | T            | F                   |
| T   | F   | F        | T        | T                    | F            | T                   |
| F   | T   | T        | F        | T                    | F            | T                   |
| F   | F   | T        | T        | T                    | F            | T                   |

**Conclusion:** The two propositions have identical truth values in every row, so **yes, they are logically equivalent.** (This is one of De Morgan's Laws.)

> **Grading notes:**
> - The intermediate columns ($\neg p$, $\neg q$, $p \wedge q$) must be present and correct for Master.
> - Up to 2–3 cell-level errors are allowed across all three parts combined before dropping to Proficient.
> - A student who correctly identifies logical equivalence in Part 3 but has a few errors in interior columns can still earn Master if the errors are clearly minor (e.g., one wrong cell propagated consistently).
> - **Common error:** Forgetting that $p \rightarrow q$ is only false when $p$ is T and $q$ is F. Watch for students who mark the conditional F whenever either operand is F.

---

## Learning Target 6

> I can determine if an object is an element of a set, whether one set is a subset of (or equal to) another, and convert a set from set-builder notation to roster notation.

---

**Problem 1.** True or False:

| Statement | Answer | Brief reason |
|-----------|--------|--------------|
| $5 \in \lbrace 1 , 3, 5, 7, 9 \rbrace$ | **TRUE** | 5 is explicitly listed |
| $\mathbb{N} \subseteq \mathbb{Z}$ | **TRUE** | Every natural number is an integer |
| $\lbrace a, b \rbrace = \lbrace b, a, a \rbrace$ | **TRUE** | Sets do not contain duplicates; $\lbrace b,a,a \rbrace = \lbrace a,b \rbrace$ as a set.



| Statement | Answer |
|-----------|--------|
| $\lbrace2, 4\rbrace \subseteq \lbrace1, 2, 3, 4, 5\rbrace$ | **TRUE** |
| $\emptyset \subseteq \emptyset$ | **TRUE** — the empty set is a subset of every set, including itself |

**Summary of answers:** T, T, T, T, T

---

**Problem 2.** Roster notation:

**(a)** $\lbrace n \in \mathbb{Z}  :  n^2 \leq 16 \rbrace$

The integers whose square is at most 16: $n^2 \leq 16 \Rightarrow -4 \leq n \leq 4$.

$$\lbrace-4, -3, -2, -1, 0, 1, 2, 3, 4\rbrace$$

**(b)** $\lbrace k \in \lbrace 0, 1, 2, 3, 4, 5\rbrace :  k \pmod{3} = 1 \rbrace$

$$\lbrace1, 4\rbrace$$

> **Grading notes:**
> - For (a), students must include negative integers. Omitting negatives (writing $\lbrace 0,1,2,3,4\rbrace$) is a significant error — it shows misunderstanding of $\mathbb{Z}$.
> - For (b), methodical checking of each element is expected (or can be inferred). A bare answer of $\lbrace 1,4\rbrace$ with no work shown is a minor concern; if everything else looks solid, it's fine.

---

## Learning Target 7

> (**CORE**) I can find the union, intersection, difference, and Cartesian product of two sets and the complement, cardinality, and power set of a single set.

Sets: $A = \lbrace 1,2,3,4,5,6\rbrace$, $B = \lbrace 1,3,5,7,9\rbrace$, $C = \lbrace 2,4,6,8\rbrace$, $U = \lbrace 1,2,3,4,5,6,7,8,9,10\rbrace$

---

**Problem 1.**

**(a)** $A \cup B = \lbrace 1, 2, 3, 4, 5, 6, 7, 9\rbrace$

**(b)** $A \cap C = \lbrace 2, 4, 6\rbrace$

**(c)** $B - C$: elements in $B$ not in $C$. $B = \lbrace1,3,5,7,9\rbrace$, $C = \lbrace 2,4,6,8\rbrace$. No overlap.
$$B - C = \lbrace 1, 3, 5, 7, 9\rbrace$$

**(d)** $C - B$: elements in $C$ not in $B$. Same reasoning — no overlap.
$$C - B = \lbrace 2, 4, 6, 8\rbrace$$

---

**Problem 2.** $B^c$ (complement of $B$ w.r.t. $U$): elements of $U$ not in $B$.

$U = \lbrace 1,2,3,4,5,6,7,8,9,10\rbrace$, $B = \lbrace 1,3,5,7,9\rbrace$

$$B^c = \lbrace 2, 4, 6, 8, 10\rbrace$$

---

**Problem 3.** $\lbrace a, b\rbrace \times \lbrace 1, 2, 3\rbrace$

$$\lbrace (a,1),\ (a,2),\ (a,3),\ (b,1),\ (b,2),\ (b,3)\rbrace$$

---

**Problem 4.** $\mathcal{P}(\lbrace0,1\rbrace)$

$$\mathcal{P}(\lbrace 0,1\rbrace) = \lbrace \emptyset,\ \lbrace 0\rbrace,\ \lbrace 1\rbrace,\ \lbrace 0,1\rbrace\rbrace$$

> **Grading notes:**
> - Cartesian product elements must be written as **ordered pairs**, not sets. Writing $\lbrace a,1\rbrace$ instead of $(a,1)$ is a significant error.
> - The power set must include $\emptyset$ and the full set itself. Omitting either is a significant error.
> - Up to 2 minor errors allowed overall (e.g., a single element accidentally omitted from a union/intersection).
> - **Common error on (c)/(d):** Students sometimes confuse set difference with intersection. $B - C$ is not $B \cap C$.

---

## Learning Target 9

> (**CORE**) I can state the predicate, prove the base case, state the inductive hypothesis, and describe the inductive step for a mathematical proposition to be proven by induction.

**Proposition:** For all integers $n \geq 0$, $5$ divides $6^n - 1$.

---

**Problem 1. Base case.**

The base case corresponds to $n = 0$.

Check: $6^0 - 1 = 1 - 1 = 0$. Since $5$ divides $0$ (because $0 = 5 \cdot 0$), the base case holds. ✓

---

**Problem 2. Inductive hypothesis.**

Assume that for some integer $k \geq 0$, $5$ divides $6^k - 1$.

Equivalently: assume $(6^k - 1) \pmod{5} = 0$, or that $6^k - 1 = 5m$ for some integer $m$.

---

**Problem 3. Inductive step.**

Show that $5$ divides $6^{k+1} - 1$.

(Students are not required to complete the proof — they only need to state what must be shown.)

> **For the instructor's reference, here is the proof of the inductive step:**
> $$6^{k+1} - 1 = 6 \cdot 6^k - 1 = 6 \cdot 6^k - 6 + 5 = 6(6^k - 1) + 5$$
> By the inductive hypothesis, $5 \mid (6^k - 1)$, so $5 \mid 6(6^k-1)$. And clearly $5 \mid 5$. Therefore $5 \mid 6^{k+1}-1$. $\square$

> **Grading notes:**
> - The base case value is $n = 0$. Students who say $n = 1$ and then verify $6^1 - 1 = 5$ (which is also divisible by 5) are making a minor error on the base case value, but only if their verification is consistent with their stated value. If the problem said $n \geq 1$ this would be correct; since it says $n \geq 0$, the correct base case is $n = 0$.
> - The inductive hypothesis must say "for **some** $k$" (existential), not "for **all** $k$" (universal). Using a universal quantifier here is a minor error.
> - The inductive step must clearly state: prove that $5$ divides $6^{k+1} - 1$. Vague statements like "show it works for $k+1$" are acceptable if it's clear they mean the right thing.

---

## Learning Target 10

> (**CORE**) I can solve simple counting problems that involve a mixture of the Additive Principle, Multiplicative Principle, and Principle of Inclusion and Exclusion.

---

**Problem 1.** Coffee shop: 3 sizes, 5 espresso drinks, 4 teas. Customer chooses exactly one drink.

The customer is choosing from $5 + 4 = 9$ drink types (espresso or tea), and then independently choosing a size... 

> **Careful reading note:** The problem says "3 sizes, 5 types of espresso drink, and 4 types of tea" and asks for ways to choose "exactly one drink." The most natural interpretation is: size × drink type. So the answer is $3 \times (5 + 4) = 3 \times 9 = 27$.
>
> However, a student might reasonably read this as: just pick one item from the combined menu (ignoring size), giving $5 + 4 = 9$ by the **Additive Principle**. This interpretation is also defensible if size is considered fixed or irrelevant. 
>
> **Grading recommendation:** Accept either $27$ (Multiplicative + Additive) or $9$ (Additive alone), as long as the student clearly names and correctly applies the principle(s). The key is correct reasoning, not a unique answer.

**Intended answer:** $3 \times (5 + 4) = \mathbf{27}$, using the **Additive Principle** (to combine drink types) and the **Multiplicative Principle** (to combine with size choice).

---

**Problem 2.** Password: 2 distinct uppercase letters, then 4 digits (repeated allowed).

- Choose 1st letter: 26 options
- Choose 2nd letter (distinct): 25 options
- Choose each of 4 digits: 10 options each

Total: $26 \times 25 \times 10^4 = 650 \times 10000 = \mathbf{6{,}500{,}000}$

By the **Multiplicative Principle**.

---

**Problem 3.** Integers from 1 to 200 divisible by 4 or by 6. Use **Inclusion-Exclusion**.

- Divisible by 4: $\lfloor 200/4 \rfloor = 50$
- Divisible by 6: $\lfloor 200/6 \rfloor = 33$
- Divisible by both (LCM of 4 and 6 is 12): $\lfloor 200/12 \rfloor = 16$

By PIE: $50 + 33 - 16 = \mathbf{67}$

> **Grading notes:**
> - Problem 1: Accept reasonable interpretations as long as the named principle matches the computation.
> - Problem 2: A common error is using $26 \times 26$ (forgetting "distinct"). This is a significant error. Another is computing $10^4 = 1000$ instead of $10000$ — that's a computational error (minor).
> - Problem 3: The key significant error to watch for is adding instead of subtracting the overlap ($50 + 33 + 16 = 99$), or finding the wrong LCM. Using LCM = 24 instead of 12 is a significant factual error. Arithmetic errors in the floor computations (e.g., $\lfloor 200/6 \rfloor = 34$) are minor.

---

## Learning Target 11

> (**CORE**) I can compute binomial coefficients and solve simple counting problems involving combinations and permutations.

---

**Problem 1.** Compute $\binom{10}{4}$.

$$\binom{10}{4} = \frac{10!}{4! \cdot 6!} = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1} = \frac{5040}{24} = \mathbf{210}$$

---

**Problem 2.** Committee of 6 from 14 candidates (order doesn't matter).

$$\binom{14}{6} = \frac{14!}{6! \cdot 8!} = \frac{14 \times 13 \times 12 \times 11 \times 10 \times 9}{6 \times 5 \times 4 \times 3 \times 2 \times 1} = \frac{3003840}{720} = \mathbf{3003}$$

---

**Problem 3.** Rearrangements of `PICTURE` (7 distinct letters).

$$7! = \mathbf{5040}$$

---

**Problem 4.** Two-character strings from `PICTURE`.

`PICTURE` has 7 distinct letters: P, I, C, T, U, R, E. A "two-character string" implies order matters (e.g., `IC` ≠ `CI`).

This is a $k$-permutation: $P(7, 2) = 7 \times 6 = \mathbf{42}$

> **Grading notes:**
> - Problem 1: Students must show at least the setup $\frac{10!}{4! \cdot 6!}$ or expand the numerator/denominator. A bare answer of 210 with no work shown does not meet Master.
> - Problem 2: Same requirement — show the formula setup. $\binom{14}{6}$ must be explicitly computed, not just stated.
> - Problem 3: `PICTURE` has all distinct letters so $7!$ is correct. Watch for students who treat repeated letters as present (there are none here).
> - Problem 4: The phrase "two-character strings" implies ordered selection ($k$-permutation). Students who compute $\binom{7}{2} = 21$ are treating this as an unordered combination — that's a significant error. The answer $42$ requires recognizing that order matters for strings.
> - Answers must not be in scientific notation. All digits must be visible.
