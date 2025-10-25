# Chi-Squared Distribution

## Introduction
This lecture shows how to derive the **chi-squared distribution**, which is the distribution of $X^2$ when $X$ is a normally distributed random variable. The chi-squared distribution is extremely useful for hypothesis testing in statistics.

## Setup
- Let $X$ be a standard unit normal (Gaussian) distribution: mean 0, standard deviation 1.
- Define a new random variable: $Y=X^2$
- $Y$ follows the **chi-squared distribution**.

## Applications of Chi-Squared
- **Hypothesis testing**: Testing if collected data matches a proposed distribution.
- If you subtract data from a model and square the errors, those squared errors approximately follow a normal distribution (by the Central Limit Theorem).
- The sum of squares of these errors follows a chi-squared distribution.
- Chi-squared can be used even when the original distribution is not normal.

## Derivation Procedure
You cannot simply square the PDF of $X$ to get the PDF of $Y=X^2$. Instead, follow these steps:

### Step 1: Write the CDF of $Y$
The cumulative density function of $Y$ is:
$F_Y(y)=P(Y<y)=P(X^2<y)$

### Step 2: Relate to $X$
$P(X^2<y)=P(-\sqrt{y}<X<\sqrt{y})$

This means $X$ must be between $-\sqrt{y}$ and $+\sqrt{y}$.

### Step 3: Express Using CDF of $X$
For a standard unit normal, the CDF is denoted $\Phi$ (phi):
$F_Y(y)=\Phi(\sqrt{y})-\Phi(-\sqrt{y})$

### Step 4: Differentiate to Get PDF
To get the probability density function of $Y$, take the derivative with respect to $y$:
$f_Y(y)=\frac{d}{dy}F_Y(y)$

Using the chain rule:
$f_Y(y)=\Phi'(\sqrt{y})\cdot\frac{1}{2}y^{-1/2}-\Phi'(-\sqrt{y})\cdot(-\frac{1}{2})y^{-1/2}$

### Step 5: Simplify
The derivative $\Phi'$ is just the PDF of $X$, denoted $f_X$. Due to symmetry of the normal distribution:
$f_Y(y)=y^{-1/2}\cdot f_X(\sqrt{y})$

### Step 6: Substitute the Normal PDF
The PDF of standard unit normal is:
$f_X(x)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}$

Plugging in $\sqrt{y}$ for $x$:
$f_Y(y)=y^{-1/2}\cdot\frac{1}{\sqrt{2\pi}}e^{-y/2}$

## Final Result: Chi-Squared PDF
$f_Y(y)=\frac{y^{-1/2}e^{-y/2}}{\sqrt{2\pi}}$

This is the **chi-squared distribution** (specifically, chi-squared with 1 degree of freedom).

## Key Formulas
- **Standard unit normal PDF**: $f_X(x)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}$
- **Chi-squared PDF** (for $Y=X^2$): $f_Y(y)=\frac{y^{-1/2}e^{-y/2}}{\sqrt{2\pi}}$
- **General procedure**: $f_Y(y)=\frac{d}{dy}F_Y(y)$, where $F_Y(y)$ is expressed in terms of known CDFs.

## Important Notes
- You cannot just square the PDF of $X$ to get the PDF of $Y=X^2$. That would not be a valid probability density.
- Always start with the CDF of the new variable, relate it to the old variable, then differentiate.
- The chi-squared distribution will be used extensively in later lectures on hypothesis testing.