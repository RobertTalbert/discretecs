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

We saw in the last video that the usual base 10 or decimal representation is where you think of a number as a sum of copies of powers of 10. We use 10 because most humans have 10 fingers. But what if you encountered an alien species with 8 fingers? They would probably count the same way, but their system would involve representing a number using copies of powers of 8, and only the digits 0 through 7. That's actually not science fiction, but a common way for computers to represent integers.

Just as it's possible to write any number as a sum of copies of powers of 2 or 10, we can write any number (remember this means nonnegative integer for now) as a sum of copies of powers of 8. When we do this, we are using the base 8 or octal representation of that number. 

Here are the powers of 8 from 0 through 11, for reference. If some of of these look familiar, remember that 8 is a power of 2, and so all of these are also powers of 2 which we saw last time. 

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

Finally here's a dad joke for you. Why did the computer scientist always get Christmas and Halloween mixed up? 

It's because Oct 31 = Dec 25. 

[sigh]

OK, so in this video we learned about octal or base 8 representation, hexadecimal or base 16 representation, and how to convert back and forth between base 2, 8, 10, and 16. Next up we're going to address a missing piece, which is an algorithm to quickly convert from decimal to any of these other bases. See you there. 

## 1.3

So far we've learned about representing integers in different number bases, specifically base 10 which is what we learn as kids, and bases 2, 8, and 16 which are commonly used in computer science. These different number bases are a lot like different units of measurement, like how milliliters, gallons, and cups are both measures of volume, but each one is more useful in some contexts than others. One thing we need to learn to do is convert between these different ways of representing numbers. We've seen how to convert a representation from base 2, 8, or 16 to base 10 (which is pretty simple) and from base 2 to either base 8 or 16 (which is also pretty simple). Going from base 10 to any other base, on the other hand, isn't hard but it sort of felt like guesswork earlier. In this video we're going to learn an algorithm for making conversion from base 10 systematic and fast. 

First of all, what does that word "algorithm" mean? The basic definition is a finite process or a set of rules that we or a computer will follow to make a computation or solve a problem. For example, in school we learned algorithms for multiplying two numbers together. In computer science we have algorithms for efficient sorting of lists, finding the shortest path through a network, and more. Algorithms are at the core of computer science and you will be visiting them regularly throughout this course and throughout your careers. 

We're going to describe an algorithm that will convert a number from base 10 to base 2, and to set this up, let's consider the following process on a specific number. Take the number 2417 in base 10. 

Divide this number by 10 and record the quotient (how many times 10 goes into it) and the remainder (the amount left over). If you do the long division on this (another algorithm we learned in school), 10 goes into 2419 241 times with a remainder of 7. So the quotient is 241 and the remainder is 7. Note that the remainder must be less than 10, because if the remainder is 10 or bigger we could just divide again. Record both the quotient and the remainder. Now repeat this process using the quotient 241 as the new input. Divide 241 by 10: The quotient is 24 and the remainder is 1. Record both. Now repeat the process again using the previous step's quotient as the new input: Divide 24 by 10 and you have a new quotient of 2 and a remainder of 4. Repeat again: Divide 2 by 10 and this yields a quotient of 0 and a remainder of 2. If we were to repeat this process more, we would be getting a quotient and a remainder of 0, so once we get a quotient of 0 the algorithm terminates. 

Now if you look at the list of remainders we kept, these are the base 10 digits of the original number 2417 in reverse order. Repeated division by 10 in other words produces a list of the digits. 

