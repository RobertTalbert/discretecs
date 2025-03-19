# Application/Analysis Homework 8

## Instructions

Please **work all problems on your own paper, note-taking app, on a whiteboard, or typed**. Whatever format you use, submit a **single, black-and-white PDF of your work** by creating this PDF and uploading it to the folder on Blackboard labeled **Application/Analysis Homework 8**. If you handwrite your work on paper or a whiteboard, **scan** it to a black-and-white PDF and upload the PDF. **Do not just take a picture with your phone -- scan it, using a scanning app** so that the result is a PDF, not an image. You practiced this process in the Startup Activity, and there is a tutorial in the START HERE area about how to do it. 

Application/Analysis Homework sets are graded on the basis of **completion and effort only** and you will earn 4 engagement credits for earning a *Success* mark. The standards for earning that mark are given in the [Standards for Student Work](https://github.com/RobertTalbert/discretecs/blob/master/MTH225-Winter2025/course-docs/Standards%20for%20Student%20Work%20MTH%20225%20W25.md) document. Make sure to review those standards before you turn in your work. 

---

## OPTIONAL: Practice exercises 

The following practice exercises are OPTIONAL. If you turn these in, I will look over your work and give you feedback as needed. But they are not graded. 

1. Compute the following binomial coefficients using the closed formula we constructed in class: 
   - (a) $\binom{8}{3}$
   - (b) $\binom{10}{5}$
   - (c) $\binom{12}{6}$
   - (d) $\binom{15}{7}$
   - (e) $\binom{20}{10}$
2, Find the number of subsets of the set $\lbrace a,b,c,d,e,f,g,h,i,j, k, l \rbrace$ that have exactly 5 elements.
3. Find the number of ways to select a committee of 5 people from a group of 10 people, where the order of selection does not matter.
4. Find the number of ways to select a committee of 5 people from a group of 10 people, where the order of selection does matter.

 
## Multiple choice

The following multiple choice items are REQUIRED, that is NOT OPTIONAL. For each, give the letter for the response you believe is most correct. Explanations are not required; but if you give one and there's an issue with your reasoning, I'll give you feedback. 

1. For any natural number $n$, the value of $\binom{n}{0}$ is 
   - (a) 0
   - (b) 1
   - (c) $n$
   - (d) $n+1$
   - (e) None of these

2. The number of ways to select a committee of 5 people from a group of 10 people, where the order of selection does not matter, is 
   - (a) $\binom{10}{5}$
   - (b) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6$
   - (c) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5$
   - (d) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4$
   - (e) None of these

3. The number of ways to select a committee of 5 people from a group of 10 people, where the order of selection does matter, is 
   - (a) $\binom{10}{5}$
   - (b) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6$
   - (c) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5$
   - (d) $10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4$
   - (e) None of these

4. The binomial coefficient is used in counting problems that involve 
    - (a) Selections of items from a set where the order of selection matters
    - (b) Selections of items from a set where the order of selection does not matter
    - (c) Arrangements of items in a sequence
    - (d) All of the above
    - (e) Just (a) and (b)

5. The number $11 \times 10 \times 9$ is the same as 
    - (a) $\binom{11}{3}$
    - (b) $\binom{11}{2}$
    - (c) $\binom{11}{1}$
    - (d) $\binom{11}{0}$
    - (e) None of these


## Problems to solve 


1. One application of the binomial coefficient is to a particular kind of problem where we are counting **the number of ways to distribute $n$ identical items into $k$ distinct boxes**. For example, suppose we have 10 identical apples and 5 distinct boxes. How many ways are there to distribute the apples into the boxes? This problem will have you think through some *incorrect* ways to answer this question and then arrive at the correct method. 
    - (a) Here is one incorrect approach: The answer is $\binom{10}{5} = 252$ because we are selecting 5 apples from 10. Explain why this is incorrect.
    - (b) Here is another incorrect approach: The answer is $10^5 = 100000$ because it's a license plate problem: Make 10 blanks, one for each apple, and in each blank write the numbers 1, 2, 3, 4, or 5 to indicate which box to put that apple into. There are 10 apples and 5 choices per apple, so $10^5$ in all. Explain why this is incorrect.
    - (c) [Now go here and watch a video](https://vimeo.com/626749580) about an approach called the :"stars and bars" method, also known as the "dots and dividers" method. Apply this method to solve the problem of distributing 10 identical apples into 5 distinct boxes. Write out the solution in detail.
    - (d) Explain why the "dots and dividers" method is the correct way to solve this problem.


2. In Application/Analysis Homework 7 you looked at a proposed proof of an identity involving binomial coefficients. Here is another identity involving binomial coefficients: For all natural numbers $n$ and $k$ with $n \geq k$, $\binom{n}{k} = \binom{n}{n-k}$. 
    - (a) Prove that this identity is true, using the closed formula we built in class. Apply that formula to the left, and apply it to the right, and then explain why the two resulting expressions are equal. Note: This does not invole mathematical induction. 
    - (b) Prove that this identity is true, *without* using the closed formula or induction, but instead by using an argument based on counting and an interpretation of the meaning of $\binom{n}{k}$. Explain your reasoning in detail; there should not be any calculations involved, just clear English explanations. 

*Note on problem 2*: **"Proofs" like these must not use examples.** They should be general arguments that work for all natural numbers $n$ and $k$ with $n \geq k$. You can use examples in your notes to help you understand why the argument works, but the proof itself should be general with no references to any specific choices of $n$ or $k$. 