# Answers: Counting Level 1 and Level 2, version 3

## Counting Level 1

(1) There are $2^6 = 64$ palindrome bitstrings of length 11. The first (leftmost) six bits can be chosen freely (for example, 101110xxxxx) but then the remaining five bits have to mirror the first five (example: 10111011101). Since each bit has two choices, that counts up to $2^6$. 

(2a) With no restrictions, there are 50 ways to select first prize, then 49 ways to select second prize, then 48 ways to select third prize for a total of $50 \cdot 49 \cdot 48 = 117600$. 

(2b) There are three cases for the person with ticket 22: That person can win first prize, second prize, or third prize. If he wins first prize, then there are 49 ways to allocate second prize and then 48 ways to give third prize for a total of $49 \cdot 48 = 2352$. If he wins second prize, there are 49 ways to give first prize and 48 ways to give third prize, for a total again of 2352. Finally if he wins third prize then there are 49 ways to give first prize and 48 ways to give second prize, for a total of 2352. So the complete total number of ways to give out the prizes is $3 \times 2352 = 7056$. 

(3a) Since each coin flip can be heads or tails, there are $2^8 = 256$ ways this can happen. 

(3b) Of the 8 flips, we want 3 of them to be heads. The total number of such selections is $\binom{8}{3} = 56$. 

## Counting Level 2

(1a) Think of BCD as a single block that can be permuted around the string, like a new letter. Therefore the question is asking how many ways are there to permute five objects -- the letter A, the block BCD, the letter E, the letter F, and the letter G. That number is $5! = 120$. 

(1b) Similarly think of ABC and DE as being blocks, like new letters. We are now permuting four objects: ABC, DE, F, and G. There are $4! = 24$ ways to do this. 

(1c) The answer here is 0, because it's impossible to have the strings ABC and BED at all under these conditions (it would force at least one letter to repeat, which is prohibited). 

(2) Break this into cases where we count the number of 1-element, 3-element, 5-element, 7-element, and 9-element subsets. Count each case and then add the results (because those are separate, independent cases). The answer will be 

$$\binom{10}{1} + \binom{10}{3} + \binom{10}{5} + \binom{10}{7} + \binom{10}{9} = 10 + 120 + 252 + 120 + 10 =  512$$

Alternatively and simpler: There are $2^{10}$ subsets in all and exactly half of those will have an odd number of elements, so $2^9 = 512$. 

(3) Use the Binomial Theorem and look at the term in the sum when $i = 7$. The coefficient is $\binom{12}{7} = 792$. 