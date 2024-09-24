---
layout: page
title: Probability
permalink: /modules/ready-set-bet/probability
---


## Probability

Intuitively, the **probability** of an event happening represents the ratio of
the number of times something happens in millions of identical experiments,
divided by the total number of experiments performed.

For example, if we roll a six-sided die a million times and count how many times we get a $$5$$, and then divide that count by a million, then we should end up with a value of around $$0.1667$$, representing the fact that the probability of rolling a $$5$$ is $$1/6$$.

## Uniform probabilities

To calculate the probability, we need to set up two things:
* the **sample space** $$\Omega$$, which is the set of all possible outcomes of a random experiment
* the **event** $$E$$, which is a subset of the sample space, representing the outcomes that satisfy the event

If all the possible outcomes in the sample space are equally likely, then the probability is then given by the formula

$$\mathbb{P}(E) = \frac{|E|}{|\Omega|}.$$

**Example:**
Suppose we are rolling a single die and want the probability of getting a $$5$$.
* The experiment here is rolling a die.
* The possible outcomes are getting a number between $$1$$ and $$6$$, so the sample space is

$$\Omega = \{1,2,3,4,5,6\}.$$

* The event is getting a $$5$$, so the event is

$$E = \{5\}.$$

The probability is then

$$\mathbb{P}(E) = \frac{|E|}{|\Omega|} = \frac{1}{6}.$$

**Example:**
Suppose we are rolling a single die and want the probability of getting an even number.
* The experiment here is rolling a die.
* The possible outcomes are getting a number between $$1$$ and $$6$$, so the sample space is

$$\Omega = \{1,2,3,4,5,6\}.$$

* The event is getting an even number is the set of all outcomes where this is true, so it is

$$E = \{2,4,6\}.$$

The probability is then

$$\mathbb{P}(E) = \frac{|E|}{|\Omega|} = \frac{3}{6} = \frac{1}{2}.$$

Thus if we were to roll a die a million times, we would get an even number about half the time.

**Example:**
Suppose we are rolling two dice and want the probability the sum of the dice is $$5$$.
* The experiment here is rolling two dice.
* The possible outcomes are 

$$\begin{align}
\Omega = 
  \{ & (1,1),(1,2),(1,3),(1,4),(1,5),(1,6),(2,1),(2,2),(2,3),(2,4),(2,5),(2,6),\\
     & (3,1),(3,2),(3,3),(3,4),(3,5),(3,6),(4,1),(4,2),(4,3),(4,4),(4,5),(4,6),\\
     & (5,1),(5,2),(5,3),(5,4),(5,5),(5,6),(6,1),(6,2),(6,3),(6,4),(6,5),(6,6)\}.
\end{align}$$

* The event is the sum being $$5$$, so the outcomes with this result are

$$E = \{(1,4),(2,3),(3,2),(4,1)\}.$$

The probability is then

$$\mathbb{P}(E) = \frac{|E|}{|\Omega|} = \frac{4}{36} = \frac{1}{9}.$$

Thus if we were to roll a pair of dice a million times, we would get the sum to be $$5$$ roughly $$1$$ out of every $$9$$ times.

## Expectation values

In applications of probability to the real world, we often assign a value $$f(x)$$ to every possible outcome $$x$$ in the event space.
As an example, imagine we are playing a game of chance at a casino involving rolling a single die.
Depending on the outcome, we lose or gain money according to the following table:

| outcome of die | money gain / lost (dollars) |
| 1 | 3  |
| 2 | -2 |
| 3 | 1  |
| 4 | -2 |
| 5 | 1  | 
| 6 | -2 |

In this way, it is natural to assign $$f(1) = 3$$, $$f(2) = -2$$, $$f(3) = 1$$, and so on...

The **expectation value** $$E$$ is the amount of money we expect to win (or lose) per game on average if we were to play millions of games and calculate the average outcome.
For the above game, if we play a million times, add up all the money won and lost, and then divide by the number of games played, we will end up getting a number around $$-0.1667$$, meaning that on average we will lose about $$17$$ cents per game.

We can calculate the expectation value using the formula

$$E(f) = \text{(probability of $1$)}\cdot\text{(value of 1)} + \text{(probability of $2$)}\cdot\text{(value of 2)} + \dots + \text{(probability of $6$)}\cdot\text{(value of 6)}.$$

Using our notation from above:

$$E(f) = \mathbb{P}(1) f(1) + \mathbb{P}(2) f(2) + \mathbb{P}(3) f(3) + \mathbb{P}(4) f(4) + \mathbb{P}(5) f(5) + \mathbb{P}(6) f(6).$$

Putting in the actual values, we get

$$E(f) = \frac{1}{6}3 + \frac{1}{6}(-2) + \frac{1}{6}1 + \frac{1}{6}(-2) + \frac{1}{6}1 + \frac{1}{6}(-2) = -\frac{1}{6}.$$


**Example:**
Suppose you roll two dice a million times.  Give an estimate of what the average of the sum of the two dice will be, if we average over all million experiments.