The algorithm for converting base 10 to base 2 is exactly the same algorithm we just described except we are going to divide by 2 each time rather than 10. When we divide an integer by 2, we always get a remainder of either 0 (if the number is even) or 1 (if it's odd) and never anything else. So those remainders are going to be bits. 

Let's start with a simple two-digit decimal integer, 37. This is the original input. The way the conversion algorithm works is that we will repeatedly divide the input by 2, record the quotient and remainder, and then repeat that process using the previous step's quotient as the new input, and then stop when the quotient is 0. 

So first, 37 / 2 is 18 with a remainder of 1. Record 18 and 1 in memory. 
Next: 18 / 2 is 9 with remainder 0. Record those two in memory. 
Next: 9 / 2 is 4 with remainder 1. 
Next: 4 / 2 is 2 with remainder 0. 
Next: 2  / 2 is 1 with remainder 0. 
Next: 1 / 2 gives a quotient of 0 with a remainder of 1, so record those in memory but then stop since the quotient is 0.  

To end the algorithm and get the binary representation, construct a string from the remainders in the reverse order in which they appeared: 100101. 

Let's check to make sure this is right. 100101 is 1 2^5, 1 2^2, and 1 2^0 which is 32 + 4 + 1 and that is indeed 37 in base 10. 

Now you try it. In the very first video, we converted the base 10 integer 275 to binary without this algorithm and the answer was 100010011. Pause the video, and take a few minutes to work through the algorithm to convert the bases with the algorithm. 

Here's the work for this process, and you can see that it does indeed produce the right binary. 

For the moment, we are going to take it on faith that this algorithm really works for every input we could throw at it. But as computer scientists, we don't want to just take algorithms on faith --- we want to be convinced that algorithms always work for any input within the scope of the program. A million examples of successful processing will not be enough for this --- we will need to reason through algorithms and explain why, in ALL cases and not just the ones we choose or observe, the algorithm works. Reasoning through algorithms independently of random testing is a major learning goal for this course and we will do so for this algorithm a little later in the course. 

But do notice that this algorithm, while tedious to do by hand, is quite fast because every iteration of the loop where we divide and record the quotient and remainder cuts the input size literally in half. So although it obviously takes more steps to convert a large decimal integer than it does a small one, a number with twice as many decimal digits does not necessarily take twice as many steps. Another important concept we will be thinking about in this course is just how exactly algorithms scale up when the input size increases and how that scaling up might be modeled with mathematical functions. 

Another great thing about this algorithm is that it can be modified to convert a decimal integer into ANY base, not just binary, simply by changing the number we divide by. For example if we wanted to convert the number 1982 from decimal to octal, just run the same process but divide by 8. In this case, 

1982 / 8 = 247 with remainder 6
247 / 8 = 30 with remainder 7
30 / 8 = 3 with remainder 6 
3 / 8 = 0 with remainder 3, stop here and list back the remainders in reverse order to get 3676 which is 1982 in octal. 

Here's an example in hexadecimal that shows how fast this can be --- look at 161067 in base 10. 
161067 / 16 = 10066 with remainder 11
10066 / 16 = 629 with remainder 2
629 / 16 = 39 with remainder 5
39 // 16 = 2 with remainder 7 
2 // 16 = 0 with remainder 2

So the base 16 representation of 161067 is 2752B (remember B is the hexadecimal for the number 11).

In this video, you learned an algorithm for converting from base 10 to any other base you want. And we've introduced some important concepts about algorithms -- what they are, the importance of reasoning through them, and the concept of understanding mathematically how they scale up. In the next few videos we're going to focus on binary representation specifically and think about how computers do basic arithmetic with base 2. 


# 1.4

As we've learned, binary or base 2 representation is how computers store and process numerical information. In fact it's how computers store and process ANY kind of information, since computers don't know how to do anything else besides math. Everything you do on a computer is the result of some mathematical processes performed on numbers written in binary. 

In the next few videos we're going to learn how this works on the most basic level --- specifically by learning how to do arithmetic, which means basic addition, subtraction, multiplication, and division using numbers that are written in binary. This video focuses on addition, and then there will be videos for the other three basic arithmetic operations. 

To understand how to add two binary numbers together, let's first do some VERY basic review about how we learned to add two decimal numbers together back when we were kids. Look at the sum 147 + 782. 

The algorithm we learned way back in the day goes like this. First write the numbers vertically like so. THen start adding in the ones position. Here, 7 + 2 is 9 so that goes in the ones place for the answer. Then move on to the tens place. This time, the sum of the digits, 4 + 8, is 12. It would be nonsensical to write a "12" in the answer for the tens place because 12 is bigger than 10. It overflows the space. So what we do is write down the 2 (which is in the ones place of this digit sum) and "carry the 1" over to the hundreds place, where we now have three things to add: the 1 and the 7, and the additional 1 from the carry. That adds up to 9, and this doesn't overflow the space so we write it down. Therefore the answer is 929. 

Adding numbers in binary uses the same principle and in some ways it's easier, because you now only have two possible digits to work with --- 0 and 1 --- rather than ten. In base 10, all addition is really carried out only on the simple digits 0 through 9. We split up and "carry" digits that are outside that range. So let's review how to add single digits together in binary. 

Well, 0 in binary still means 0, so 0 + 0 = 0. And 1 still means 1, so 1 + 0 = 1 and also 0 + 1 = 1. But when we add 1 and 1, it gets a little tricky. The answer is 2, but we have to keep everything in binary at all times, so: 1 + 1 = 10 which is 2 in binary. That means when we at 1 and 1, it's going to be like adding 4 and 8 in decimal -- it generates a number that overflows a single digit, and we'll need to carry a 1. 

Now we're ready to think about how computers add larger numbers in binary. Let's look at 110 + 11. In decimal, this is 6 + 3 so the answer should be 9. But we want to do this entirely in binary without changing the representation to decimal, because computers wouldn't make that change. 

Just like in base 10, line these up vertically like so. 

  110
+ 011

I added a 0 on the left side of the second number just for padding, to show you how the two numbers line up. It's not totally necessary. 

Now just like in base 10, add one place at a time starting with the ones place. Here, 0 + 1 is just 1, so that goes in the ones place for the answer. Moving to the next place (which is the "2" place, not the "tens" place) we encounter 1 + 1. As we saw above, the answer is not "2" but 10. This overflows the space, so we will write down 0 and carry the 1. Again this is exactly the same thing as adding 8 + 4 in decimal, writing down the 2 and carrying the 1. 

Now in the next place (the 4's place) we have 1 + 1 + 0. That's 10. There's no other places to carry to, so we can just write down 10. So in the end we have as the result 1001, and in decimal that is indeed 9 like it's supposed to be. 

Let's look at another example: 11101 + 11001.  In decimal this is 29 + 25 so the answer is supposed to be 54. I encourage you to pause the video and try working this out for yourself before watching the solution, and remember it is totally fine to make mistakes! You won't really learn anything otherwise, and nobody is watching. 

So we begin by lining these up vertically and adding place by place starting with the ones place. This is 1 + 1 which is 10. Write 0 and carry the 1. In the 2's place, we have 1 + 0 + 0 which is just a 1, so write that. there's no carry here, so just move to the 4's place. This is 1 + 0 which is just a 1, so write that with no carry. then in the 8's place, we have 1+1 again, so write 0 and carry the 1. Now in the 16's place, we have 1 + 1 + 1. This is technically 3, but in binary that's 11. We're at the far left end of the number so we can't really carry anything, so we end with just 11. We arrive at the answer 110110, and if you check it, this is indeed 54 in base 10. 

So congratulations, you've now learned the basics behind doing addition in binary without translating to decimal first! Now we have to tackle subtraction, which will happen in the next video. 

# 1.5

In the last video we learned how to do addition in binary. Next up is subtraction. Since it was helpful to first think carefully about how addition worked in base 10 arithmetic, let's begin with a look at how subtraction works in base 10. 

Here's an example: 326 - 152. The way we learned it when we were kids is first, just as with addition, write these on top of each other with the larger number at the top. Then go place by place and subtract only the numbers in each place. In this example the first step is 6 - 2 which is 4, and that goes in the ones place for the answer. But when we move on to the tens place, we have to think about what to do. We have 2 - 5, but this is a negative number, and it doesn't make sense to put -3 in the tens place. So what we do is sort of the opposite of "carrying" in addition --- we "borrow". We borrow a 1 from the next place up and make that 2 into a 12. Now the subtraction makes sense: 12 - 5 is 7, so we put that down in the tens place. The final place used to be 3 - 1 but now it's 2 - 1 since we borrowed so the final answer is 174. 

What exactly is going on with "borrowing"? A lot of kids learning arithmetic struggle with that concept and it's no wonder. It feels like an arbitrary rule but there's actually a basis to it. In addition we sometimes have to "carry", when for example we added 4 + 8 in the tens place. What's really happening here is that we add two single digits and get something too big for a single digit, so we split it up --- the 12 becomes 10 + 2 and we add 1 to the next place value up. Borrowing is just this in reverse --- if the subtraction on a single digit results in something too small, we grab one copy of the next place value up and combine it with the current place. 

This is important because subtraction in binary also involves borrowing, but again we only have two digits to work with, 0 and 1. Let's see how this works with the example 1101 - 110. In decimal this would be 13 minus 6, so the answer should be 7. 

Lining these up with the big one on top, in the ones place we have 1 - 0. this is just 1, so put that down with no extra steps needed. In the 2's place we have something to think about. 0 - 1 doesn't compute. It's analogous to having 2 - 5 in the earlier base 10 example. So here we borrow from the next place up. But it's a little tricky. Borrowing reduces the 1 that's in the 8's place to a 0.   That "1" represents a copy of 2^3 or 8. But we're borrowing it into the 4's place, so that's two copies of 4, not one copy. So when we put it in the 4's place, it's not a 1 --- it's a 10. 

To understand this, go back to the decimal example. When we had 2 - 5 and borrowed a 1 from the hundreds place, the 1 represents a copy of 100, not 10. So that 1 wasn't a 1, it's a 10. That's why the 2 becomes a 12 and not a 3. 

So back to binary, we have 10 minus 1, which is really 2 - 1 so the answer is just 1. 

Moving to the 4's place, we have 0 - 1 which is the same situation as previously. So borrow a 1 from the 8s place, turn that 0 into a 10, and subtract to get 1. There's nothing left, so the answer is 111. In decimal, that's "7" which is what we were supposed to get. 

Let's do a more complex example with two eight-bit integers: 11010101 - 10010111. Again, I encourage you to pause the video and work this out before seeing the solution and try to explain to yourself what you're doing. 

In decimal this is 213 minus 151 so the answer should be 62. su