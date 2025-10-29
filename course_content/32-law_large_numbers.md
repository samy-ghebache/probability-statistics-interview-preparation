# Law of Large Numbers

## Concept Overview
The law of large numbers is a fundamental statement about sequences of independent random variables. It describes how the sample mean of these random variables converges to the true mean as the number of samples grows.

## Statement of the Law
Given a sequence of independent random variables, each with the same mean $\mu$ and the same standard deviation $\sigma$ (variance $\sigma^2$):

- Define the **sample mean**:
  - $X_{bar}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$

- The law of large numbers says:
  - As $n$ goes to infinity, $X_{bar}$ converges to $\mu$

## Formal Statement
- For any $\epsilon>0$, the probability that the sample mean $X_{bar}$ differs from the true mean $\mu$ by more than $\epsilon$ approaches zero as $n$ approaches infinity:
  - $P(|X_{bar}-\mu|>\epsilon)\to0$ as $n\to\infty$

## Proof Outline

### Expectation of the Sample Mean
- The expected value of the sample mean is equal to the true mean:
  - $E[X_{bar}]=\mu$

### Variance of the Sample Mean
- The variance of the sample mean (with independent random variables) is:
  - $Var(X_{bar})=\frac{\sigma^2}{n}$

- As $n$ increases, $\frac{\sigma^2}{n}$ gets smaller — the variance of $X_{bar}$ approaches zero as $n$ goes to infinity.

### Using Chebyshev's Inequality
- Chebyshev's inequality provides a formal bound:
  - $P(|X_{bar}-\mu|\geq\epsilon)\leq\frac{Var(X_{bar})}{\epsilon^2}$
  - Substitute the variance:
    - $P(|X_{bar}-\mu|\geq\epsilon)\leq\frac{\sigma^2}{n\epsilon^2}$
  - As $n$ increases, this bound approaches zero.

## Intuitive Picture
- With a small $n$, the sample mean has high variance and may vary widely.
- As $n$ increases, the distribution of $X_{bar}$ becomes sharply peaked around $\mu$.
- This holds for many types of random variables (Bernoulli, Poisson, exponential, gamma, etc.)

## Importance
- The law of large numbers is the foundation for concepts like Monte Carlo sampling, survey sampling, and general inferential statistics.
- The upcoming central limit theorem strengthens this result, showing the average approaches a normal distribution under broad conditions.

## Key Formulas

- Sample mean: $X_{bar}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$
- Expected value of sample mean: $E[X_{bar}]=\mu$
- Variance of sample mean: $Var(X_{bar})=\frac{\sigma^2}{n}$
- Chebyshev bound: $P(|X_{bar}-\mu|\geq\epsilon)\leq\frac{\sigma^2}{n\epsilon^2}$

***