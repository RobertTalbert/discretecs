# MTH 225: Set operations activity 

---

## Part 1: Basic Set Operations (6 minutes)

Let U = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10} (the universal set)  
Let A = {1, 2, 3, 4, 5}, B = {4, 5, 6, 7}, and C = {2, 4, 6, 8}

**Compute the following:**

1. A ∪ B
2. A ∩ B
3. A ∩ C
4. B ∪ C
5. A − B (set difference: elements in A but not in B)
6. B − A
7. A' (complement of A)
8. (A ∩ B)'

---

## Part 2: Cartesian Products (4 minutes)

Let X = {a, b} and Y = {1, 2, 3}

9. Find X × Y (list all ordered pairs)

10. Find Y × X

11. What is |X × Y|?

12. If |P| = 4 and |Q| = 5, what is |P × Q|?

13. True or False: X × Y = Y × X

---

## Part 3: Combined Operations (4 minutes)

Using the same sets from Part 1: U = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}, A = {1, 2, 3, 4, 5}, B = {4, 5, 6, 7}, C = {2, 4, 6, 8}

14. (A ∪ B) ∩ C

15. A ∪ (B ∩ C)

16. (A ∩ B) ∪ (A ∩ C)

17. A − (B ∩ C)

18. (A − B) ∪ (B − A) — this is called the **symmetric difference**

---

## Part 4: Application Problems (6 minutes)

**Problem 19: Student Course Enrollment**

At a small college:
- Let M = the set of students taking Math
- Let C = the set of students taking Computer Science  
- Let P = the set of students taking Physics

There are 50 students total. 25 are taking Math, 20 are taking Computer Science, and 15 are taking Physics. 10 students are taking both Math and CS, 5 are taking both Math and Physics, 3 are taking both CS and Physics, and 2 students are taking all three courses.

a) Describe in words what the set M ∩ C represents.

b) How many students are taking Math or Computer Science (or both)?  
   *Note: This is trickier than it looks.*

c) Describe in words what the set M − C represents.

d) If U is the set of all 50 students, what does (M ∪ C ∪ P)' represent?

**Problem 20: Database Queries**

A company database has:
- E = {employees in the Engineering department}
- S = {employees with salaries over $100k}
- R = {employees who work remotely}

Express each query using set operations:

a) Employees who are in Engineering AND make over $100k

b) Employees who work remotely OR are in Engineering

c) Employees in Engineering who do NOT work remotely

d) Employees who make over $100k but are NOT in Engineering

**Problem 21: Programming Application**

In Python, if A and B are sets:
- `A | B` computes A ∪ B
- `A & B` computes A ∩ B
- `A - B` computes A − B

Write the Python set expression for: (A ∪ B) − (A ∩ B)

---

## Challenge Question

22. Prove or provide a counterexample: For any sets A and B, is it true that A − B = B − A?

---
