# Joint Probability Distributions

## Introduction
A **joint probability distribution** describes how two (or more) random variables depend on each other and jointly affect the probability of both events happening.

## Definition
Given two random variables $X$ and $Y$, the joint probability distribution is:
- $P(x,y)$ = probability that random variable $X$ equals $x$ AND random variable $Y$ equals $y$

This concept applies to both discrete and continuous random variables.

## Examples of Joint Distributions

### Turbulent Fluid Flow
- In turbulence, the velocity components $U$, $V$, and $W$ (in $X$, $Y$, $Z$ directions) are jointly distributed random variables.
- The joint distribution depends on the flow structure.
- In isotropic turbulence, components might be independent.
- In boundary layer flows, there is specific structure to the joint distribution.

### Medical and Health Data
- Patient demographics, biometrics, and health outcomes are jointly distributed.
- Example: Probability of heart disease given age, gender, location, height, weight, etc.
- These joint distributions inform medical decisions.
- Principal Component Analysis (PCA) uses joint distributions of high-dimensional data.

### Sports Analytics
- Camera data tracking player positions on a basketball court creates a probability density of where a player is most likely to be.
- This is a continuous joint distribution over the court coordinates.

## Continuous Joint Distributions
For continuous random variables, the joint probability density function (PDF) is denoted $f(x,y)$.
- The probability of being in a region $A$ is:
  - $P((X,Y)\in A)=\int\int_A f(x,y)\,dx\,dy$

## Two-Dimensional Gaussian
If $X$ and $Y$ are both normally distributed (Gaussian) random variables:
- The joint distribution $f(x,y)$ is a two-dimensional Gaussian.
- This is radially symmetric if $X$ and $Y$ are independent.
- This is the underlying assumption in PCA: high-dimensional data follows a high-dimensional Gaussian distribution.

## Marginal Distributions
- The **marginal distribution** is obtained by averaging out one variable.
- Marginal distribution of $X$: Average out all $Y$ values.
- Marginal distribution of $Y$: Average out all $X$ values.
- For a 2D Gaussian joint distribution, each marginal distribution is also Gaussian.

## Independence
Two random variables $X$ and $Y$ are **independent** if:
- $P(x,y)=P(x)\times P(y)$

This means the joint probability is the product of individual probabilities.

### Connection to Separation of Variables
- Independence is like separation of variables in differential equations.
- If variables are independent, the joint PDF can be written as a product: $f(x,y)=f_X(x)\times f_Y(y)$

### Example: Dartboard
- When throwing darts at a circular board, aiming for the bullseye creates a 2D Gaussian distribution.
- In Cartesian coordinates $(x,y)$, this distribution is NOT separable (not independent in $x$ and $y$).
- In polar coordinates $(r,\theta)$, the distribution might be separable (independent in radius and angle).
- Good coordinate systems can reveal independence; bad coordinates can obscure it.

## Key Formula
- **Joint probability (discrete):** $P(x,y)$
- **Joint PDF (continuous):** $f(x,y)$
- **Independence:** $P(x,y)=P(x)\times P(y)$ or $f(x,y)=f_X(x)\times f_Y(y)$
- **Probability in region $A$:** $P((X,Y)\in A)=\int\int_A f(x,y)\,dx\,dy$

## Summary
- Joint distributions describe how multiple random variables relate to each other.
- Independence allows factorization of joint distributions into products.
- Marginal distributions are obtained by averaging out variables.
- Good coordinate systems can simplify joint distributions (like polar vs. Cartesian).
- Applications include turbulence, medical data, sports analytics, and PCA.