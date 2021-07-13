# Scripts for module 1 videos 


## 1.1 

This course is about the basic foundations of computer science, and there's nothing more foundational than numbers. In order to do anything mathematical in computer science, our first order of business is to understand how computers handle numbers. That's what this video is about. 

By "number", for now we're only going to mean non-negative integers. An "integer" is simply a whole number, something that isn't a fraction or decimal. So for the time being when we say "number" we mean 0, 1, 2, 3, and so on and we will leave negative numbers and fractions or decimals out of the picture for now. 

Let's think first about how we as human beings think about numbers. Look at the number 275. When you were a kid, you learned that this number has three digits -- the 2, the 7, and the 5 -- and those digits appear in different places. The 5 is in the ones place, the 7 is in the tens place, and the 2 is in the hundreds place. Let's think about those "places". Each "place" in a number is a power of 10: 1 is 10^0, 10 is 10^1, 100 is 10^2. 

The digits are there in those places to tell you how many copies of that power of 10 to use. So 275 uses 2 hundreds, 7 tens, and 5 ones. We could write this by pulling apart the different places and writing 

275 = 200 + 70 + 5 

which is 2 * 10^2 + 7 * 10^1 + 5 * 10^0. So we can write 275 as a sum of copies of powers of 10, and the digits we use tell us how many copies of each power of 10 to include. 

To take another example, look at 17025. This has digits not only in the ones, tens, and hundreds places but also the thousands and ten-thousands places. This can be written also as a sum of copies of powers of 10: 

17025 = 1 * 10000 + 7 * 1000 + 0 * 100 + 2 * 10 + 5 * 1 

or, 1 * 10^4 + 7 * 10^3 + 0 * 10^2 + 2 * 10^1 + 5 * 10^0. 

What those very simple examples illustrate is the fact that **every nonnegative integer can be written as a sum of copies of powers of 10** and the number of copies ranges from 0 to 9 (which are the digits of the number). 



This format for writing numbers is called the base 10 or decimal representation of the number. The word decimal doesn't mean fractions like 3.14. It uses the prefix "deci" which means 10. So the decimal representation of a number is our usual way of writing things where the digits refer to copies of powers of 10, in different places. 

Why do we use powers of 10? It's simply because we're human beings and we have ten fingers, and long ago this is how we learned to count. If we'd evolved to have 8 fingers, or 16, then things would have turned out differently. 

Humans like you and I store and process numbers in decimal form. All the arithmetic you learned when you were a kid, for example, uses base 10 representation. Computers, on the other hand, are not human and do not have 10 fingers. Our use of base 10 representation makes no sense to a computer, despite the fact that computers seem to have no trouble working with numbers. But in fact, below the surface, in order to do any math on a computer --- and the only thing a computer actually does, is math --- we have to learn how to translate from our world of numbers to theirs. 

How do we do that? 

You have to understand that computers are electronic devices, so they only understand two things: On, and off. Computers process electrical pulses that have only those two states. We usually represent those two states with either a 1 (for "on") or a 0 (for "off"). So whereas we humans have literally ten digits on our hands and therefore ten digits used for numbers, computers only have two digits. Since there are only two, we refer to this as binary rather than decimal, and the term binary digit is usually shortened to just "bit". 

Everything you see a computer do, including the playback of this video, your word processor, the video game you like to play --- it's all just an extremely long string of bits telling the hardware what to do. Any information processed by a computer is in binary, including numbers. So how is this done when you only have two digits? 

Just like we can write every number as a sum of copies of powers of 10, it turns out we can write any number as a sum of copies of powers of 2. When we do this, we create what's called the base 2 or binary representation of that number. Because we're going to be using powers of 2, here they are from 2^0 which is 1 all the way up through 2^11 which is 2048. Hard-core computer people might recognize 2^10 or 1024 because this is the number of bytes in a kilobyte. I highly recommend you learn these powers of 2 so that they are as  familiar to you as powers of 10. 

Look for example at 275 again. Although it's not necessarily easy to see, we can write this number as a sum of powers of 2 like this: 

275 = 256 + 16 + 2 + 1. 

All those are powers of 2 and there were several that we skipped. In this representation we used 

1 2^8 
0 2^7 
0 2^6 
0 2^5
1 2^4 
0 2^3 
0 2^2
1 2^1 
1 2^0

The binary representation of the number 275 is the string of digits you see in the second row: 100010011. 

Notice importantly that *unlike* decimal representation where we use the digits 0 through 9, in binary the only digits we ever use are 0 and 1. We'd never see a 2, or a 5 or a 7 show up because this would simply mean we'd use a higher power of 2. It's just like how you don't see "13" show up as one of the digits in a decimal representation. 

Here's another example of changing a decimal number to binary: 1902. That number can be written as this sum of powers of 2: 

1902 = 1024 + 512 + 256 + 64 + 32 + 8 + 4 + 2

So we have 2^10, 2^9, 2^8, then a 2^6, 2^5, 2^3, 2^2, and 2^1 and no other powers of 2. That means the binary representation is 11101101110. 

It's not totally clear right now how we can easily split up a number into a sum of powers of 2 like this other than through guess and check. But don't worry -- In a later video we're going to present a speedy algorithm for doing this which will make it easy to convert representations from base 10 to base 2.

