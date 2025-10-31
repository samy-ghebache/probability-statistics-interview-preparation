# Joint, Marginal, and Conditional Probability Distributions

## Introduction
This lecture builds on conditional probability by introducing joint probability distributions for two random variables $X$ and $Y$. From joint distributions, we can derive marginal densities (by averaging out one variable) and conditional densities (probability of one variable given another).

## Joint Probability Distribution
- **Joint PDF**: For continuous random variables $X$ and $Y$, the joint probability density function is denoted $f(x,y)$.
- The probability that $(X,Y)$ lives in some 2D area is computed by integrating:
  - $P((X,Y)\in A)=\int\int_A f(x,y)\,dx\,dy$

## Marginal Density Functions
The **marginal density** allows us to obtain a PDF for just one variable by averaging out the other variable.

### Marginal Density of X
- Integrate out the $Y$ variable:
  - $f_X(x)=\int_{-\infty}^{\infty}f(x,y)\,dy$
- This gives the probability distribution of $X$ averaged over all possible values of $Y$.

### Marginal Density of Y
- Integrate out the $X$ variable:
  - $f_Y(y)=\int_{-\infty}^{\infty}f(x,y)\,dx$
- This gives the probability distribution of $Y$ averaged over all possible values of $X$.

## Discrete Random Variables
For discrete random variables, replace integrals with sums.

### Marginal Probability of X
- Sum over all possible values of $Y$:
  - $P(X=x)=\sum_y P(X=x,Y=y)$

### Marginal Probability of Y
- Sum over all possible values of $X$:
  - $P(Y=y)=\sum_x P(X=x,Y=y)$

## Conditional Density Functions
The **conditional density** is the probability distribution of one variable given that the other variable takes a specific value.

### Discrete Case
- Probability of $X=x$ given $Y=y$:
  - $P(X=x|Y=y)=\frac{P(X=x,Y=y)}{P(Y=y)}$
- This is the joint probability divided by the marginal probability of $Y$.

### Continuous Case
- Probability density of $Y$ given $X=x$:
  - $f_{Y|X}(y|x)=\frac{f(x,y)}{f_X(x)}$
- This is the joint PDF divided by the marginal density of $X$.

## Example: Two-Dimensional Gaussian
- A symmetric 2D Gaussian in $X$ and $Y$ can be written as:
  - $f(x,y)=\frac{1}{2\pi}e^{-(x^2+y^2)/2}$
- Each of $X$ and $Y$ is individually Gaussian.
- You can convert to polar coordinates: $f(r,\theta)$ where $r^2=x^2+y^2$.

## Key Points
- **Marginal densities** are obtained by integrating (or summing) out one variable from the joint distribution.
- **Conditional densities** relate to conditional probability and are computed as the joint distribution divided by the marginal distribution.
- Verify that marginal densities are valid PDFs by checking that they integrate to 1.
- These concepts generalize the conditional probability formulas used in Bayes' theorem.

## Exercises
- Verify that marginal densities are well-defined PDFs (integrate to 1).
- Practice converting between joint and marginal distributions.
- Write out the relationship between these distribution functions and the earlier conditional probability formulas.
- Try deriving marginal densities for simpler distributions.