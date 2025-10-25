# Exponential Distribution: Hazard Rate

## Introduction
The **exponential distribution** is useful for computing the probability that a rare event (e.g., failure of a light bulb) will happen at time $T$ in the future. This lecture focuses on the **hazard rate** and its relationship to the **memoryless property**.

## Memoryless Property Review
- If $s$ amount of time has already elapsed, the probability of lasting another $T$ amount of time is the same as the probability of lasting $T$ starting at time zero.
- The "clock resets" after time $s$ has passed.
- This is counterintuitive: even if a light bulb has lasted 100 hours, its probability of failing in the future is as if we started from time zero right now.

## Hazard Rate Definition
The **hazard rate** is the probability of failing in the next infinitesimal time interval $dt$, given that the system has already lasted time $t$.

## Computing the Hazard Rate
We want to compute:
$P(T < t+dt | T > t)$

This is the probability of failing between time $t$ and $t+dt$, given that we have already lasted time $t$.

### Step 1: Reformulation
$P(T < t+dt | T > t) = 1 - P(T > t+dt | T > t)$

### Step 2: Apply Memoryless Property
Using the memoryless property, if we have already lasted time $t$, the probability of lasting another $dt$ is:
$P(T > t+dt | T > t) = P(T > dt)$

### Step 3: Use the CDF
The cumulative distribution function (CDF) is:
$P(T > t) = 1 - F(t) = e^{-\lambda t}$

So:
$P(T > dt) = e^{-\lambda dt}$

### Step 4: Substitute
$P(T < t+dt | T > t) = 1 - e^{-\lambda dt}$

### Step 5: Taylor Series Expansion
For small $dt$, we can expand $e^{-\lambda dt}$ using a Taylor series:
$e^{-\lambda dt} = 1 - \lambda dt + \frac{1}{2}\lambda^2 dt^2 - ...$

Substituting:
$P(T < t+dt | T > t) = 1 - (1 - \lambda dt + \frac{1}{2}\lambda^2 dt^2 - ...)$

### Step 6: Small $dt$ Approximation
Since $dt$ is infinitesimal, higher-order terms ($dt^2$, $dt^3$, etc.) are negligible:
$P(T < t+dt | T > t) \approx \lambda dt$

## Hazard Rate Result
The hazard rate is:
$P(t < T < t+dt) = \lambda \times P(T > t) \times dt$

- $\lambda$ is the **hazard rate**: the constant risk of failure per unit time.
- The probability of dying in the next $dt$ is $\lambda dt$.

## Interpretation
- The hazard rate $\lambda dt$ represents the continuous risk of failure.
- By virtue of the light bulb not failing, it has a constant hazard rate $\lambda dt$ for continuing to exist.
- This is a fundamental property of the exponential distribution.

## Summary of Key Formulas
- **Memoryless Property:** $P(T > t+s | T > t) = P(T > s)$
- **CDF:** $F(t) = 1 - e^{-\lambda t}$
- **Hazard Rate:** $P(T < t+dt | T > t) \approx \lambda dt$
- **General Form:** $P(t < T < t+dt) = \lambda \times P(T > t) \times dt$