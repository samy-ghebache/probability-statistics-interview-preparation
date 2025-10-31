# Markov's Inequality

## Introduction
Markov's inequality is a fundamental result in probability that leads to the proof of Chebyshev's inequality, the law of large numbers, and the central limit theorem. These theorems describe how probability distributions behave in the limit of large $n$.

## Statement of Markov's Inequality
For a non-negative random variable $X$ (i.e., $X\geq 0$), the probability that $X$ is greater than or equal to some value $a$ is bounded by:

$P(X\geq a)\leq\frac{E[X]}{a}$

where $E[X]$ is the expected value of $X$.

## Intuitive Example
Suppose $E[X]=10$.

Then:

$P(X\geq 20)\leq\frac{10}{20}=\frac{1}{2}$

**Interpretation**: If the expected value is 10, at most half of the probability distribution can be to the right of 20. If more than half were to the right of 20, there would not be enough probability mass on the left to balance out to an expected value of 10.

The limiting case occurs when half the distribution is stacked at $X=20$ and the other half is stacked at $X=0$.

## Proof of Markov's Inequality
### Step 1: Definition of Expected Value
For a discrete random variable $X$:

$E[X]=\sum_{x}x\cdot P(X=x)$

where the sum is over all possible values of $x$.

### Step 2: Restrict the Sum
Since $X$ is non-negative and probabilities are non-negative, restricting the sum to $x\geq a$ gives:

$E[X]\geq\sum_{x\geq a}x\cdot P(X=x)$

This inequality holds because we are summing over fewer positive terms.

### Step 3: Replace $x$ with $a$
For all $x\geq a$, we have $x\geq a$. Therefore:

$\sum_{x\geq a}x\cdot P(X=x)\geq\sum_{x\geq a}a\cdot P(X=x)$

### Step 4: Factor Out $a$
$\sum_{x\geq a}a\cdot P(X=x)=a\sum_{x\geq a}P(X=x)=a\cdot P(X\geq a)$

### Step 5: Combine Inequalities
From Steps 1-4:

$E[X]\geq a\cdot P(X\geq a)$

Dividing both sides by $a$:

$P(X\geq a)\leq\frac{E[X]}{a}$

This completes the proof.

## Summary
- Markov's inequality provides an upper bound on the probability that a non-negative random variable exceeds a certain value.
- The inequality is intuitive: if the mean is small, the probability of large values must also be small.
- This result is foundational for proving Chebyshev's inequality and the law of large numbers.

## Key Formula
$P(X\geq a)\leq\frac{E[X]}{a}$

for $X\geq 0$ and $a>0$.