In this case, the event space is the same as the previous example above, consisting of pairs if integers $$(i,j)$$ with $$1\leq i,j\leq 6$$.
The value function is the sum $$f(i,j) = i+j$$, so the expectation value is

$$\begin{align}
E(f) 
  & = f(1,1)\frac{1}{36} + f(1,2)\frac{1}{36} + f(1,3)\frac{1}{36} + f(1,4)\frac{1}{36} + f(1,5)\frac{1}{36} + f(1,6)\frac{1}{36}\\
  & + f(2,1)\frac{1}{36} + f(2,2)\frac{1}{36} + f(2,3)\frac{1}{36} + f(2,4)\frac{1}{36} + f(2,5)\frac{1}{36} + f(2,6)\frac{1}{36}\\
  & + f(3,1)\frac{1}{36} + f(3,2)\frac{1}{36} + f(3,3)\frac{1}{36} + f(3,4)\frac{1}{36} + f(3,5)\frac{1}{36} + f(3,6)\frac{1}{36}\\
  & + f(4,1)\frac{1}{36} + f(4,2)\frac{1}{36} + f(4,3)\frac{1}{36} + f(4,4)\frac{1}{36} + f(4,5)\frac{1}{36} + f(4,6)\frac{1}{36}\\
  & + f(5,1)\frac{1}{36} + f(5,2)\frac{1}{36} + f(5,3)\frac{1}{36} + f(5,4)\frac{1}{36} + f(5,5)\frac{1}{36} + f(5,6)\frac{1}{36}\\
  & + f(6,1)\frac{1}{36} + f(6,2)\frac{1}{36} + f(6,3)\frac{1}{36} + f(6,4)\frac{1}{36} + f(6,5)\frac{1}{36} + f(6,6)\frac{1}{36}\\
  & =  2\frac{1}{36} + 3\frac{1}{36} + 4\frac{1}{36} + 5\frac{1}{36} + 6\frac{1}{36} + 7\frac{1}{36}\\
  & +  3\frac{1}{36} + 4\frac{1}{36} + 5\frac{1}{36} + 6\frac{1}{36} + 7\frac{1}{36} + 8\frac{1}{36}\\
  & +  4\frac{1}{36} + 5\frac{1}{36} + 6\frac{1}{36} + 7\frac{1}{36} + 8\frac{1}{36} + 9\frac{1}{36}\\
  & +  5\frac{1}{36} + 6\frac{1}{36} + 7\frac{1}{36} + 8\frac{1}{36} + 9\frac{1}{36} + 10\frac{1}{36}\\
  & +  6\frac{1}{36} + 7\frac{1}{36} + 8\frac{1}{36} + 9\frac{1}{36} + 10\frac{1}{36} + 11\frac{1}{36} \\
  & +  7\frac{1}{36} + 8\frac{1}{36} + 9\frac{1}{36} + 10\frac{1}{36} + 11\frac{1}{36} + 12\frac{1}{36}\\
  & = \frac{27}{36} + \frac{33}{36} + \frac{39}{36} + \frac{45}{36] + \frac{51}{36} + \frac{57}{36} = \frac{252}{36} = 7.
\end{align}$$

So on average the sum looks like it will be around $$5.333$$


## Non-uniform probabilities

In some situtions, the probability of different outcomes of an event in the sample space may be different.
For example, a **biased coin** may have a higher probability of getting a heads than a tails.
The sample space in this case is 
$$\Omega = \{\text{heads},\text{tails}\}$$
consisting of the possible outcomes of heads and tails, respectively.
However, now we also need to specify the probability $$p_{\text{heads}}$$ and $$p_{\text{tails}}$$ of getting a heads and a tails, respectively.



In general, event space is $$\Omega = \{x_1,x_2,x_3,\dots, x_n\}$$ and the probability $$\mathbb P(\{x_j\})$$ is specified by some number $$p_j$$.  Then the expectation value of a function $$f(x)$$ on the sample space is

$$E(f) = p_1f(x_1) + p_2f(x_2) + p_3f(x_3) + \dots + p_nf(x_n).$$


**Example:**  Suppose that have a six-sided die.  Four of the sides are colored blue and the two remaining sides are colored gold.
The sample space describing the experiment of rolling the dice is then


$$\Omega = \{\text{blue},\text{gold}\}.$$

The probabilities of each outcome are given by

$$p_{\text{blue}} = \frac{2}{3},\quad\text{and}\quad p_{\text{gold}} = \frac{1}{3}.$$

Suppose that we make a bet where if we get a gold, we win $$5$$ dollars, but if we get a blue, we lose $$3$$ dollars.
In this case, the value function is

$$f(\text{blue}) = -3,\quad f(\text{gold}) = 5.$$

The expected money won or lost per roll is:

$$E(f) = -3p_{\text{blue}} + 5p_{\text{gold}} = -3\frac{2}{3} + 5\frac{1}{3} = -\frac{1}{5} = -0.20.$$

So per bed, we expect to lose $$20$$ cents.



