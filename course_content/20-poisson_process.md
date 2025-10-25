# Relationship Between Exponential and Poisson Distributions

## Introduction
The exponential distribution and Poisson distribution are intimately related. The exponential distribution describes the waiting time between rare events, while the Poisson distribution describes the number of events in a given time interval.

## Setup: String of Random Events
- Consider a string of events (e.g., receiving emails) occurring at some rate.
- These events happen at times $T_1, T_2, T_3, \ldots, T_N$ on a timeline from 0 to $T$.
- Define waiting times between events: $W_1, W_2, W_3, \ldots$ (time between consecutive events).

## Waiting Times: Exponential Distribution
- **Waiting times $W_J$ are independent and exponentially distributed** with parameter $\lambda$.
- $\lambda$ is the **rate of events** (e.g., 5 emails per minute).
- The waiting time between events follows an exponential distribution.

## Number of Events: Poisson Distribution
- The **number of events in a time interval $t$** is Poisson distributed.
- The Poisson parameter is $\lambda t$ (rate $\times$ time).
- Formula: Number of events in time $t$ is Poisson with parameter $\lambda t$.

## Key Insight
- **Waiting times** (continuous): Exponentially distributed.
- **Number of events** (discrete): Poisson distributed.
- These describe the same random process from different perspectives.

## Example: Email Arrivals
- Emails arrive at rate $\lambda=5$ per minute.

### Probability of Waiting $t$ Minutes for Next Email
- This is the probability that the waiting time $T>t$.
- Using the exponential distribution:
  - $P(T>t)=1-P(T<t)=e^{-5t}$

### Probability of No Emails in Next $t$ Minutes
- This is a discrete event: getting exactly $k=0$ emails in time $t$.
- Using the Poisson distribution:
  - $P(k=0)=\frac{\lambda^k e^{-\lambda t}}{k!}=\frac{5^0 e^{-5t}}{0!}=e^{-5t}$
- **Notice:** $P(T>t)=P(k=0)=e^{-5t}$ (identical probabilities, same event from different viewpoints).

### Probability of Exactly One Email in $t$ Minutes
- Using the Poisson distribution:
  - $P(k=1)=\frac{\lambda^1 e^{-\lambda t}}{1!}=5e^{-5t}$
- This is 5 times more likely than getting no emails.

## Summary of Key Formulas
- **Exponential distribution (waiting time):**
  - $P(T>t)=e^{-\lambda t}$
- **Poisson distribution (number of events):**
  - $P(k \text{ events in time } t)=\frac{(\lambda t)^k e^{-\lambda t}}{k!}$
- **Connection:**
  - Probability of waiting time $>t$ equals probability of 0 events in time $t$.

## Poisson Processes
- Random events occurring at rate $\lambda$ are called **Poisson processes**.
- Waiting times are exponentially distributed (continuous).
- Number of events in a fixed time interval is Poisson distributed (discrete).