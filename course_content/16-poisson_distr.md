# Poisson Distribution

## Context: When Normal Approximation Fails
- The binomial distribution converges to the normal distribution for large $n$ under modest assumptions.
- However, if the probability $p$ is too small or too large, the normal approximation fails.
- The **Poisson distribution** is the solution for rare events (small $p$).

## Problem with Normal Approximation for Small $p$
### Example
- Let $n=1000$ (large number of trials).
- Let $p=\frac{1}{1000}$ (very rare event).
- Mean: $np=1$
- Variance: $npq\approx 1$ (since $q\approx 0.999\approx 1$).
- Standard deviation: $\sigma\approx 1$

### Issue
- The normal distribution $X\sim N(1,1)$ has mean 1 and standard deviation 1.
- About 16% of this distribution falls below $X=0$.
- Negative number of successes is non-physical (impossible in probability).
- This makes the normal approximation unreliable for small $p$ or $q$.

## Deriving the Poisson Approximation
### Step 1: Define Lambda
- Let $\lambda=np$ (expected number of successes).

### Step 2: Start with Binomial Distribution
- If $X$ is binomial with parameters $n$ and $p$:
  - $P(X=K)=\binom{n}{K}p^K(1-p)^{n-K}$

### Step 3: Expand in Terms of Lambda
- $P(X=K)=\frac{n!}{K!(n-K)!}\left(\frac{\lambda}{n}\right)^K\left(1-\frac{\lambda}{n}\right)^{n-K}$

### Step 4: Rearrange
- $P(X=K)=\frac{\lambda^K}{K!}\cdot\frac{n(n-1)(n-2)\cdots(n-K+1)}{n^K}\cdot\left(1-\frac{\lambda}{n}\right)^n\cdot\left(1-\frac{\lambda}{n}\right)^{-K}$

### Step 5: Take Limit as $n\to\infty$
- $\frac{\lambda^K}{K!}$ remains unchanged.
- $\frac{n(n-1)(n-2)\cdots(n-K+1)}{n^K}\to 1$ (ratio of $K$ terms close to $n$ divided by $K$ copies of $n$).
- $\left(1-\frac{\lambda}{n}\right)^{-K}\to 1$ (goes to $1^{-K}=1$).
- $\lim_{n\to\infty}\left(1-\frac{\lambda}{n}\right)^n=e^{-\lambda}$ (definition of exponential).

### Result: Poisson Distribution
$$P(X=K)=\frac{\lambda^K}{K!}e^{-\lambda}$$

## When to Use Poisson Distribution
- Large $n$ (many trials).
- Small $p$ or $q$ (rare events).
- Governs rare or sporadic events.

## Example: Factory Lights
### Setup
- Probability of one light failing in a day: $p=0.002$
- Number of lights: $n=10000$
- Lambda: $\lambda=np=10000\times 0.002=20$

### Distribution
- The probability of exactly $K$ lights failing in one day is Poisson distributed with $\lambda=20$:
  - $P(X=K)=\frac{20^K}{K!}e^{-20}$

### Applications
- Compute probability of 5 lights failing.
- Compute probability of 1 light failing.
- Compute probability of 20 lights failing.

## Summary of Key Formula
- **Poisson Distribution:**
  - $P(X=K)=\frac{\lambda^K}{K!}e^{-\lambda}$
  - Where $\lambda=np$ (expected number of successes).

## Historical Note
- Poisson distribution used to analyze rare events (e.g., Prussian Army horse deaths).
- Statisticians tested whether observed deaths were expected under random rare events or due to systemic issues (mistreatment, poor management).