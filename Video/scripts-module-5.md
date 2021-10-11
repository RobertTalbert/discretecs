# Module 5 scripts 

## 5.1

- What is a sequence? Just an ordered list of numbers 
- Examples
  - With a pattern
  - Without really a pattern but an ordering, digits of pi
  - Often start counting at 0 but sometimes 1  (*We will start counting at 0 unless explicitly shown otherwise*)
  - Label the elements with a subscript called the index
  - Sequences are also functions from N into the set of real numbers 
- Two ways of generating sequences
  - With a closed formula
    - Examples: a_n = n^2, b_n = 3(1.1)^n -- to generate elements just plug numbers in (spreadsheet or Python function, Python list comprehension)  
  - Recursively
    - Sequence terms are defined using previously-computed sequence terms
    - Requires a recurrence relation to define how to relate terms, and an initial condition (one or more terms of the sequence -- one less than the number of terms needed by the recurrence relation)
    - Example: a_n = 2 * a_{n-1} with initial condition a_0 = 3
    - Example: b_n = b_{n-1} + 2b_{n-2} with initial conditions b_1 = 1, b_2 = 1. Notice we need TWO initial conditions 
 
## 5.2

- What we often do with sequences: Add or multiply the terms. Two math notation pieces that shorten this up. 
- Sigma notation
  - What it looks like and what the parts mean
  - Examples (from 5.1) 
  - This is a FOR loop where we're accumulating by adding. 
- Pi notation
  - Exactly the same as sigma notation but multiplying instead 
  - Examples 
  - It's a FOR loop where we multiply instead. 
- Partial sums: 
  - kth partial sum of a sequence = sigma of 0 through k-1 (first k elements)
  - Equal to sigma of 1 through k-1 of sequence where the index is shifted 

## 5.3 

- Two special kinds of sequences where the elements have a special relationship
- Arithmetic
  - The sequence is growing by the same amount each time
  - Example: 3, 5, 7, 9, 11, ... always +2
  - Example: 10, 5, 0, -5, -10, .... always -5
- Geometric
  - The sequence is growing by the same factor each time
  - Example: 3, 6, 12, 24, 48, ... always *2 
  - Example: 5, (grow by *1.1)
- Quiz: Label each as geometric, arithmetic, or neither 
- Example: Summing up powers of 2 --- conjecture? 