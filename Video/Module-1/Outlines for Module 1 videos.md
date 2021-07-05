# Outlines for Module 1 videos 

## 1.1: Representing a number in base 10 and base 2

- First order of business in doing math for computing: Think about numbers the way computers think about them
- "Numbers" for now just means nonnegative integers -- whole numbers 0, 1, 2, 3, .... 
- How do humans think about numbers? 
  - Take 275. 
    - When you were a kid: the hundreds, tens, and ones place 
    - Each "place" is a power of 10: 100 is 10^2, 10 is 10^1, 1 is 10^0 
    - Each power of ten has a digit 0-9 associated to it to tell how many of those powers to use. 
    - So 275 is 2 hundreds, 7 tens, and 5 ones. 
    - We'd write it as 200 + 70 + 5 or 2 * 10^2 + 7 * 10^1 + 5 * 10^0. 
    - I.e. every nonnegative integer is a sum of powers of 10. Why 10? Because we have ten fingers and that's how we count. 
  - This is called "base 10" or "decimal" representation. Decimal doesn't mean fraction
- How do computers think about numbers? 
  - Computers aren't human, don't have fingers
  - As electronic devices, they "understand" only two things: On and Off. Represented by 1 and 0. 
  - Every piece of information in a computer is a string of 1's and 0's -- because it's two states, we call those strings "binary". Each 0 or 1 = "binary digit" or "bit". 
  - Numbers have to be represented this way as well. We have 10 things to count with, computers only have 2. So we use "base 2" representation. 
- What is base 2 representation? 
  - Exactly the same thing as base 10, only use powers of 2 instead of powers of 10. 
  - Powers of 2: 2^0 = 1, 2^1 = 2 , etc. 
  - Can we write 275 as a sum of powers of 2? 
    - 275 is 256 + 16 + 2 + 1 
    - Table of powers of 2 
    - 100010011 
    - Notice: Since we use powers of 2, each digit is either 0 or 1. 
  - Example: Converting 10101100 from binary to decimal 
    - Table
    - Answer is 172
  - Converting from decimal to binary --- algorithm to be discussed later that makes this quick 
  - Review 
    - Decimal (base 10) representation
    - Binary (base 2) representation
    - How to convert from binary to decimal 

## 1.2 Representation in base 8 and base 16 

- Last video: How to represent a decimal (base 10) integer in base 2 (binary) 
- Computers use other bases as well 
- Base 8 (octal)
  - Exactly the same idea as base 2, just use powers of 8 instead -- can use digits 0-7 
  - Cannot use 8 or higher -- doing so would be like using "14" as one of the digital in a decimal number
  - 8^0 = 1, 8^2 = 64, 8^3 = 256, ... 
  - Used to compress information in binary since 8 is itself a power of 2 
  - Example: What is 172 in octal? 
    - 2 64's + 5 8's + 4 1's 
  - Example: If 1402 is in octal, what's the decimal? (one-4-oh-2 not "fourteen hundred and two") 
    - 1 * 8^3 + 4 * 8^2 + 0 * 8^1 + 2 * 8^0 = 770
- Base 16 (hexadecimal) 
  - Use powers of 16 instead of powers of 10 
  - Often see hexadecimal code for things like colors or url shorteners -- compresses a lot of information into a small string 
  - Since the base is 16, we can use 16 "digits": 0-9 and then A, B, C, D, E, F. A = 10, B = 11, C = 12, D = 13, E = 14, F = 15. 
  - Example: The hexadecimal number 1A8 is 1 * 16^2 + 10 * 16 + 8 * 1 = 424. 
  - Example: The decimal number 250 is 15 * 16 + 11 * 1. So "FA". 
  - https://www.w3schools.com/colors/colors_hexadecimal.asp  Using Laker Blue 264391
- Converting decimal to either of these -- algorithm coming up 
- Dad Joke
  - Why did the computer scientist get Halloween and Christmas confused? 
  - Because Oct 31 = Dec 25 
- Review: 
  - Octal (base 8)
  - Hexadecimal (base 16)
  - Converting from octal or hexadecimal to decimal 

## 1.3 Algorithm for decimal conversion 

## 1.4 Addition in binary 

## 1.5 Subtraction in binary

## 1.6 Multiplication in binary 

## 1.7 Division in binary 

## 1.8 Two's Complement 

## 1.9 The dividion algorithm 

## 1.10 The modulus operator 


