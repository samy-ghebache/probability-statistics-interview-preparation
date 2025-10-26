# Variance and Standard Deviation

## Introduction
- **Expected value** (mean $\mu$): Measures the center of mass of a distribution.
- **Variance**: Measures the average squared deviation of $X$ from the mean $\mu$.
- **Standard deviation**: The square root of the variance, measuring the spread of the distribution.

## Visual Intuition
For a Gaussian (normal) distribution:
- The mean $\mu$ is the center of the distribution.
- The standard deviation $\sigma$ indicates the spread around $\mu$.
- About 68% of the distribution lies within $\pm 1\sigma$ of $\mu$.
- Additional standard deviations: $\pm 2\sigma$, $\pm 3\sigma$, etc.

## Definition of Variance
The variance of $X$ is defined as:

$\text{Var}(X)=E[(X-\mu)^2]$

This is the expected value of the squared deviation of $X$ from the mean $\mu$.

## Useful Formula for Variance
The variance can also be computed as:

$\text{Var}(X)=E[X^2]-E[X]^2$

Or equivalently:

$\text{Var}(X)=E[X^2]-\mu^2$

## Derivation
Starting from the definition:

$\text{Var}(X)=E[(X-\mu)^2]$

Expand the squared term:

$\text{Var}(X)=E[X^2-2\mu X+\mu^2]$

Use linearity of expectation:

$\text{Var}(X)=E[X^2]+E[-2\mu X]+E[\mu^2]$

Simplify each term:
- $E[\mu^2]=\mu^2$ (expectation of a constant is the constant)
- $E[-2\mu X]=-2\mu E[X]=-2\mu^2$ (expectation of constant times $X$ is constant times $E[X]$)

Thus:

$\text{Var}(X)=E[X^2]-2\mu^2+\mu^2=E[X^2]-\mu^2$

## Computing the Second Moment
For a continuous random variable, the second moment is:

$E[X^2]=\int_{-\infty}^{\infty}x^2 p(x)\,dx$

This is the **second moment** of the probability density function.

## Standard Deviation
The standard deviation is:

$\text{SD}(X)=\sqrt{\text{Var}(X)}$

It measures the spread of the distribution.

## Gaussian Distribution
For a normally distributed random variable $X$ with mean $\mu$ and variance $\sigma^2$:

$p(x)=\frac{1}{\sqrt{2\pi\sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

- $E[X]=\mu$
- $\text{Var}(X)=\sigma^2$
- $\text{SD}(X)=\sigma$

The Gaussian distribution is completely characterized by its first and second moments (mean and variance).

## Properties of Variance
### Variance is Always Non-Negative
$\text{Var}(X)\geq 0$

This is because variance is the expectation of a squared quantity.

### Variance of Independent Variables
If $X$ and $Y$ are independent:

$\text{Var}(X+Y)=\text{Var}(X)+\text{Var}(Y)$

**Important:** This is NOT true if $X$ and $Y$ are dependent.

For example:

$\text{Var}(2X)\neq 2\text{Var}(X)$

Instead:

$\text{Var}(2X)=4\text{Var}(X)$

## Moments
- **First moment**: Mean $\mu=E[X]$
- **Second moment**: $E[X^2]$
- Higher moments (3rd, 4th, etc.) characterize more complex distributions with asymmetries and other features.
- For well-behaved distributions like the Gaussian, the first and second moments uniquely determine the distribution.

## Summary
- Variance measures average squared deviation from the mean.
- Formula: $\text{Var}(X)=E[X^2]-\mu^2$
- Standard deviation is the square root of variance.
- For independent variables: $\text{Var}(X+Y)=\text{Var}(X)+\text{Var}(Y)$
- Gaussian distributions are fully characterized by mean and variance.