Notice that converting the representation in the other direction, from binary to decimal, is on the other hand pretty easy. For example look at the binary integer 10101100. This is saying this number 2^2 + 2^3 + 2^5 + 2^7 and a calculator will tell you this is the decimal number 172. Just use the bits to tell you which powers of 2 to include, find those powers of 2, then sum them up. 

So in this video you've learned what our primary school concept of base 10 representation means, what a binary digit or bit is, what base 2 or binary representation means, a basic first idea of how to convert an integer from decimal to binary representation (although we're going to improve on this in a later video) and how to convert from binary to decimal. That's a big step toward being able to understand how computers and computer programs really work! Congratulations and see you in the next video. 

## 1.2

In the previous video, you learned about decimal or base 10 representation of an integer which is how humans think about numbers, and binary or base 2 representation which is how computers think about them. It turns out that binary isn't the *only* way computers represent numbers, though. There are two other number bases that are commonly used, and in this video we're going to learn about those. 

We saw in the last video that the usual base 10 or decimal representation is where you think of a number as a sum of copies of powers of 10. We use 10 because most humans have 10 fingers. But what if you encountered an alien species with 8 fingers? They would probably count the same way, but their system would involve representing a number using copies of powers of 8, and only the digits 0 through 7. That's actually not science fiction, but a common way for computers to represent integers --- using this "base 8" system, also known as *octal*. 

In base 8, we just write an integer as a sum of copies of powers of 8. Here are the powers of 8 from 0 through 10, for reference. If some of of these look familiar, remember that 8 is a power of 2, and so all of these are also powers of 2 which we saw last time. More on that in a minute. 

In the last video we practiced with converting an integer from decimal to binary and vice versa. Let's do the same thing now, with octal. Look at the integer 196. This is in decimal form --- it can't be in octal because the digit "9" does not exist in octal. We can write 192 as...

192 = 3 * 64 + 0 * 8 + 4 * 1 

Remember we're using powers of 8 here, and because of that we can use digits 0 through 7, we're not restricted to just 0 or 1. As with base 10 and base 2, writing 192 in base 8 means stripping off the digits and writing them in a string: 

192 in base 10 = 304 in base 8

Notice we say "three zero four" not "three hundred and four" because the "3" here is *not* hundreds. 

Likewise, let's say we have 1402 that's represented in base 8. What is this number in base 10? Just like with binary, converting from octal to decimal is easy --- just count up the powers of 8. 

1402 = 1 * 8^3 + 4 * 8*2 + 0 * 8^1 + 2 * 8^0 = 770. 

Converting from binary to octal is easy too, in fact octal is often used to shorten binary strings. Given the binary string, group the bits into threes and convert each group of three to a number between 0 and 7, and that's your octal representation. For example, take the binary integer 10110001.

Group into threes: (010)(110)(001) Adding the zero on the left to pad it, so it's a group of 3. 

Then convert each group to decimal which is easy because the numbers are small: 010 is 2, 110 is 6, 001 is 1. The resulting octal integer is 251. (As a decimal, that's 177.)

Continuing this trend of using number bases that are powers of 2, another common base used in computer science is base 16, known as hexadecimal. If you've been around computers you have probably seen hexadecimal numbers. They're sometimes used for example to represent colors in web design --- for example this website lets you dial up a color using hexdecimal code. They are also used in URL shortening services. 

Hexadecimal or base 16 is the same idea as base 2, 8, or 10 --- except instead of writing an integer as a sum of copies of powers of 2, 8, or 10, we write it as a sum of copies of powers of 16. This introduces something curious. In base 2, we used digits either 0 or 1 to represent the place values. And in octal we used 0 through 7. In base 16, we'd use 0 through 15. But this would get confusing to use two decimal digits to represent a single place value, so we use the ordinary 0 through 9 to represent 0 through 9, and for 10, 11, 12, 13, 14, and 15 we use the letters a, b, c, d, e, and f. 

For example, the hexadecimal number "1A8" is 

1A8 = 1 * 16^2 + (10) * 16^1 + 8 * 16^0 which is 424 in base 10. 

Converting the other way, look at the decimal number 250. Written as a sum of powers of 16, this is

250 = 15 * 16^1 + 10 * 16^0. The "digit" 15 is represented be the letter F and 10 by A. So 250 in base 10 is "FA" in base 16. 

Hexadecimal is widely used because it crunches the size of an integer down into a smaller string of digits. Notice the three-digit decimal integer 250 is only two digits long in base 16. In binary the result is more dramatic. To convert from binary to hexadecimal, similarly to how we converted binary to base 8, group the bits into fours and convert each group into 0-9 or A-F. For example

10110001 would be grouped as (1011)(0001) which would convert to (11)(1) or B1. Hexadecimal in other words represents a binary integer in one-fourth of its original length, which saves on storage. 

Finally here's a dad joke for you. Why did the computer programmer always get Christmas and Halloween mixed up? 

It's because Oct 31 = Dec 25. 

[sigh]

OK, so in this video we learned about octal or base 8 representation, hexadecimal or base 16 representation, and how to convert back and forth between base 2, 8, 10, and 16. Next up we're going to address a missing piece, which is an algorithm to quickly convert from decimal to any of these other bases. See you there. 