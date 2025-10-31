# Gamma Distribution

## Introduction
The **gamma distribution** is a generalization of the exponential distribution. While the exponential distribution gives waiting times between events, the gamma distribution gives the waiting time for the $r$-th arrival in a Poisson process.

## Context: Poisson Process
- Events arrive at rate $\lambda$ (e.g., emails).
- Events happen at times $T_1, T_2, T_3, \ldots$
- Waiting times between events are exponentially distributed.
- Number of events in time $t$ is Poisson distributed with parameter $\lambda t$.

## Gamma Distribution
- The waiting time for the $r$-th arrival, denoted $T_r$, is **gamma distributed**.
- $T_r$ is the sum of $r$ exponential waiting times:
  - $T_r=W_1+W_2+\cdots+W_r$
- $T_r$ follows a gamma distribution: $T_r\sim\text{Gamma}(r,\lambda)$
- Parameters: $r$ (number of events) and $\lambda$ (rate).

## Derivation (Sketch)
The probability that the waiting time for the $r$-th arrival is greater than $t$ is equivalent to having fewer than $r$ events in time $t$:
- $P(T_r>t)=P(N_t\leq r-1)$

Where $N_t$ is the number of Poisson events in time $t$.

Using the Poisson distribution:
- $P(N_t\leq r-1)=\sum_{k=0}^{r-1}e^{-\lambda t}\frac{(\lambda t)^k}{k!}$

This is the cumulative distribution function (CDF).

Taking the derivative gives the probability density function (PDF):
- $f(t)=e^{-\lambda t}\frac{\lambda^r t^{r-1}}{(r-1)!}$

This is the **gamma distribution PDF**.

## Example: Waiting at the DMV (Series)
- You must talk to 3 different people in sequence (persons A, B, C).
- Each person has an exponentially distributed wait time with expected value 15 minutes.
- Rate: $\lambda=\frac{1}{15}$
- Total waiting time is gamma distributed: $T\sim\text{Gamma}(3,\frac{1}{15})$

## Homework Problem: Parallel Lanes
- At a grocery store, 3 lanes are open.
- Each lane has an exponentially distributed wait time of 15 minutes.
- What is the distribution of your waiting time if you can choose any lane?
- How does this differ from the series case?

## Summary
- **Gamma distribution**: Models waiting time for the $r$-th event in a Poisson process.
- **PDF**: $f(t)=e^{-\lambda t}\frac{\lambda^r t^{r-1}}{(r-1)!}$
- **Parameters**: $r$ (number of events), $\lambda$ (rate).
- **Series case**: Waiting for $r$ sequential exponential events.
- **Parallel case**: Different scenario (homework problem).