# Functions of Random Variables

## Introduction
Functions of random variables allow us to transform one random variable into another. If $X$ is a random variable and $G$ is a function, we can define a new random variable $Y=G(X)$. This is important for converting between different representations of data.

## Examples of Functions of Random Variables
- Converting temperature from Fahrenheit to Celsius.
- Computing the distribution of $X^2$ when $X$ is normally distributed.
- Converting velocity distribution to kinetic energy distribution: $Y=\frac{1}{2}mX^2$ where $X$ is velocity.

## Notation
- **PDF (Probability Density Function)**: $f_X(x)$ is the PDF of random variable $X$.
- **CDF (Cumulative Density Function)**: $F_X(x)=P(X\leq x)=\int_{-\infty}^{x}f_X(t)dt$ is the CDF of $X$.
- For the new random variable $Y=G(X)$:
  - PDF of $Y$: $f_Y(y)$
  - CDF of $Y$: $F_Y(y)$

## Key Principle
You **cannot** directly transform the PDF of $X$ into the PDF of $Y$ by simply plugging $X$ into $G$. This does not preserve the property that the area under the PDF equals 1.

Instead, you must:
1. Convert the CDF of $X$ to the CDF of $Y$.
2. Differentiate the CDF of $Y$ to get the PDF of $Y$.

## Procedure for Finding the Distribution of $Y=G(X)$
### Step 1: Find the CDF of $Y$
$F_Y(y)=P(Y\leq y)=P(G(X)\leq y)$

Express this in terms of $X$ and use the CDF of $X$.

### Step 2: Differentiate to Get the PDF of $Y$
$f_Y(y)=\frac{d}{dy}F_Y(y)$

## Example: Linear Transformation
Let $X$ be a normally distributed random variable with mean $\mu$ and standard deviation $\sigma$: $X\sim N(\mu,\sigma^2)$.

Define $Y=aX+b$ where $a>0$ and $b$ are constants (e.g., converting Celsius to Fahrenheit: $Y=\frac{9}{5}X+32$).

### Finding the CDF of $Y$
$F_Y(y)=P(Y\leq y)=P(aX+b\leq y)=P(X\leq\frac{y-b}{a})=F_X(\frac{y-b}{a})$

### Finding the PDF of $Y$
$f_Y(y)=\frac{d}{dy}F_Y(y)=\frac{d}{dy}F_X(\frac{y-b}{a})=\frac{1}{a}f_X(\frac{y-b}{a})$

### Result
If $X\sim N(\mu,\sigma^2)$, then $Y=aX+b\sim N(a\mu+b,a^2\sigma^2)$.

## Important Applications
### Chi-Squared Distribution
If $X\sim N(0,1)$ (standard normal), then $Y=X^2$ follows a chi-squared distribution. This is used in hypothesis testing to determine if data fits an expected distribution.

### Standardization
To convert a normal distribution $X\sim N(\mu,\sigma^2)$ to a standard normal $Z\sim N(0,1)$:
$Z=\frac{X-\mu}{\sigma}$

This uses $a=\frac{1}{\sigma}$ and $b=-\frac{\mu}{\sigma}$ in the linear transformation formula.

## Summary
- To find the distribution of $Y=G(X)$, use the CDF method.
- Relate $F_Y(y)$ to $F_X(x)$ using the transformation $G$.
- Differentiate $F_Y(y)$ to obtain $f_Y(y)$.
- This procedure preserves the property that probabilities sum to 1.