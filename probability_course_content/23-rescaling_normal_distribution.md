# Random Variables

## Introduction
A **random variable** in probability and statistics is a variable that can take on a set of possible values, each with an associated probability. Just like variables in algebra or calculus, random variables can be discrete or continuous.

## Example: Coin Flips
- Flip a fair coin 4 times.
- The sample space $\Omega$ consists of all possible sequences (e.g., HHHH, HHHT, ..., TTTT).
- There are $2^4=16$ possible outcomes.
- Define random variable $X$ as the number of heads in the 4 flips.
- $X$ can take values $0,1,2,3,4$.

## Discrete vs. Continuous Random Variables
- **Discrete random variable**: Takes on a countable set of values (e.g., number of heads).
- **Continuous random variable**: Takes on any value in a range (e.g., height of Americans).

## Assigning Probabilities
Each value of $X$ has a probability:
- $P(X=0)=\frac{1}{16}$
- $P(X=1)=\frac{4}{16}$
- $P(X=2)=\frac{6}{16}$
- $P(X=3)=\frac{4}{16}$
- $P(X=4)=\frac{1}{16}$

This is an example of the **binomial distribution**.

## Probability Distribution
A **probability distribution** summarizes the probabilities for all possible values of a random variable $X$.
- For the coin flip example, the distribution is:
  - $X$: $0,1,2,3,4$
  - $P(X)$: $\frac{1}{16},\frac{4}{16},\frac{6}{16},\frac{4}{16},\frac{1}{16}$

## Probability Density Function (PDF)
- For continuous random variables, the probability distribution is called a **probability density function (PDF)**.
- The PDF is a model of a random process.
- Real-world processes are approximated by mathematical distributions (e.g., binomial, normal).

## Applications
- **Hypothesis testing**: Use data to test if a process follows a certain distribution.
- **Parameter estimation**: Estimate parameters (e.g., mean, standard deviation) from data.
- **Visualization**: Plot probability distributions to summarize data.
- **Computation**: Calculate probabilities for ranges of values.

## Calculus with Random Variables
- For continuous distributions, probability for a range is computed by integrating the PDF:
  - $P(4<X<6)=\int_4^6 p(X)\,dX$
- For discrete distributions, use sums:
  - $P(4<X<6)=\sum_{k=4}^{6}P(X=k)$

## Functions of Random Variables
- You can define functions on random variables:
  - Expected value: $E[X]$
  - Variance: $Var(X)$
  - Standard deviation: $\sigma_X$
- You can propagate uncertainty through systems (e.g., engineering, dynamics).

## Cumulative Distribution Function (CDF)
- The **cumulative distribution function (CDF)** gives the probability that $X$ is less than a certain value:
  - $F(x)=\int_{-\infty}^x p(X)\,dX$

## Summary
- Random variables provide a concise summary of all probabilities.
- Probability distributions (PDFs for continuous, probability mass functions for discrete) model random processes.
- These tools allow for hypothesis testing, parameter estimation, visualization, and computation.
- You can build functions on random variables and propagate uncertainty through systems.
- The CDF is another useful function related to random variables.

---

# Functions of Random Variables and Standardization

## Functions of Random Variables
- If you have a random variable $X$ with a known PDF and CDF, you can create a new random variable $Y=G(X)$ where $G$ is some function (e.g., $X^2$, $aX+b$, $\sqrt{X}$).
- There is a procedure to build the PDF and CDF of $Y$ from the PDF and CDF of $X$.
- Start with the CDF of $X$ to build the CDF of $Y$, then differentiate to get the PDF of $Y$.

## Linear Transformation of Normal Distribution
- If $X$ is normally distributed with mean $\mu$ and standard deviation $\sigma$ (written as $X\sim N(\mu,\sigma)$), and you create a new variable $Y=aX+b$, then:
  - $Y$ is also normally distributed.
  - New mean: $a\mu+b$
  - New standard deviation: $a\sigma$
  - New variance: $a^2\sigma^2$

## Standard Normal Distribution
- The **standard unit normal distribution** has mean $0$ and standard deviation $1$.
- Written as $Y\sim N(0,1)$.
- This is a special case that is very useful for calculations.

## Standardization (Z-Score)
- To map a normal distribution $X\sim N(\mu,\sigma)$ to the standard normal $Y\sim N(0,1)$, use:
  - $Y=\frac{X-\mu}{\sigma}$
- This shifts the distribution to center it at zero (by subtracting $\mu$) and scales it (by dividing by $\sigma$) so the standard deviation becomes $1$.

## Why Standardization is Useful
- In the past, computing probabilities for arbitrary normal distributions was difficult.
- The standard normal distribution has well-documented lookup tables for its cumulative distribution function (CDF), often denoted as $\Phi$.
- By standardizing, you can map any normal distribution calculation to the standard normal and use these tables.

## Computing Probabilities Using Standardization
- To compute $P(a<X<b)$ for $X\sim N(\mu,\sigma)$:
  - Standardize the bounds: $\frac{a-\mu}{\sigma}$ and $\frac{b-\mu}{\sigma}$
  - Compute: $P(a<X<b)=P\left(\frac{a-\mu}{\sigma}<Y<\frac{b-\mu}{\sigma}\right)$
  - Use the standard normal CDF: $\Phi\left(\frac{b-\mu}{\sigma}\right)-\Phi\left(\frac{a-\mu}{\sigma}\right)$

## The Standard Normal CDF
- The CDF of the standard normal is denoted $\Phi$ (uppercase phi).
- It represents the area under the standard normal curve from $-\infty$ to a given value.
- Available in statistical tables and as function calls in modern software.

## Modern Usage
- Today, computers can directly compute probabilities for any normal distribution.
- However, standardization is still a useful concept for understanding and analysis.
- Many statistical procedures and software still use standardization internally.

## Summary of Key Formulas
- **Linear transformation of normal variable:**
  - If $X\sim N(\mu,\sigma)$ and $Y=aX+b$, then $Y\sim N(a\mu+b,a\sigma)$
- **Standardization:**
  - $Y=\frac{X-\mu}{\sigma}$ transforms $X\sim N(\mu,\sigma)$ to $Y\sim N(0,1)$
- **Probability using standardization:**
  - $P(a<X<b)=\Phi\left(\frac{b-\mu}{\sigma}\right)-\Phi\left(\frac{a-\mu}{\sigma}\right)$