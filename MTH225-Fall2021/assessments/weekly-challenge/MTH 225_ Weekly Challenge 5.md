---
tags: mth225, weekly-challenge
---

# MTH 225: Weekly Challenge 5

**Due on Blackboard by 11:59pm Eastern on Saturday 10/9.** See "Submission Instructions" at the end of this document for details. 

:::warning
**Instructions**: 

* Your work on Weekly Challenges should consist of **complete solution attempts for all the Application/Extension Problems and complete and thoughtful responses to all the Feedback and Reflection prompts**. Before submitting your work, make sure you've reviewed the [Specifications for Satisfactory Work in MTH 225](/Cy6P0rGZQzuOM3NwZ3ZuMw) document to make sure your work meets the standards to the best of your knowledge. 
* **Practice Exercises are optional.** You do not need to turn any part of these in. But if you want feedback on any of them, turn those in with the rest of your work and I'll look at it. 
* See "Submission Instructions" at the end for guidelines on formatting and turning in your work. 
:::


## Practice Exercises 

**Practice Exercises are optional and for your benefit only.** You do not need to turn in work or answers unless you want feedback on your work. 

**Additive and Multiplicative Principles:** Find the number of...

* Binary strings (0's and 1's) that have 8 bits
* 8-bit binary strings that end in "10" on the right (example: 10110010)
* 8-bit binary strings that end either in "10" or "11" on the right 
* 8-bit binary strings that either start with a "01" on the left, or end in a "10" on the right (or both). 

If you submit these, make sure to give a short one-sentence explanation for each answer, so I (Talbert) can give good feedback. 

<!---
**Binomial coefficient:** Find the number of...

* 8-bit strings with exactly 2 "1" bits (Do not actually list these! Just determine how many of them there are.)
* The number of 6-element subsets of the set $\{0,1,2,3,4,5,6,7,8\}$  (Do not actually list these! Just determine how many of them there are.)
--->

## Application/Extension Problems 



In [Weekly Challenge 2](/09WyyAFLQ2Odl5RijKKGAw), you learned a simple cryptographic system, the *Caesar* or *shift* cipher. The encryption process worked by taking letters, converting them to numbers 0..25, then adding on a key value, then computing the result modulo 26, then converting back to letters. Here's a variation on the shift cipher. To encrypt a message, Alice follows all the steps of the shift cipher *except* **instead of adding the key, she multiplies by it**. All other parts of the encryption process stay the same. 

:::info 
**Example**: Alice wants to send the message `WARNING`. She generates a random key of $K = 31$. From there, she does the following. Note the addition in the fourth column is now multiplication, otherwise the process is the same as in the shift cipher: 



| Plaintext letter | Number value $x$ | $Kx$ | $(Kx) \, \% \, 26$ | Ciphertext letter |
|:----------------:|:----------------:|:-------:|:---------------------:|:-----------------:|
|        W         |       22           |  682       |       6                |    G               |
|       A           |       0           |  0       |     0                  |     A              |
|      R            |      17            |  527       |    7                   |   H                |
|      N            |        13          |  403       |    13                   |  N                 |
|       I           |        8          |   248      |     14                  |    O               |
|       N           |       13           |  403       |    13                   |   N                |
|        G         |       6           |   186      |     4                  |    E               |

So Alice sends the message `GAHNONE` to Bob.
:::

Here's some Python code that implements this cipher: 

```python=
# Helping function, converts letters A..Z to numbers 0..25
# ord(x) returns the ASCII Unicode value of a character 
# "A" has value 65 so we subtract 65 to start the alphabet at 0

def letter_to_number(L):  
    return ord(L) - 65

# Helping function, converts numbers 0..25 to letters A..Z
# chr(x) does the opposite of ord( ), converts numbers to Unicode 

def number_to_letter(a):
    return chr(a + 65)

# Main function to encrypt a message
def encrypt(message, key):
    ciphertext = ""   
    for letter in message: 
        x = letter_to_number(letter)
        cipher_letter = number_to_letter((key*x) % 26)
        ciphertext += cipher_letter    
    return ciphertext
```

Copy this code into a scratchwork Jupyter notebook and play with it. Here's some sample input and output: 

