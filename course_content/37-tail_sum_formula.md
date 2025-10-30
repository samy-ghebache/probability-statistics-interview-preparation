# Tail Sum Formula for Expectation

## Overview
The **tail sum formula** provides an alternative way of computing the expectation of a discrete random variable $X$ that takes only non-negative values. This result is surprisingly useful and gives a geometric perspective to expectation.

## Assumptions
- $X$ is a discrete random variable.
- $X$ takes non-negative integer values: $0,1,2,\dots,n$.

## Traditional Formula for Expectation
The expectation of $X$, written $E[X]$, is usually defined as:
$E[X]=\sum_{k=0}^{n}kP(X=k)$

For $k=0$, $0 \times P(X=0)=0$, so the sum can be started at $k=1$:
$E[X]=\sum_{k=1}^{n}kP(X=k)$

## Expansion of the Sum
Expanding the sum explicitly:
$E[X]=1P(X=1)+2P(X=2)+3P(X=3)+\dots+nP(X=n)$

If rewritten by grouping terms:
- $P(X=1)$ appears once
- $P(X=2)$ appears in both $2P(X=2)$ and $P(X=2)$ when unrolling multiples
- Continue this process for all $k$

This creates a "triangular" sum where each $P(X=k)$ is counted $k$ times.

## Key Pattern and Rearrangement
The expanded sum becomes:
$E[X]=P(X\geq1)+P(X\geq2)+\dots+P(X\geq n)$

- $P(X\geq k)$ means the probability that $X$ is at least $k$

## The Tail Sum Formula

**Tail Sum Formula:**
$E[X]=\sum_{k=1}^{n}P(X\geq k)$

- For each $k$ from $1$ to $n$, add up the probability that $X$ is at least $k$.

## Relation to Cumulative Distribution Function
- $P(X\geq k)$ is the "tail" probability: $1$ minus the cumulative distribution function up to $k-1$.
- $P(X\geq k)=1-F(k-1)$, where $F$ is the cumulative distribution function.

## Interpretation
- The formula gives a geometric and intuitive way of understanding expectation as the sum of the "tails" of the distribution.
- Each row in the expanded sum is the probability that $X$ is at least some value $k$.

## Summary Table

| Formula                          | Meaning                                         |
|-----------------------------------|-------------------------------------------------|
| $E[X]=\sum_{k=0}^{n}kP(X=k)$     | Standard definition of expectation              |
| $E[X]=\sum_{k=1}^{n}P(X\geq k)$  | Tail sum formula for non-negative $X$           |
