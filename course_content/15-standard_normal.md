# Normal Distribution

## Introduction
For relatively large $n$ and moderate probabilities, the binomial distribution converges to the **normal distribution** (also called the Gaussian distribution).

## Normal Distribution Basics
- The normal distribution is a bell-shaped curve characterized by two parameters:
  - **Mean** $\mu$: The center of the distribution
  - **Standard deviation** $\sigma$: Measures the spread of the distribution
  - **Variance** $Var(X)=\sigma^2$: Standard deviation squared

- Large $\sigma$: More spread out distribution
- Small $\sigma$: Narrow, peaked distribution

## Standard Unit Normal
The **standard unit normal** is the canonical form where:
- Mean $\mu=0$
- Standard deviation $\sigma=1$

This is symmetric about $x=0$.

## Probability Density Function (PDF)
- The PDF $f(x)$ gives the probability density at value $x$.
- For continuous distributions, compute probabilities by integrating:
  - $P(a<X<b)=\int_a^b f(x)\,dx$
- Example: $P(-1<X<1)=\int_{-1}^1 f(x)\,dx$

## Cumulative Distribution Function (CDF)
- The **CDF** is the integral of the PDF from negative infinity to $x$:
  - $F(x)=\int_{-\infty}^x f(x)\,dx$
- This gives the probability that $X\leq x$: $P(X\leq x)$
- The CDF starts at 0 (at $x=-\infty$) and converges to 1 (at $x=+\infty$)
- For the standard unit normal, the CDF is denoted $\Phi$ (capital phi)

## Computing Probabilities with CDF
- $P(a<X<b)=F(b)-F(a)=\Phi(b)-\Phi(a)$
- Example: $P(-1<X<1)=\Phi(1)-\Phi(-1)$

## Standard Deviation Properties
- **68% Rule**: Approximately 68% of values fall within one standard deviation of the mean
  - $P(\mu-\sigma<X<\mu+\sigma)\approx 0.68$
- For standard unit normal: $P(-1<X<1)\approx 0.68$
- From lookup tables: $\Phi(1)\approx 0.841$
  - This means 84.1% probability of being left of $x=1$
  - By symmetry, 16% on each tail outside $[-1,1]$, giving 68% inside

## Historical Note
In the past, CDF values were looked up in printed tables. Today, these are easily computed using Python libraries like `scipy.stats`.

## Example: Coin Flips
Flip a coin 400 times with $p=\frac{1}{2}$.

- Number of heads $X$ is binomially distributed: $X\sim Binomial(n=400,p=\frac{1}{2})$
- Expected mean: $\mu=np=200$
- Variance: $\sigma^2=np(1-p)=400\times\frac{1}{2}\times\frac{1}{2}=100$
- Standard deviation: $\sigma=10$

Approximate as normal: $X\sim Normal(\mu=200,\sigma=10)$

### Computing Complex Probabilities
Question: What is $P(190\leq X\leq 230)$?

**Using binomial (hard):**
- $P(190\leq X\leq 230)=P(X=190)+P(X=191)+\ldots+P(X=230)$
- This requires summing 41 individual binomial probabilities

**Using normal approximation (easy):**
- Compute the area under the normal PDF between 190 and 230
- $P(190\leq X\leq 230)=\Phi(230)-\Phi(190)$
- Using Python or tables: approximately 85% chance

## Key Formulas
- **PDF of normal distribution**: $f(x)$
- **CDF of normal distribution**: $F(x)=\int_{-\infty}^x f(x)\,dx$
- **Probability in range**: $P(a<X<b)=F(b)-F(a)$
- **Standard unit normal CDF**: $\Phi(x)$
- **Binomial to normal approximation**: $X\sim Binomial(n,p)\approx Normal(\mu=np,\sigma^2=np(1-p))$

## Summary
The normal distribution makes probability calculations much easier than working with binomial distributions for large $n$. Using the CDF (via lookup tables historically, or Python today), you can quickly compute probabilities for ranges of values without summing many individual terms.