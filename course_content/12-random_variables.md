# Random Variables

## Introduction
A **random variable** in probability and statistics is a variable that can take on a set of possible values, each with an associated probability. Just like variables in algebra or calculus, random variables can be discrete or continuous.

## Example: Coin Flips
- Flip a fair coin 4 times.
- The sample space $\Omega$ consists of all possible sequences (e.g., HHHH, HHHT, ..., TTTT).
- There are $2^4 = 16$ possible outcomes.
- Define random variable $X$ as the number of heads in the 4 flips.
- $X$ can take values $0, 1, 2, 3, 4$.

## Discrete vs. Continuous Random Variables
- **Discrete random variable**: Takes on a countable set of values (e.g., number of heads).
- **Continuous random variable**: Takes on any value in a range (e.g., height of Americans).

## Assigning Probabilities
Each value of $X$ has a probability:
- $P(X=0) = \frac{1}{16}$
- $P(X=1) = \frac{4}{16}$
- $P(X=2) = \frac{6}{16}$
- $P(X=3) = \frac{4}{16}$
- $P(X=4) = \frac{1}{16}$

This is an example of the **binomial distribution**.

## Probability Distribution
A **probability distribution** summarizes the probabilities for all possible values of a random variable $X$.
- For the coin flip example, the distribution is:
  - $X$: $0, 1, 2, 3, 4$
  - $P(X)$: $\frac{1}{16}, \frac{4}{16}, \frac{6}{16}, \frac{4}{16}, \frac{1}{16}$

## Probability Density Function (PDF)
- For continuous random variables, the probability distribution is called a **probability density function (PDF)**.
- The PDF is a model of a random process.
- Real-world processes are approximated by mathematical distributions (e.g., binomial, normal).

## Applications
- **Hypothesis testing**: Use data to test if a process follows a certain distribution.
- **Parameter estimation**: Estimate parameters (e.g., mean, standard deviation) from data.
- **Visualization**: Plot probability distributions to summarize data.
- **Computation**: Calculate probabilities for ranges of values.

## Calculus with Random Variables
- For continuous distributions, probability for a range is computed by integrating the PDF:
  - $P(4 < X < 6) = \int_4^6 p(X)\,dX$
- For discrete distributions, use sums:
  - $P(4 < X < 6) = \sum_{k=5}^{5} P(X=k)$

## Functions of Random Variables
- You can define functions on random variables:
  - Expected value: $E[X]$
  - Variance: $Var(X)$
  - Standard deviation: $\sigma_X$
- You can propagate uncertainty through systems (e.g., engineering, dynamics).

## Cumulative Distribution Function (CDF)
- The **cumulative distribution function (CDF)** gives the probability that $X$ is less than a certain value:
  - $F(x) = \int_{-\infty}^x p(X)\,dX$

## Summary
- Random variables provide a concise summary of all probabilities.
- Probability distributions (PDFs for continuous, probability mass functions for discrete) model random processes.
- These tools allow for hypothesis testing, parameter estimation, visualization, and computation.
- You can build functions on random variables and propagate uncertainty through systems.
- The CDF is another useful function related to random variables.

***

All formulas are written as requested. If you want more examples or tailored notes, let me know!