```
> print(encrypt("WARNING", 31))
> GAHNONE

> print(encrypt("HELLO WORLD", 22))
> YKIIWCQWKIO
```

Make sure to include the `print` statement just as it appears here, in order to see the output. 

Given a specific key, **encryption is a function from the set $\{A,B,C,\dots,Z\}$ to itself**. For instance, in the example above using $K=31$, $W$ maps to $G$ and $R$ maps to $H$. In fact, we can use the Python code to get an input-output table for encryption: 

```
> print(encrypt("ABCDEFGHIJKLMNOPQRSTUVWXYZ", 31))
> AFKPUZEJOTYDINSXCHMRWBGLQV
```

So with a key of 31, A maps to A, B maps to F, C maps to K, and so on. Note that **changing the key, changes the mapping**: 

```
> print(encrypt("ABCDEFGHIJKLMNOPQRSTUVWXYZ", 22))
> AWSOKGCYUQMIEAWSOKGCYUQMIE
```

So with a key of 22, the mapping of the alphabet to itself is now different --- A still maps to A, but now B maps to W, C maps to S, and so on. 

The problems in this week's challenge have to do with the properties of this encryption function. 

:::info
**Note:** In these exercises you're being asked to experiment with code to make a **conjecture** about something. A *conjecture* is an educated guess about a pattern or fact, that you believe is true based on partial information. 

For example, if I took the sequence of numbers 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ... (a.k.a. the "[Fibonacci sequence](https://www.mathsisfun.com/numbers/fibonacci-sequence.html)" we saw in a class example) and were asked *Which of these numbers is even?*, I might notice that *every third one appears to be even*. That's a conjecture. 

A more precise way to state it would be to express it mathematically, for example: If $F(0) = 1$, $F(1) = 1$, $F(2) = 2$, and so on then $F(n)$ is even as long as $n+1$ is a multiple of $3$. I could then test that conjecture. My conjecture states that F(5) should be even, and this works out --- 1, 1, 2, 3, 5, 8 so $F(5) = 8$ which is even. 

Now that the conjecture appears to be true, what needs to take place is to explain why it's always true, using an explanation that is more than just generating more examples. 
:::


1. In your scratchwork Python notebook (or by hand), encrypt the letter "A" using several different choices of keys. You should notice that no matter what the key, "A" always encrypts to itself. (This was *not* the case in the shift cipher.) That is, a reasonable *conjecture* is that **the letter "A" always encrypts to itself for any value of the key**. Explain why this will always be the case, using math and the details of the encryption process. 
2. Encrypt the letter "N" using different choices of keys. (Don't just use two or three keys; leverage Python to test dozens of them, maybe using a loop or list comprehension.) Make a conjecture about what "N" encrypts to. This should be a statement that relates the value of the key to the encrypted value of "N". State your conjecture clearly and precisely. Then, give a convincing mathematical explanation for why your conjecture is true, using math and the details of the encryption process. 
3. In the last two Python examples above showing the entire alphabet being encrypted, notice that the encryption function is injective when $K = 31$ (no two letters encrypt to the same letter), but not injective when $K = 22$ because for example "M" and "Z" both encrypt to the letter "E". Which values of the key will make the encryption function injective? Experiment using the Python code provided and make a conjecture, then give a convincing mathematical explanation for why your conjecture is true. If it's easier, you can instead make a conjecture about when the encryption function is *not* injective and explain. 
 
## Feedback and Reflection 

This week, instead of doing the usual questions, fill out this form: 

https://docs.google.com/forms/d/e/1FAIpQLSddxQl5lcWpciTM-ih2FdEWCXYdHV_h5rInHD-_w9b0tfcRIw/viewform

You filled out a similar form three weeks ago. Your answers might have changed since then, so think carefully and respond honestly based on where you are now. 

## Submitting your work

This week you are not writing any Python code, so you do not have to use a Jupyter notebook unless you want to. If you do, please use the submission workflow we used last week: **Submit the `.ipynb` notebook *and* a PDF version, on Blackboard if you are using a Jupyter notebook.**

You are highly encouraged to type up your work, since it makes it easier to correct later if needed. Please avoid handwritten work. If you must hand-write your work, it needs to be neatly done and professionally organized, or it may receive an Incomplete (IC). 