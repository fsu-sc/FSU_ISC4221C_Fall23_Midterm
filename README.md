# FSU_ISC4221C_Fall23_Midterm
Example Midterrm from 2011

## Problem 1: 
In the game of word ladders, we are given a starting word and a target word, and asked to
transform the starting word into the target word by changing one letter at a time, each time creating a new,
legal word. The sequence of words formed in this way is the “ladder”. For instance, given the starting word
`foe` and the target word `hat`, we might find the following ladder:

```
foe
fox
fax
fat
hat
```

Your task is to write a program that tries to solve the word ladder game.
 You will be given a list of about 1,000 three letter words that are legal 
 “moves” in the game. Your program should allow the user to type in a starting 
 word and a target word. If no word ladder can be found between the two words,
  then the program should report this. Otherwise, it should print out the word
  ladder that it found to connect the two words. Your list of three letter 
  words is available on Blackboard as wordlist in file `threes.txt`.

### (a.) Describe your approach to this problem in words. A paragraph or two will be enough. In particular:
1. Explain what this problem has to do with graph algorithms;
2. Describe the algorithm you will implement;
3. Explain how you dealt with the special features of this particular problem in order to implement the
algorithm;

### (b.) Demonstrate your program on the following pairs of starting and target words by displaying the output from your program:

1. from `yes` to `nay`;
2. from `fox` to `gnu`;
3. from `oca` to `cub`;


## Problem 2: 
 In this problem we want to develop a retirement calculator based on Monte 
 Carlo simulations. Initially we will assume we have a portfolio which is 
 100% stocks and then we will modify our portfolio to contain stocks and bonds.

### (a)  

In this case we make the following assumptions:

* Our portfolio is **100%** stocks.
* Our stocks provide a return of $p\%$ annually and this return has a standard deviation of $\sigma\%$.
* We withdraw $w\%$ of our initial capital per year (but on a monthly basis) 
for living expenses.  Recall if we want 100 points with mean 0 and 
standard deviation 5 we use $5. ∗ \text{randn(100, 1)}$

Write a routine to estimate the average amount of capital left after **n** years if 
we compound monthly. For ease of grading, set **seed = 1234**. Then add a 
loop to run this simulation **m** times and determine the probability that the 
remaining capital is positive. Note that using Monte Carlo we would estimate 
our yearly percent return as $p \pm \sigma * \text{randn}(1,1)$ it doesn’t
 matter whether we use “+”or “-” because the numbers are distributed around 0.

### (b)  
Assume we have a return of $5\%$ on our stocks with a standard deviation of $15\%$;
 assume our initial capital is $100,000. 
 
 1) Use your code to determine the largest amount (to the nearest $10) of
  the initial capital that can be withdrawn on a monthly basis so that 
  after 25 years the capital is positive with probability at least
    0.9; use 10,000 simulations.
 2) Now suppose that I expect to live 25 years after retirement and I estimate
  that I need $5000 per month for living expenses with a $5\%$ annual 
  increase in this amount. If we use the percentages in (b), then I want
to determine the smallest amount of initial capital I need to guarantee 
(to 90% accuracy ) that I will have a positive capital at the end of 25 years. 
Write a routine to call your Monte Carlo simulation which uses a
Bisection approach to determine the initial capital needed. Start with the 
interval of [100, 000, 5, 100, 000].
Find the result to the nearest $1000. Make a table providing information 
for each iteration of the Bisection Method.

### (d)
 Now suppose that a friend tells me that I am better off with a portfolio 
 that is mixed between stocks and bonds. Assume that stocks yield $2.5\%$
  but are safer with a standard deviation of $5\%$. Make a table of
the initial capital needed if we have the following splits of stocks to bonds: 

<ol type="i">
  <li>100%-0%;</li>
  <li>75%-25%,</li>
  <li>0%-100%</li>
</ol>

 What is the best option for me?