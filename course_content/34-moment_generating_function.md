# Moment Generating Functions

## Introduction
The **moment generating function** (MGF) is a central concept in probability theory, helping compute moments (expectation, variance, skewness, kurtosis) and serving as a powerful tool for proving major theorems such as the Central Limit Theorem.

## What Is a Moment?
- The $n$-th moment of a distribution is the expected value of $X^n$ for a random variable $X$.
- Common moments:
  - First moment: Mean
  - Second moment: Variance (specifically, variance $= E[X^2]-(E[X])^2$)
  - Third moment: Skewness ($E[X^3]$)
  - Fourth moment: Kurtosis ($E[X^4]$)
- Moments uniquely characterize many distributions.

## Definition of the Moment Generating Function

### Discrete Random Variables
The moment generating function $M_X(t)$ for a discrete random variable $X$ is defined as:
$M_X(t)=\sum_{x}e^{tx}P(X=x)$

### Continuous Random Variables
For a continuous random variable $X$:
$M_X(t)=\int_{-\infty}^{\infty}e^{tx}f(x)dx$

$f(x)$ is the probability density function of $X$.

## Key Theorem: Moments from the MGF
The $n$-th derivative of the moment generating function evaluated at $t=0$ gives the $n$-th moment:
$E[X^n]=\frac{d^n}{dt^n}M_X(t)\bigg|_{t=0}$

## Examples

### Poisson Distribution
Let $X$ be Poisson with parameter $\lambda$.
- Probability mass function:
  $P(X=k)=\frac{\lambda^k e^{-\lambda}}{k!}$
- Moment generating function:
  $M_X(t)=\sum_{k=0}^{\infty}e^{tk}\frac{\lambda^k e^{-\lambda}}{k!}$
  $=e^{-\lambda}\sum_{k=0}^{\infty}\frac{(\lambda e^{t})^k}{k!}$
  $=e^{-\lambda}e^{\lambda e^{t}}$
  $=e^{\lambda(e^{t}-1)}$

### Normal Distribution
Let $X$ be standard normal ($\mu=0$, $\sigma^2=1$).
- Probability density function:
  $f(x)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}$
- Moment generating function:
  $M_X(t)=\int_{-\infty}^{\infty}e^{tx}\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}dx$
  $=e^{\frac{t^2}{2}}$

### Exponential Distribution
Let $X$ be exponential with parameter $\lambda$.
- Probability density function:
  $f(x)=\lambda e^{-\lambda x}$
- Moment generating function:
  $M_X(t)=\int_{0}^{\infty}e^{tx}\lambda e^{-\lambda x}dx$
  $=\frac{\lambda}{\lambda-t}$, for $t<\lambda$

## Summary of Properties
- MGFs generate all moments of a distribution efficiently.
- $M_X(t)$ uniquely determines the cumulative distribution for many distributions.
- Useful for characterizing, proving, and calculating expectations, variances, and higher moments.
- The moment generating function for common distributions:
  - Poisson: $e^{\lambda(e^{t}-1)}$
  - Normal: $e^{\frac{t^2}{2}}$
  - Exponential: $\frac{\lambda}{\lambda-t}$ for $t<\lambda$

## Applications
- Calculating moments: Mean, variance, skewness, kurtosis
- Proving Central Limit Theorem
- Modeling distributions and their cumulative probabilities
- Calculation and simplification in probability and statistics

***