# Moment Generating Function (MGF) Property

## Introduction
The moment generating function (MGF) is essentially the Laplace transform of the probability density function (PDF). It is a powerful tool for computing expectations, variance, and higher order moments of a distribution. The MGF is crucial in proving the central limit theorem, which states that the sum of many independent random variables tends toward the normal distribution.

## Key Property: Sums of Independent Random Variables
Let $x$ and $y$ be independent random variables (not necessarily from the same distribution) with moment generating functions $m_x(t)$ and $m_y(t)$.

- Define a new variable: $z=x+y$
- The moment generating function of $z$ is given by:

$M_z(t)=M_x(t)\times M_y(t)$

In words: **The MGF of the sum of independent random variables is the product of their MGFs.**

### Extension to n Variables
If you have $n$ independent random variables $x_1,x_2,...,x_n$ and define their sum $s_n=x_1+x_2+\cdots+x_n$, the MGF of $s_n$ is:

$M_{s_n}(t)=(M_{x}(t))^n$

(where all $x_i$ have the same distribution and thus the same MGF).

## Application: Central Limit Theorem
This property will be instrumental in the proof of the central limit theorem, as it allows us to show that the sum's MGF converges to the MGF of a normal distribution.

## Sketch of the Proof
- The MGF of $z=x+y$ is defined as: 
  $M_z(t)=E[e^{t z}]$
- Since $z=x+y$, substitute:
  $M_z(t)=E[e^{t(x+y)}]=E[e^{tx}e^{ty}]$
- When $x$ and $y$ are independent:
  $E[e^{tx}e^{ty}]=E[e^{tx}] \times E[e^{ty}]$
- Therefore:
  $M_z(t)=M_x(t)\times M_y(t)$

A more detailed proof would show this by writing out the full joint expectation as a double integral and splitting it, thanks to independence, but the main takeaway is the formula above.

## Important Formulas

- **MGF of sum of independent random variables:**
  $M_{x+y}(t)=M_x(t)\times M_y(t)$
- **MGF of sum of n iid random variables:**
  $M_{s_n}(t)=(M_{x}(t))^n$

***