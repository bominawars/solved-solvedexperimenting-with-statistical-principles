Download Link: https://assignmentchef.com/product/solved-solvedexperimenting-with-statistical-principles
<br>
In this assignment you will experiment with random variation over discrete events. It will be very helpful to use the analytical results and the experimental results to help verify the other is correct. If they do not align,you are probably doing something wrong (this is a very powerful and important thing to do whenever working with real data).

As usual, it is highly recommended that you use LaTeX for this assignment. If you do not, you may lose points if your assignment is difﬁcult to read or hard to follow.

Find a sample form in this directory: http://www.cs.utah.edu/˜jeffp/teaching/latex/1 Birthday Paradox (30 points) Consider a domain of size n = 4000.

A: (5 points) Generate random numbers in the domain [n] until two have the same value. How many random trials did this take?

We will use k to represent this value.

B: (10 points) Repeat the experiment m = 300 times, and record for each how many random trials this took. Plot this data as a cumulative density plot where the x-axis records the number of trials required k, and the y-axis records the fraction of experiments that succeeded (a collision) after k trials. The plot should showacurvethatstartsata y valueof 0,andincreasesas k increases,andeventuallyreachesa y valueof 1.

C: (5 points) Empiricallyestimatetheexpectedthenumberof k randomtrialsinordertohaveacollision. That is, add up all values k, and divide by m.

D: (10 points) Describe how you implemented this experiment and how long it took for m = 300 trials. Showaplotoftheruntimeasyougraduallyincreasetheparameters n and m. (Foratleast3ﬁxedvalues of m between 300 and 10,000, plot the time as a function of n.)

You should be able to reach values of n = 1,000,000 and m = 10,000. 2 Coupon Collectors (30 points) Consider a domain [n] of size n = 200.

A: (5 points) Generate random numbers in the domain [n] until every value i ∈ [n] has had one random number equal to i. How many random trials did this take? We will use k to represent this value.

B: (10 points) Repeat step A for m = 300 times, and for each repetition record the value k of how many random trials we required to collect all values i ∈ [n]. Make a cumulative density plot as in 1.B.

C: (5 points) Use the above results to calculate the empirical expected value of k. D: (10 points) Describe how you implemented this experiment and how long it took for n = 200 and m = 300 trials.

Show a plot of the runtime as you gradually increase the parameters n and m. (For at least 3 ﬁxed values of m between 300 and 5,000, plot the time as a function of n.) You should be able to reach n = 20,000 and m = 5,000. 3 Comparing Experiments to Analysis (24 points)

A: (12 points) Calculate analytically (using formulas from the notes) the number of random trials needed so there is a collision with probability at least 0.5 when the domain size is n = 4000. (Show your work.) How does this compare to your results from

Q1.C?B: (12 points) Calculate analytically (using formulas from the notes) the expected number of random trials before all elements are witnessed in a domain of size n = 200? (Show your work.) How does this compare to your results from

Q2.C? 4 Random Numbers (16 points) Considerwhentheonlyrandomfunctionyouhaveisonethatchosesabitatrandom. Inparticularrand-bit() returns 0 or 1 at uniformly random. A: (6 points) How can you use this to create a random integer number between 1 and n = 1024?

B: (5 points) Describe a Las Vegas randomized algorithm (“Las Vegas” means: it may run for ever, but youcanboundhowlongyouexpectittotake,andwhenitﬁnishesyouknowitisdone)forwhen n = 1000.

C: (5 points) How many calls does this take as a function of n (say I were to increase the value n, how does the number of calls to rand-bit() change)? Keep in mind that in many settings generating a random bit is much more expensive that a standard CPU operation (like an addition, if statement, or a memory reference), so it is critical to minimize them.

5 BONUS (2 points) Consider a domain size n and let k be the number of random trials run, where each trial obtains each value i ∈ [n] with probability 1/n. Let fi denote the number of trials that have value i. Note that for each i ∈ [n] we have E[fi] = k/n. Let µ = maxi∈[n] fi/k.

Consider some parameter δ ∈ (0,1). As a function of parameter δ, how large does k need to be forPr [|µ − 1/n| ≥ 0.05] ≤ δ? That is, how large does k need to be for all counts to be within 5% of the average with probability δ? (Fine print: you don’t need to calculate this exactly, but describe an function of δ for the value k which can be prove this probabilistic property.) How does this change if we want Pr[|µ−1/n|≥ 0.005] ≤ δ (for 0.5% accuracy)? (Make sure to show your work)