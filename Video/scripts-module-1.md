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

In the last video we practiced with converting an integer from decimal to binary and vice versa. Let's do the same thing now, with octal. Look at the integer 196. This is in decimal form --- it can't be in octal because the digit "9" does not exist in octal. We can write 196 as...

196 = 3 * 64 + 0 * 8 + 4 * 1 

Remember we're using powers of 8 here, and because of that we can use digits 0 through 7, we're not restricted to just 0 or 1. As with base 10 and base 2, writing 196 in base 8 means stripping off the digits and writing them in a string: 

196 in base 10 = 304 in base 8

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

So far we've learned about representing integers in different number bases, specifically base 10 which is what we learn as kids, and bases 2, 8, and 16 which are commonly used in computer science. These different number bases are a lot like different units of measurement. Milliliters, gallons, and cups are all measures of volume, but each one is more useful in some contexts than others, and we often have to convert from one measure of volume to another. Similarly, it's important to be able to convert between different number base representations. We've seen how to convert a representation from base 2, 8, or 16 to base 10 (which is pretty simple) and from base 2 to either base 8 or 16 (which is also pretty simple). Going from base 10 to any other base, on the other hand, isn't hard but when we did it, it might have felt to you like guesswork. In this video we're going to make the process of converting from decimal to other bases more foolproof through a simple and rigorous algorithm. 

First of all, an "algorithm" is a finite process or a set of rules that we or a computer will follow to make a computation or solve a problem. An algorithm, if correct, will have a definite start point, and it will end after a finite number of steps with a correct result. 

For example, in school we learned algorithms for multiplying two numbers together. In computer science we have algorithms for all kinds of things like sorting of lists, finding the shortest path through a network, and more. Algorithms are at the core of computer science and you will be visiting them regularly throughout this course and throughout your careers. 

We're going to describe an algorithm now that will convert a number from base 10 to base 2, and to set the stage, let's consider the following process that isn't really useful by itself but illustrates the main idea. 

Take the number 2417 in base 10. Starting with this input, let's go through some steps. 

First, divide 2417 by 10 and record the quotient (how many times 10 goes into it) and the remainder (the amount left over). If you do the long division on this (another algorithm we learned in school), 10 goes into 2417 241 times with a remainder of 7. So the quotient is 241 and the remainder is 7. Note that the remainder must be less than 10, because we're dividing by 10, and if the remainder were 10 or greater we could just divide again. Record both the quotient and the remainder. 

Now repeat this process but use the quotient from the previous step, 241, as the new input. Divide 241 by 10: The quotient is 24 and the remainder is 1. Record both. Now repeat the process again using the previous step's quotient as the new input: Divide 24 by 10 and you have a new quotient of 2 and a remainder of 4. Repeat again: Divide 2 by 10 and this yields a quotient of 0 and a remainder of 2. If we were to repeat this process more, we would be getting a quotient and a remainder of 0, so once we get a quotient of 0 the algorithm terminates. 

Now if you look at the list of remainders we kept, these are the base 10 digits of the original number 2417 in reverse order. Repeated division by 10 in other words produces a list of the digits. 

I want you to notice two things at this point. First, algorithms in computer science and in real life often work by repetition --- you have just few lines, or even one line of code that performs a simple operation and the algorithm simply repeats, or iterates, over these instructions until some kind of condition is met and then it stops. Remember that concept as we explore algorithms in the future. Second, let's be honest, this algorithm on its own is totally useless because we don't need to go through all these steps to see the digits of a decimal number, we just look at it. The power of the algorithm really comes from the fact that we can modify it to do other things. 

