# Problem_Set_9


Single nucleotide polymorphisms (SNPs) occur when one base in DNA is changed to another. These changes can be illustrated using this diagram below 

<img src="https://user-images.githubusercontent.com/47755288/222260256-08b04e75-9c67-45fb-8863-479fdaaf88b0.png" width="300">

We are going to use a Markov Chain to examine the probability of a observing a particular basepair after N mutational events. 

$nsbp;

## Problem A

In R create a transition matrix such that the probability of going from any base to any other is equal. The probability of staying at a base during a mutational event should be 0. _Note_ It may be helpful to give your rows and columns names. 

## Question A.1
Report your transition matrix

## Question A.2

If you start at the base T, what is the probability that the state will return to T at 4 mutational events. Use the matrix math for this, which may require the ```expm``` package. 

## Question A.3

After how many mutational events is the probability of being at any base equal if you start at state T. I.e. How many mutational events occur such that p(A)=p(T)=p(C)=p(G)=approximately 0.25

## Question A.4

If you start at either purine with an equal probability, what is the probability that you will be at a purine after 4 mutational events? 


## Problem B

Transitions and transversions **do not** occur at the same rate. There are known differences between the rates at which one base mutates to another. One study created this map of rates of change between the bases. 

![image](https://user-images.githubusercontent.com/47755288/222265387-8a41eead-63fb-4bba-ba29-3afb379e63d4.png)

Create a new transition matrix using the data in the above figure. _NOTE_ The percentages are not the probabilities. You should use those percentages to compute the probabilities! There will be a new/unique probability for all positions in the matrix except for the no-change probabilities. 

## Question B.1

Report your new transition matrix.

## Question B.2

If you start at the base T, what is the probability that the state will return to T at 4 mutational events. Use the matrix math for this, which may require the ```expm``` package. 

## Question B.3
Plot the probability of the state being T for 20 mutational changes. 

## Question B.4
If you start at either purine with an equal probability, what is the probability that you will be at a purine after 4 mutational events?

$nbsp;

## Problem C

Most mutational events are fixed by DNA repair enzymes and are not passed on to the next generation. Therefore, what we modeled above were "observable" mutational events. A more realistic estimate is that the base stays the same in 99.9% (or 999 out of 1000) mutational events. 

1. Create a new transition matrix from the previous matrix that adjusts the probabilities so that there is a 0.999 probability of staying at the same base **and** the remaining probabilities are proportional to problem 2. _Hint_ start by dividing your previous matrix by 1000
2. If you start at the base T, what is the probability that the state will be any other state than T after 4 mutational events. Use the matrix math for this, which may require the ```expm``` package. 
3. If you start at the base T, what is the probability that the state will be any other state than T after 400 mutational events. Use the matrix math for this, which may require the ```expm``` package. 
4. After 10,000 mutational events, what base(s) are you most likley to end up at for starting at
- A
- T
- C
- G

BONUS: What evolutionary phenomenon did we demonstrate in the last step (Problem 3, question 4) 
