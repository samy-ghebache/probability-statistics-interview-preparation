# Geometric Distribution

## Introduction
The **geometric distribution** describes the probability of the first success occurring on the nth trial in a sequence of independent Bernoulli events.

## Setup
- We have a sequence of **Bernoulli events** (independent trials with two outcomes: success or failure).
- Each trial has probability $P$ of success.
- Each trial has probability $1-P$ of failure (often denoted $Q=1-P$).

## Key Question
What is the probability that the **first success** occurs on exactly the **nth trial**?

## Formula for First Success on Exactly the nth Trial
For the first success to occur on exactly the nth trial:
- The first $n-1$ trials must be failures.
- The nth trial must be a success.

Since the trials are independent:

$P(\text{first success on nth trial})=(1-P)^{n-1}\times P$

Or using shorthand $Q=1-P$:

$P(X=n)=Q^{n-1}\times P$

## Definition of Geometric Distribution
A random variable $X$ is **geometrically distributed** with parameter $P$ if:

$P(X=n)=Q^{n-1}\times P$

where $Q=1-P$ and $n=1,2,3,...$

## Example: Rolling a Five
- Rolling a die, looking for a five.
- Probability of success (rolling a five): $P=\frac{1}{6}$
- Probability of failure (not rolling a five): $Q=\frac{5}{6}$
- $X$ is geometrically distributed with parameter $P=\frac{1}{6}$

### Question: Probability it takes at least 10 rolls to get a five

**Method 1: Sum of probabilities**

$P(X\geq 10)=P(X=10)+P(X=11)+P(X=12)+...$

$P(X\geq 10)=Q^9 P+Q^{10}P+Q^{11}P+...$

Factor out $Q^9 P$:

$P(X\geq 10)=Q^9 P(1+Q+Q^2+Q^3+...)$

Using the geometric series formula $1+Q+Q^2+...=\frac{1}{1-Q}$:

$P(X\geq 10)=Q^9 P\times\frac{1}{1-Q}$

Since $1-Q=P$:

$P(X\geq 10)=Q^9 P\times\frac{1}{P}=Q^9$

Therefore:

$P(X\geq 10)=Q^9=\left(\frac{5}{6}\right)^9$

**Method 2: No successes in first 9 rolls**

The probability that it takes at least 10 rolls is equivalent to having no successes in the first 9 rolls:

$P(X\geq 10)=P(\text{no successes in first 9 rolls})=Q^9$

This gives the same result.

## Summary
- The geometric distribution models the number of trials until the first success.
- Formula: $P(X=n)=Q^{n-1}\times P$ where $Q=1-P$
- Probability of first success after at least $n$ trials: $P(X\geq n)=Q^{n-1}$
- Only one parameter $P$ is needed to specify the geometric distribution.