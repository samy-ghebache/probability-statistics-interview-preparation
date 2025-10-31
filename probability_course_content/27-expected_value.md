# Expected Value of a Random Variable

## Introduction
The **expected value** (or **expectation value**) of a random variable $X$ is one of the most important concepts in probability and statistics. It represents what you would expect the average of many samples from a distribution to be.

## Intuitive Definition
- The expected value is approximately the **center of mass** of your probability distribution.
- It is a weighted average of all possible values of $X$, weighted by their probabilities.

## Formula for Discrete Random Variables
For a discrete random variable (e.g., Bernoulli, binomial, Poisson):

$E[X]=\sum_{k}x_k P(X=x_k)$

- Sum over all possible values $x_k$ that $X$ can take.
- Multiply each value by its probability.

### Example: Coin Flips
- Flip a fair coin 100 times.
- Random variable $X$ = number of heads.
- Possible values: $0,1,2,...,100$.
- Expected value: $E[X]=\sum_{k=0}^{100}k\cdot P(X=k)\approx 50$

## Formula for Continuous Random Variables
For a continuous random variable (e.g., normal/Gaussian distribution):

$E[X]=\int_{-\infty}^{\infty}x\cdot f(x)\,dx$

- Integrate over all possible values of $X$.
- $f(x)$ is the probability density function (PDF).

## Connection to Sample Mean
If you sample $X$ independently $n$ times and compute the sample mean:

$\bar{x}=\frac{1}{n}\sum_{j=1}^{n}x_j$

Then as $n\to\infty$:

$\lim_{n\to\infty}\bar{x}=E[X]=\mu$

This is the **Law of Large Numbers**: the sample mean converges to the expected value.

## Moments
- The expected value is the **first moment** of the distribution.
- Higher moments include:
  - **Second moment**: Related to variance/standard deviation.
  - **Third, fourth, fifth moments**, etc.
- Together, these moments are like a fingerprint or Taylor series expansion of the PDF.
- Related to the Laplace transform of the PDF (moment generating function).

## Potential Pitfalls
- The expected value can be misleading for certain distributions.
- Two completely different distributions can have the same expected value.
- The expected value is not necessarily the most likely value.

### Example: Bimodal Distribution
- A bimodal distribution (two peaks) can have an expected value at the center where the probability is actually zero.
- You would never sample a value near the expected value, yet it is still the center of mass.

## Mode, Mean, and Median
Three important measures of central tendency:

- **Mode**: The most likely value of $X$ (where the PDF is maximized). $\text{mode}=\arg\max P(X)$
- **Mean**: The expected value (weighted average). $\text{mean}=E[X]=\mu$
- **Median**: The middle of the distribution (50th percentile). $\text{median}=X\text{ such that }P(X\leq\text{median})=0.5$

## Robustness: Mean vs. Median
- The **mean** is highly sensitive to outliers.
- The **median** is robust to outliers.

### Example: US Household Wealth
- **Median** household wealth: ~$200k (the peak of the distribution).
- **Mean** household wealth: ~$1 million (shifted by ultra-wealthy outliers like Bezos, Gates, Musk).
- A few extreme outliers shift the mean by a factor of 5, but the median remains at the peak.

## Summary
- Expected value is a weighted average of all possible values.
- For discrete: $E[X]=\sum_{k}x_k P(X=x_k)$
- For continuous: $E[X]=\int_{-\infty}^{\infty}x\cdot f(x)\,dx$
- Sample mean converges to expected value (Law of Large Numbers).
- Expected value is the first moment; higher moments characterize the distribution.
- Not always the most likely value; can be misleading for unusual distributions.
- Mean is sensitive to outliers; median is robust.