---
tags: mth225, weekly-practice
---

# MTH 225: Weekly Challenge 2

**Due on Blackboard by 11:59pm Eastern on Saturday 9/18.** See "Submission Instructions" at the end of this document for details. 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* You may type up your work or write it by hand on paper, whiteboard, or in a notes app. **Typewritten work is preferred** because it makes revisions easier for you.
* If you handwrite your work on paper or a whiteboard, your work needs to be **scanned to a legible, black-and-white PDF**. 
* All your work is to be submitted as a **single PDF** at the appropriate assignment area on Blackboard in the *Weekly Challenges* folder. Please do not submit multiple PDFs, or files that are not in PDF format. 
:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

**Division algorithm:** Find the quotient and remainder when $b$ is divided by $a$, for each of the following: 

- $b = 2008, a = 7$
- $b = 6622, a = 11$

**Modulus operator:** Find the value of each of the following: 

- $92 \, \% \, 4$ 
- $2891 \, \% \, 5$ 
- $90009 \, \% \, 11$ 
- $222 \, \% \, 26$ 
- $(-92) \, \% \, 4$ 

**Truth tables:** Make a truth table for each of these propositions: 

- $(\neg A) \wedge B$
- $(A \wedge B) \rightarrow (A \vee B)$  (Why does the result make common sense?)
- $A \wedge \neg (B \vee C)$
- $(A \wedge (\neg B)) \rightarrow C$


## Application/Extension Problems 

:::info
Remember, your submission should include complete solution attempts at *all* of the problems below. Each attempt should be a good-faith attempt at a correct answer and solution. 
:::

**Cryptography** is the study of secure communications in the presence of an adversary. You can think of it as "codemaking and codebreaking" although there's more to the subject than that. If you are a Cybersecurity major, this is a large part of what you are studying; but cryptography is the business of each one of us, since we live in a digitally connected world where we are constantly sending sensitive information back and forth and we don't want it to be publicly available. 

Almost all cryptography today is based on mathematics, and in MTH 225 we are learning some of the basic tools in the cryptographic toolbox. This week's application problems will focus on some *very* early uses of cryptography going all the way back to ancient Roman times. 

We'll build in cryptographic applications into many of our remaining Weekly Challenges because it's useful, cool, and fun. 

:::warning
Before attempting these problems, please read through the [Very Short Introduction to Cryptography](/HIom2Po5RNiscLfUYC6qCw) first. 
:::

Here is a very old cryptographic system called the **Caesar cipher** or **shift cipher**. It was reportedly used by Julius Caesar's armies during the Gallic Wars to encrypt messages being sent back and forth. Here's how the encryption works (suitably updated to modern times): 

- To each of the 26 letters of the English alphabet, assign a number using the rule A = 0, B = 1, C = 2, and so on up through Y = 24, Z = 25. 
- If Alice wants to send Bob a message --- assume that it's all text with no punctuation or numbers --- she first converts each letter of the text to its number. The plaintext is now a string of numbers between 0 and 25, inclusive. 
- Alice and Bob then agree upon a key, which in this case is a randomly-generated positive integer, which we call $K$. They both use the same key. 
- Alice then goes through each number $x$ in the plaintext and computes $(x + K) \, \% \, 26$. That is, she adds the key to the number and then reduces mod 26. This results in a *new* string of numbers, also between 0 and 25 inclusive. 
- Alice then converts each of those numbers back to letters (since they're between 0 and 25, this works). The result, is the ciphertext which she sends to Bob. 

:::info 
**Example**: Alice wants to send the message `WARNING`. She generates a random key of $K = 30$. From there, she does the following: 



| Plaintext letter | Number value $x$ | $x + K$ | $(x + K) \, \% \, 26$ | Ciphertext letter |
|:----------------:|:----------------:|:-------:|:---------------------:|:-----------------:|
|        W         |       22           |  52       |       0                |    A               |
|       A           |       0           |  30       |     4                  |     E              |
|      R            |      17            |  47       |    21                   |   V                |
|      N            |        13          |  43       |    17                   |  R                 |
|       I           |        8          |   38      |     12                  |    M               |
|       N           |       13           |  43       |    17                   |   R                |
|        G         |       6           |   36      |     10                  |    K               |

So Alice sends the message `AEVRMRK` to Bob.
:::


**Problems to work:** 

1. Make up a short message (10 characters or less) and encrypt it using this system. Remember to generate a key! Show all your steps (maybe use a table like above). 
2. We've seen the *encryption* process. How would the *decryption* process go? Write out a step-by-step procedure for Bob would do to decrypt a message that was encrypted using this shift cipher. Remember you can assume that Bob has the key, which is the same key Alice used. 
3. Put your procedure to the test by decrypting, step by step, the message `AEVRMRK` that Alice sent (with a key of 30). Maybe make a table like the one shown above for encrypting. 
4. Now you've generated an algorithm for decrypting a shift cipher message and used it in one example that was hopefully successful. Now, give an explanation for why your decryption process will **always** produce the plaintext, no matter what the message or the key were. Your explanation should be clear, *not* bound to any specific examples, and use the mathematical operations involved. 
5. Now pretend to be Eve. On Campuswire, you'll find a post (link will be given here eventually) that contains several messages that were encrypted using the shift cipher, but you don't know the key. This mirrors how real-life encryption should work --- the ciphertext and the encryption method should always be considered public knowledge but the key is secret. Pick the one that corresponds to you and then try to decrypt the message. You don't know the key, so you'll have to think about this. Any information you can get from the ciphertext is considered a successful "break" of the code. Whatever you are able to get successfully, explain in detail how you got it. 

## Feedback and Reflection 

:::info
Your submission should also include complete responses to *all* of the prompts below. There is no minimum word count, but your responses should be thoughtful and should actually express your thoughts on the prompt. If you'd rather discuss these with me in person, come by drop-in hours or schedule an appointment. 
:::

1. What was one thing you learned this week that you found especially interesting or useful, and why did it stand out for you? 
2. What was one thing you did this week in terms of being a learner --- attitude, behavior, study habits, life hacks, etc. --- that was especially helpful in helping you learn? 
3. What was one thing that blocked you this week in terms of being a learner? This could be something external to you, or something in your attitudes or behaviors. How will you deal with that this next week? 
4. Finally, ask me one question --- related to the course or not related to the course --- that you'd like to see me answer. (Yes, I will answer everything you throw at me.) 