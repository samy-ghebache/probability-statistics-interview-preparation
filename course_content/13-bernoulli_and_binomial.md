# Bernoulli and Binomial Random Variables

## Bernoulli Random Variable
A **Bernoulli random variable** $X$ can only take two values: 0 or 1.

### Range
- $X\in\{0,1\}$
- $1$ means the event **did happen** (success).
- $0$ means the event **did not happen** (failure).

### Examples
- Coin flip (getting heads).
- Dice roll (getting a six).
- Manufacturing (good part vs. bad part).

### Probabilities
- Probability of success: $P(X=1)=p$
- Probability of failure: $P(X=0)=1-p=q$
- Note: $p+q=1$

For a fair coin, $p=\frac{1}{2}$. For rolling a six on a die, $p=\frac{1}{6}$.

## Binomial Random Variable
A **binomial random variable** is the sum of $n$ independent Bernoulli trials.

### Definition
- Perform $n$ independent Bernoulli random trials: $B_1,B_2,...,B_n$
- Let $X$ = total number of successes
- $X=B_1+B_2+...+B_n$

### Notation
- $X\sim\text{Binomial}(n,p)$
- $n$ = number of trials
- $p$ = probability of success on each trial

### Probability Formula
The probability of getting exactly $k$ successes out of $n$ trials is:

$P(X=k)=\binom{n}{k}p^kq^{n-k}$

where:
- $\binom{n}{k}$ is the binomial coefficient (n choose k), counting the number of ways to get $k$ successes out of $n$ trials.
- $p^k$ is the probability of $k$ successes.
- $q^{n-k}$ is the probability of $n-k$ failures.

## Example: $n=2$
For two trials with success probability $p$ and failure probability $q$:

- $P(X=0)=q^2$ (both trials fail)
- $P(X=1)=2pq$ (one success, one failure)
- $P(X=2)=p^2$ (both trials succeed)

These probabilities sum to $1$: $q^2+2pq+p^2=(p+q)^2=1^2=1$

The coefficients $1,2,1$ come from Pascal's triangle (row 2).

## Example: $n=3$
For three trials:

- $P(X=0)=q^3$
- $P(X=1)=3pq^2$
- $P(X=2)=3p^2q$
- $P(X=3)=p^3$

The coefficients $1,3,3,1$ come from Pascal's triangle (row 3).

## Example: Three Sixes on 12 Dice Rolls
What is the probability of getting three sixes when rolling a die 12 times?

- $X\sim\text{Binomial}(12,\frac{1}{6})$
- $P(X=3)=\binom{12}{3}\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^9$

## Large $n$ Approximations
### Normal Distribution
For large $n$, if $n\times p\times q$ is not too small, the binomial distribution approximates a **normal distribution**:

$X\sim\text{Normal}(\mu,\sigma)$

where:
- Mean: $\mu=np$
- Standard deviation: $\sigma=\sqrt{npq}$

### Poisson Distribution
If $np$ or $nq$ is small (rare events), the binomial distribution approximates a **Poisson distribution**:

$X\sim\text{Poisson}(\lambda)$

where:
- $\lambda=np$

## Key Formulas Summary
- **Bernoulli probabilities:** $P(X=1)=p$, $P(X=0)=q=1-p$
- **Binomial probability:** $P(X=k)=\binom{n}{k}p^kq^{n-k}$
- **Normal approximation (large $n$):** Mean $=np$, Standard deviation $=\sqrt{npq}$
- **Poisson approximation (rare events):** $\lambda=np$