In fact, this very algorithm can be modified just slightly to give us the BINARY digits of this same number. All we have to do is change the instruction of dividing by 10, to dividing by 2. When we divide an integer by 2, we always get a remainder of either 0 (if the number is even) or 1 (if it's odd) and never anything else. So those remainders are going to be bits and those bits are the digits of the binary form of the integer we start with. 

Let's see how this works with a simple two-digit decimal integer, 37. Again, the way the conversion algorithm works is that we will repeatedly divide the input by 2, record the quotient and remainder, and then repeat that process using the previous step's quotient as the new input, and then stop when the quotient is 0. 

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

And that's an algorithm for converting a number from decimal to binary. But --- you wouldn't be wrong to have a LOT of questions about this algorithm. For example, WHY does this algorithm produce the correct binary form of the integer? Are we sure that it always does produce the correct binary, or did we just get lucky with these two examples? Are we sure that the algorithm always terminates, or is it possible that we could start with an integer that throws the algorithm into an infinite loop? 

These are questions that, as computer scientists, we have to ask and answer about every algorithm we meet. It's not enough just to be able to write code and compute answers --- kids, or AIs, can do that. What we have to be able to do is reason about algorithms like this and explain why they work, in ALL cases and not just the ones we choose or observe. A million examples will not do this for us. We need to use mathematics, and mathematical reasoning, to get into the deep machinery of computing processes to help us understand things that simply writing code cannot explain. Being able to use mathematics to go beyond code, and reason about computational processes, is a major high-level learning goal for this course and we will be revisiting it repeatedly throughout everything we do. 

For now, we are going to take it on faith that this base conversion algorithm really works. But we will need to come back to this algorithm later, once we have more tools for thinking about algorithms, and think about why it works. 

Notice that this algorithm, while a little tedious to do by hand, is quite fast because every iteration of the loop where we divide and record the quotient and remainder literally cuts the new input size in half. This means that it will scale up well --- while it obviously takes more steps to convert a large integer than it does a small one, a number with twice as many decimal digits does not necessarily take twice as many steps. Another important concept we will be thinking about in this course is just how exactly algorithms scale up when the input size increases and how that scaling up might be modeled with mathematical functions. 

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

So the base 16 representation of 161067 is 2752B (remember B is the hexadecimal for the number 11). Again we have not attempted to explain WHY this works other than by analogy when we divide by 10. To prove that the algorithm works for any base will require some mathematical tools we will be encountering in later videos. 

In this video, you learned an algorithm for converting from base 10 to any other base you want. And we've introduced some important concepts about algorithms -- what they are, the importance of reasoning through them, and the concept of understanding mathematically how they scale up. In the next few videos we're going to focus on binary representation specifically and think about how computers do basic arithmetic with base 2. 


# 1.4

As we've learned, binary or base 2 representation is how computers store and process numerical information. In fact it's how computers store and process ANY kind of information, since computers don't know how to do anything else besides math. Everything you do on a computer is the result of some mathematical processes performed on numbers written in binary. 

In the next few videos we're going to learn how this works on the most basic level --- specifically by learning how to do arithmetic - basic addition, subtraction, multiplication, and division - using numbers represented in binary. This video focuses on addition, and then there will be videos for the other three basic arithmetic operations. 

To understand how to add two binary numbers together, let's first do some VERY basic review about how we learned to add two decimal numbers together back when we were kids. Look at the sum 147 + 782. 

The algorithm we learned back in the day goes like this. First write the numbers vertically like so. THen start adding in the ones place. Here, 7 + 2 is 9 so that goes in the ones place for the answer. Then move on to the tens place. This time, the sum of the digits, 4 + 8, is 12. It doesn't make sense to write a "12" in the answer for the tens place because 12 is bigger than 10. It overflows the space. So what we do is write down the 2 (which is in the ones place of this digit sum) and "carry the 1" over to the hundreds place, where we now have three things to add: the 1 and the 7, and the additional 1 from the carry. That adds up to 9, and this doesn't overflow the space so we write it down. Therefore the answer is 929. 

So in base 10, all addition is really carried out only on single digit numbers, 0 through 9, one place at a time. If we do a digit sum and it gives a result bigger than 9, then we split off the ones digits from the tens digit and carry that tens digit up to the next place, and continue until there is no more carrying and no more digits. 

Adding numbers in binary uses the same principle and in some ways it's easier, because you now only have two possible digits to work with --- 0 and 1 --- rather than ten of them. Since, as we just pointed out, addition of larger numbers is really just repeated addition of single-digit numbers together with this "Carrying" process, let's think about what happens when we add two single bits together. 

Well, 0 in binary still means 0, so 0 + 0 = 0. And 1 still means 1, so 1 + 0 = 1 and also 0 + 1 = 1 because addition is commutative, meaning the order of addition doesn't affect the answer. But when we add 1 and 1, it gets a little tricky. The answer of course is 2, but remember we are in binary now, so: 1 + 1 = 10 which is 2 in binary. That means when we add 1 and 1, we end up with a two digit number that overflows the space. It's analogous to when we added 8 and 4 in the starting example. We got 12, so we wrote down 2 and carried the 1. Similarly, any time we add 1 + 1 in binary, we will have to carry a 1. 

Now we're ready to think about how computers add larger numbers in binary. Let's look at 110 + 11. In decimal, this is 6 + 3 so the answer should be 9. But we want to do this entirely in binary without changing the representation to decimal, because computers wouldn't make that change. 

Just like in base 10, line these up vertically like so. I added a 0 on the left side of the second number just for padding, to show you how the two numbers line up. It's not really necessary. 

Now just like in base 10, add one place at a time starting with the ones place. Here, 0 + 1 is just 1, so that goes in the ones place for the answer. Moving to the next place (which is the "2" place, not the "tens" place) we encounter 1 + 1. As we saw above, the answer is not "2" but 10. This overflows the space, so we will write down 0 and carry the 1. 

Now in the next place we have 1 + 1 + 0. Just like in decimal, we can only really add two things at a time, and the grouping doesn't matter because addition is not only commutative but also associative. So add 1+1 to get 10, then add 0 to just get 10 again. Just as in the last step, this overflows the one-digit sized space allowed for the answer, so just put down the ones place and carry the 1 over. In that next place over, there's nothing --- you can think of it as two zeroes if you want, so we'd be adding 1 + 0 + 0 which is just 1, and that goes here. 

So in the end we have as the result 1001, and in decimal that is indeed 9 like it's supposed to be. 

Let's look at another example: 11101 + 11001.  In decimal this is 29 + 25 so the answer is supposed to be 54. I encourage you to pause the video and try working this out for yourself before watching the solution, and remember it is totally fine to make mistakes! You won't really learn anything otherwise, and nobody is watching. 

So we begin by lining these up vertically and adding place by place starting with the ones place. This is 1 + 1 which is 10. Write 0 and carry the 1. In the 2's place, we have 1 + 0 + 0 which is just a 1, so write that. there's no carry here, so just move to the 4's place. This is 1 + 0 which is just a 1, so write that with no carry. then in the 8's place, we have 1+1 again, so write 0 and carry the 1. Now in the 16's place, we have 1 + 1 + 1. This is technically 3, but in binary that's 11. This is pretty much the same situation as having 10 --- the 11 overflows the single digit space, so we copy down the first 1 and carry the second. That last place there has nothing in it, but you can think of it as two zeroes. 1 + 0 + 0 is 1, and so that's the last part of the result. 

We arrive at the answer 110110, and if you check it, this is indeed 54 in base 10. 

So congratulations, you've now learned the basics behind doing addition in binary without translating to decimal first! Now we have to tackle subtraction, which will happen in the next video. 

# 1.5

In the last video we learned how to do addition in binary. Next up is subtraction. Since it was helpful to first think carefully about how addition worked in base 10 arithmetic, let's begin with a look at how subtraction works in base 10. 

Here's an example: 326 - 152. The way we learned it when we were kids is first, just as with addition, write these on top of each other with the larger number at the top. Then go place by place and subtract only the numbers in each place. In this example the first step is 6 - 2 which is 4, and that goes in the ones place for the answer. But when we move on to the tens place, we have to think about what to do. We have 2 - 5, but this is a negative number, and it doesn't make sense to put -3 in the tens place. So what we do is sort of the opposite of "carrying" in addition --- we "borrow". We borrow a 1 from the next place up and make that 2 into a 12. Now the subtraction makes sense: 12 - 5 is 7, so we put that down in the tens place. The final place used to be 3 - 1 but now it's 2 - 1 since we borrowed so the final answer is 174. 

What exactly is going on with "borrowing"? A lot of kids struggle with that concept and it's no wonder. It feels like an arbitrary rule but there's actually a basis to it. In addition we sometimes have to "carry", when for example we added 4 + 8 in the tens place and we end up with a number that's too large. We add two single digits and get something too big for a single digit, so we split it up --- the 12 becomes 10 + 2 and we add 1 to the next place value up. Borrowing is just this in reverse --- if the subtraction on a single digit results in something too small, we grab one copy of the next place value up and combine it with the current place. We say that we're borrowing a 1, but actually it's a 10 because it's one copy of the next higher place value. That 1 is ten times the size of the digits in the current place. 

Subtraction in binary follows the same rules as subtraction in decimal, but the concept of place value is based on 2s rather than 10s. Let's see how this works with the example 1101 - 110. In decimal this would be 13 minus 6, so the answer should be 7. 

Lining these up with the larger one on top, in the ones place we have 1 - 0. this is just 1, so put that down with no extra steps needed. In the 2's place we have something to think about. 0 - 1 is analogous to having 2 - 5 in the earlier base 10 example. It doesn't make sense to put a negative number in this place in the result (and anyway we haven't defined what it means for a bit to be negative at all yet). So, to follow the same rules, here we are going to borrow from the next place up. 

But it's a little tricky. Borrowing reduces the 1 that's in the 8's place to a 0. And although it says "1", it's from the next place up --- so it's actually a 2, because the next place up is twice the size of the current place. In base 10 it was ten times the size, but we are in base 2. So again borrowing a 1 from here is going to put a 2, not a 10, here. Since a 2 goes here and we're in binary, we will write "10" but that's not ten, that's just the binary for 2. So in our example, we have 10 minus 1, which is really 2 - 1 so the answer is just 1. 

Moving to the 4's place, we have 0 - 1 which is the same situation as previously. So borrow a 1 from the 8s place, turn that 0 into a 10, and subtract to get 1. There's nothing left, so the answer is 111. In decimal, that's "7" which is what we were supposed to get. 

That's tricky, so let's recap. Just as in regular base 10 subtraction, binary subtraction goes one place at a time. If the single bit subtraction can be carried out normally --- if it's 0 - 0, 1-0, or 1-1 -- then do so. Otherwise, if we have a 0 - 1, we borrow from the next place value up. Borrowing a 1 from the next place value up is actually borrowing a 2, or a 10 -- just as in decimal, borrowing a 1 from the next place value up is actually borrowing a 10. Now we can subtract. Continue this process until we reach the end of the digits. 

Let's do a more complex example: 100101 minus 11111. In decimal this is 37 - 31 so the answer is supposed to be 6. Let's go through the process. 

Starting with the 1's digit, it's just 1-1 which is 0, and no borrowing is necessary. Moving to the 2's place, we have 0 - 1. Like we said, we need to borrow a 1 from the next place up. So this 1 that's in the 4's place becomes a 0, and it's a 2 or 10 here in this place. Now 10 minus 1 is 1 and we're done with the 2's place, so move to the 4's place. Because we borrowed, the 4s place now has 0 - 1 so here we are again. What we should do is borrow a 1 from the next place up, but there's nothing there! It says 0. So we have to keep looking in this top number and move up the place values until we can find some place from which we can borrow. The 16's place is also a 0. We don't encounter a 1 until the 32's place. So there's a chain reaction here: Borrow a 1 from the 32's place to have a 10 in the 16's place. But we also have to borrow a 1 from the 16s place to give a 10 to the 8's place. This reduces the 10 to just a 1 in the 16s place and adds 10 in the 8's place. But then borrow from THAT to give a 10 to the 4s place like we originally needed, so the 8s place is now a 1 and the 4s place is now a 10. Subtraction can proceed as usual in the 4s place, since 10 minus 1 is 1. Now move to the 8s place -- we have 1 minus 1 which is 0 without borrowing. The 16s place is the same. And the 32s place is now entirely zero, so there's nothing to do there. 

We end with the number 110. That's a 6 in decimal, and remember that's what the answer was supposed to be. 

This example was quite tricky because we had to borrow from multiple places before subtraction could take place. This happens in decimal subtraction too, and it's just as tricky -- like when we have 3104 minus 731. In this problem. the ones digit is no problem, but in the tens digit we need to borrow a 1 from the hundreds place, but then we have to borrow another 1 from the thousands place to be able to give to the hundreds place.

So in this video you have extended your skill set to include subtracting binary numbers and not just adding them. That was tricky! So well done. Next up is multiplication. 

# 1.6

By now, I hope what you are seeing is that arithmetic in binary works pretty much exactly the same as it does in decimal, but the concept of place value is changed, and understanding binary arithmetic requires a solid understanding of what place value means. As we move from addition and subtraction to multiplication in this video and then division in the next, that theme will continue. As with addition and subtraction, let's revisit the method for multiplying two integers in base 10 and keep a careful eye on place value. 

So look at 263 times 13. Our school algorithm works like this. First position the numbers vertically with the larger one on top. Then proceed to multiply the first number by the ones digit in the second. 3 times 3 is 9. 3 times 6 is 18, and just as in addition that overflows the one-digit space allocated to it, so we write 8 and carry the 1. Now remember that *says* 1, but it's actually a ten because it's the tens digit of 18, and we are going up a place, and every place is ten times larger than the previous place. We carry the 1, then multiply 3 times 2 and *add* the 1 (because that's what carrying is, just adding) to get 7. 

Now we move on to the tens digit in the second number and we're going to store the result in a second row down below. Since this is the tens digit, not the ones digit, we shift everything in that second register over by one unit because the result will start in the tens digit of the answer. In this case the rest is easy because we're multiplying by 1, so we get 263. Then there's a final stage where we add both lower rows, and just as before we sometimes have to carry a digit when adding. Our final answer is 3419. 

Now, how would this work in binary? Let's start simple with 111 times 11. Let's roll with this and just try to follow the same rules as with base 10 multiplication. Well, 111 times 1 is just 111. Then in the second step, it's still 111 times 1 and that is still 111. But when we write it, we're shifting over a unit because we're multiplying by a higher place value, just like we were at this stage of the base 10 multiplication. So you can see that on one level, binary multiplication is shockingly easy because we are only ever multiplying by 1 which means just copy the number down, or by 0 which makes everything zero. 

So now we are just left with an addition problem, which we saw how to do two videos ago. We have 1 + 0 (although we don't write the 0) which is 1. Then 1+1 which is 2, or 10, so put down 0 and carry the 1. Now we have 1+1+1 which is 3 or "11", so put down 1 and carry the other 1. then we have 1+1, which is 10. 10101 is our result and in base 10 that's 16+4+1 which is 21, which is good because the original numbers we multiplied are 7 and 3 in base 10. 

So in fact the only thing really hard about binary multiplication is binary addition at the end. 

Let's try a larger example, 11111 times 101. In base 10 that's 31 and 5, so the answer should be 155. Lining these up, we first multiply by 1 to get 11111. Then shift once, and multiply by 0. Then we need to shift another time since we are now two places higher. Multiply by 1 to get 11111. Now add these together: 1+0 is 1, 1+0 is 1, 1+1 is 0 carry the 1; 1+1+1 is 1 carry the 1, and this happens twice; 1+1 is 0 carry a 1, then finally 10. That gives us 10011011 which you can check is indeed 155. 

One more example will illustrate what happens when the addition at the end starts to stack up. Look at 11111 times 111. That's 31 again but this time it's times 7. The answer should be 217. The multiplication steps are very simple and here's where it leads. Now we have to add -- but there's something new. We've never tried adding a stack of binary integers like this. In decimal, adding a stack of 3 or more integers works pretty much the same as adding just two integers together, although when we do, the numbers can get quite large --- adding two integers together in base 10, we sometimes don't carry just a 1 but for example in this case a 2. 

We could handle adding a stack of binary integers in one of two ways. We could add just the first two levels then add the result to the third level. That would work, but it seems like more work than needed. So let's try to adapt the base 10 method of adding to binary. 

In the ones place, it's just 1 plus two zeroes that we don't write, so we have 1. In the 2s place we have 1 + 1 which is 0, carry the 1. Now let's think. In the 4s place we have 1+1+1+1. This is 4. In binary, this is 100. What this means is that we have 0 here, and we need to carry a 1 to TWO places up. It's like if we added a stack of decimal integers so high that the tens place added up to 106, we'd put down 6 and carry the 1, but not to the next place up but the place AFTER THAT since that 1 is one hundred, not ten. So we'll carry that 1 to the 16s place and leave it until we get there. But next we need to add the 8s place. This is 1+1+1 which is 11, so write 1 and carry the 1 also to the 16s place. In that 16s place now we have 5 1's. That adds up to 5 which in binary is 101. So write 1 and carry the leftmost 1 up two places. Moving on to the 64s place, we have 1+1 which is 0, carry the 1. So finally, we have in the 128s place 1+1+1 which is 11. The result is 11011001. Is it right? Let's convert to base 10: We get 217, which is indeed what we were supposed to get. 

Whew! You've learned at least a couple of things in this video, first the general process of multiplying in binary. And second, possibly more importantly, you've learned that place value is really what all of arithmetic hinges on. If you can understand what all the digits of a number mean in terms of their place value, this unlocks all of arithmetic and also a real understanding of how a machine can do arithmetic. Next up we will tackle our fourth and final arithmetic operation, division in binary. 

# 1.7 

We've been looking at representing integers in base 2 or binary form, which is what computers use for numbers, and doing addition, subtraction, and multiplication in binary, which is what computers do with those numbers. We now come to the fourth of the basic arithmetic operations, division. In this video we're going to see how to do division of two integers in binary without translating to base 10 first. 

Division is a much more involved operation than the other three arithmetic operations. Just as with earlier operations it's helpful to look at an example from the base 10 world, and it's helpful with division to think about the algorithm we use. This algorithm is something in school we learned as *long division*. As with all algorithms, let's think about the inputs needed, what the instructions are, and how to know when to stop and also what the outputs are. Look at the example where we divide 90125 by 12. 

The inputs are the two integers, and the order here definitely matters. The way the long division algorithm proceeds is we first try to divide the divisor, that's the 12, into the left most digit of the dividend, that's the 90125. We write down how many times this goes, in this case how many times 12 goes into 9. Well, 9 is smaller than 12 so 12 doesn't go into it at all. We write 0 in the quotient (which will eventually be part of the answer) to indicate this. To move to the next step, we multiply 0 to 12 and write this below. Then we subtract -- 9 - 0 is 9. Then we bring down the next digit which gives us 90. 

Now repeat the instructions. How many times does 12 go into 90? In this case it does go, in fact 7 times. So put 7 here, and multiply 7 times 12. That gives 84 which goes here, and subtract to get 6. Bring the next digit down and repeat. 12 goes into 61 5 times. Multiply to get 60, write it down, and subtract. Bring the next digit down to get 12. 12 goes into this once. So put 1 here... multiply... subtract... bring down the next digit. 12 does not go into 5, so 0 goes here... multiply... subtract. 

There are no more digits to bring down and 12 cannot go into the previous result, so the algorithm terminates. This shows you another thing that makes division different, namely that it results in not one but two numbers --- a quotient and a remainder. In this case, the answer is a quotient of 7510 and a remainder of 5. So 12 goes into 90125, 7510 times with 5 left over. 

In the spirit of computer science, we really ought to stop here and interrogate this algorithm. Why does it work? Does it always work in the sense of producing correct results? Does it always terminate, or could we feed it input that would cause it to go on forever? Almost never are these questions addressed with kids when they learn the long division algorithm in school. We are going to think about these, however. Not right this second, but in the next video or two when we do a deep dive on the Division Algorithm. 

For now, here's what's important about long division for the purpose of connecting it to binary integers. First, it works by taking the smaller of the two integers and checking to see how many times it goes into successive digit chunks of the larger one. Then it involves a multiplication and a subtraction step. Then we notice that the algorithm stops when we run out of digits and the small number can no longer go into anything. This produces a quotient and a remainder. 

Let's see how this works in binary, by attempting to replicate the long division algorithm for the problem of 11001 divided by 11. In decimal, this is 25 divided by 3, so the answer is supposed to be 8 with a remainder of 1. So set up the problem the same way we do with decimals and proceed the same way. Look at the left most digit of the dividend (that's the  big number in this case). 11 does not divide 1 so put a 0, multiply, and then subtract and bring down the next digit. 11 goes into 11 once, so put 1 here, multiply, subtract, and then bring down the next digit. 11 doesn't go into 0, so put 0, multiply, subtract, then bring down the next digit. Again 11 doesn't go into 0, so put 0, multiply, subtract, then bring down the next digit. 11 doesn't go into 1, so put 0, multilply, subtract. There are no more digits and 11 doesn't go into the digit we have here, so we're done. As hoped, the quotient is 1000 which is 8 in base 10, and the remainder is 1 which is 1 in base 10. 

Let's try that with a more complicated example, 1001100110 divided by 1100. In decimal this is 614 divided by 12, so the answer should be 51 with a remainder of 2. Let's see if it works. 

Setting things up as usual, we check with the digits moving left to right. 1100 is pretty big, so it doesn't go into 1, or 10, or 100, or 1001. So we'll put 0 above each of the four leftmost digits. We could multliply by 0 and subtract but this wouldn't resut in anything. So instead we'll just keep putting 0's until our quotient goes in. Here at this point, it does. How many times does 1100 go into 10111? At first this seems hard but it's actually very easy, because the only digits you have to work with are 0 or 1. So the question isn't "How many times does it go in?" But rather, "Does it go in or not?" If it does, we put a 1. If not, we put a 0 like in the previous steps and move on. We don't have to think about "how many times" the quotient goes in because if it went in more than once, we would have detected this in an earlier digit. 

So here, 1100 goes in once. Put a 1, multiply which is just copying the number down. Now subtract. This is the only really non-easy computation involved. It helps to see this done separately. I'm subtracting 1100 from 10011. The first two digits involve no borrowing. The 4's digit requires that I borrow 1 from the 8s place, but the 8s place is a 0 so I have to move up to the 16s. There's a 1 there, so borrow it to make ths 10 in the 8s place into a 10. But then borrow 1 from *that* to give to the 4s. The 4s place is now a 10 and the 8s place is a 1. Now all the subtraction can take place and we end up with 0111. Notice this is smaller than 1100 --- the 0111 is a 7 in decimal and 1100 is 12 --- so this is like in decimal division, we know we've not made a mistake because the result here is smaller than the divisor. 

Now bring down the next digit, again just like in decimal long division. That gives 1110 here. 1100 goes into this, which we know because 1110 is larger than 1100. We know *that* by looking because 1110 is 1100 with an additional 2 added on there in the second bit. So 1100 goes into this --- therefore put a 1 here, multiply, and subtract. The subtraction's easier this time because there's no borrowing. We are left with 10. Bring down the next digit to get 1000. This is smaller than 1100 so 1100 does not go into it. So we put a 0 up top. I'll multiply by 0 this time so as not to lose track of where I am. Subtracting just gives 100. Bring down the next digit to get 1001. This is still smaller than 1100 so it goes in 0 times. Multiply, and subtract to get 10011. It so happens that we did this earlier, and we saw that 1100 goes into this, so we put a 1, multiply, and the subtraction is the same so we know the result is 111. Bring down the next digit and we get 1110. We saw this earlier too, and we know that 1100 goes in, so put a 1, multiply, and subtract to get 10. 

The long division stops here because there are no more digits to bring down and the result is smaller than the quotient. So looking at the work we have a quotient of 110011 and a remainder of 10. The quotient is 51 in decimal, and the remainder is 2, which is what we were supposed to get. 

I think this needs one more example, and it's time for you to try. Use long division in binary to divide 1100001001 by 10110. Pause the video and work this out. You can check your work *and* get some practice on earlier concepts by converting these to decimal and seeing what the quotient and remainder are. 

So here is the work on this. Check your own work against this and see how you did. Remember you are just now learning this process, so there's a strong chance you might have made a mistake here, especially in one of the subtraction steps, and THAT IS OK. The main thing here is to debug your work, find your mistakes and fix them and then you are good to go. 

In this video, you refreshed your memory about long division and learned how to apply the algorithm for long division to integers represented in binary. You now have all the tools you need to perform all the basic arithmetic that math is based on, using only binary integers. That's a major accomplishment and you should take a moment to feel good about that. 

In the next video, we're going to leave the binary world for a moment and dig a little more into long division by looking at the division algorithm and the very important modulus operator, used in many different computer science applications. See you there. 