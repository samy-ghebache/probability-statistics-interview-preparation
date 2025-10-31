# Binomial and Normal Distributions

## Introduction
The binomial distribution for the number of successes in $n$ independent Bernoulli trials converges to a normal (Gaussian) distribution in the limit of large $n$. This lecture derives this relationship and demonstrates it with Python code.

## Bernoulli Random Variable
- A **Bernoulli trial** has two outcomes: success (probability $p$) or failure (probability $q=1-p$).
- Example: A single coin flip is Bernoulli with $p=\frac{1}{2}$.

## Binomial Distribution
- A **binomial random variable** $X$ counts the number of successes in $n$ independent Bernoulli trials.
- Notation: $X\sim\text{Binomial}(n,p)$
- Formula: $P(X=k)=\binom{n}{k}p^kq^{n-k}$
- Where $\binom{n}{k}$ is "n choose k" (the binomial coefficient).
- This means: $X=B_1+B_2+\cdots+B_n$, where each $B_i$ is Bernoulli with probability $p$.

### Examples
- Number of heads in 10 coin flips: Binomial$(10,\frac{1}{2})$
- Number of sixes in 20 dice rolls: Binomial$(20,\frac{1}{6})$

## Normal Distribution
- For large $n$, the binomial distribution converges to a **normal (Gaussian) distribution**.
- Notation: $X\sim N(\mu,\sigma^2)$
- Mean: $\mu=n\times p$
- Variance: $\sigma^2=n\times p\times q$
- Standard deviation: $\sigma=\sqrt{n\times p\times q}$

### Normal Distribution Formula
The probability density function is:
$$P(X=x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$

### When is the Normal Approximation Valid?
- Large $n$ (roughly $n\geq 30$ is a good rule of thumb)
- $n\times p\times q$ not too small
- $p$ and $q$ not too small (otherwise use Poisson distribution)

## Advantages of Normal Distribution
- **Easier to compute** probabilities compared to summing binomial terms.
- Example: Computing the probability that the number of heads in 100 coin flips is between 20 and 50 is easier with the normal distribution.

## Python Implementation
### Import Libraries
```python
import numpy as np
import scipy as sp
from scipy import special
import matplotlib.pyplot as plt
```

### Parameters
- $n=100$ (number of trials)
- $p=0.5$ (probability of success)
- $q=0.5$ (probability of failure)

### Binomial Distribution (Exact)
For $k=0$ to $n$:
$$P(X=k)=\binom{n}{k}p^kq^{n-k}$$

### Normal Approximation
- Mean: $\mu=n\times p$
- Standard deviation: $\sigma=\sqrt{n\times p\times q}$
- Formula: $P(X=x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

## Results from Python
### Case 1: $n=100$, $p=0.5$
- Binomial and normal distributions are almost perfectly overlapping.
- Very difficult to see any difference between the two curves.

### Case 2: $n=30$, $p=0.5$
- Still a very good approximation.
- $n\approx 30$ is where the normal approximation starts to become very accurate.

### Case 3: $n=10$, $p=0.5$
- Some discretization effects are visible.
- Still surprisingly good approximation.

### Case 4: $n=5$, $p=0.5$
- Normal approximation breaks down.
- Too few trials for the normal approximation to be accurate.

### Case 5: $n=30$, $p=0.02$ (small $p$)
- Normal distribution predicts negative successes (non-physical).
- When $p$ or $q$ is very small, the normal approximation fails.
- In this case, use the **Poisson distribution** instead.

## Central Limit Theorem
- If you add up $n$ independent identically distributed random variables, their sum converges to a normal distribution for large $n$.
- This holds for almost any distribution (uniform, Poisson, geometric, etc.).
- The binomial distribution is a special case: it is the sum of $n$ independent Bernoulli random variables.
- This is one of the most important results in probability theory.

## Summary
- The binomial distribution $\text{Binomial}(n,p)$ converges to the normal distribution $N(n\times p,n\times p\times q)$ for large $n$.
- The normal approximation is accurate for $n\geq 30$ and when $p$ and $q$ are not too small.
- The normal distribution is easier to compute with than the binomial distribution.
- When $p$ or $q$ is very small, use the Poisson distribution instead.
- This convergence is an example of the Central Limit Theorem.