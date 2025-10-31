# Central Limit Theorem

## Statement
The **central limit theorem (CLT)** is one of the most important results in probability and statistics. It states that if you take $n$ independent and identically distributed random variables $X_1,X_2,...,X_n$ (for example, $n$ coin flips, dice rolls, survey responses, or measurements), then the sample mean will converge to the mean of the underlying distribution as $n$ grows large.

## Sample Mean
Let the sample mean be:
$x_n=\frac{1}{n}\sum_{i=1}^{n}X_i$

As $n$ increases,
- $x_n$ becomes a normally distributed random variable
- Mean: $\mu$
- Variance: $\frac{\sigma^2}{n}$
- Standard deviation: $\frac{\sigma}{\sqrt{n}}$

## Central Limit Theorem Formula
The distribution of the sample mean for large $n$:
$x_n\sim N(\mu,\frac{\sigma^2}{n})$

## Practical Implication
If you average enough samples, regardless of the original distribution (uniform, exponential, etc.), the sample mean will look Gaussian (normal). The expected value of the mean is the true population mean and the sampling distribution’s standard deviation gets smaller with more samples.

## Application to Sums
You can also express CLT in terms of the sum $S_n$:
$S_n=\sum_{k=1}^{n}X_k$

For large $n$,
$S_n\sim N(n\mu,n\sigma^2)$
- Mean: $n\mu$
- Variance: $n\sigma^2$
- Standard deviation: $\sigma\sqrt{n}$

## Importance
- Works for any original distribution as long as variables are independent and identically distributed with a well-defined mean and variance.
- Explains why the normal distribution occurs so often in statistics.
- Fundamental to experimental error, confidence intervals, and statistical hypothesis testing.

## Moment Generating Function
The theoretical proof relies on the **moment generating function**, denoted $M(t)$ for a probability density $p(x)$. For sums of independent variables:
$M_{S_n}(t)=\prod_{i=1}^{n}M_{X_i}(t)$
As $n$ increases, this product approximates the moment generating function of a normal distribution.

## Summary of Key Formulas
- Sample mean: $x_n=\frac{1}{n}\sum_{i=1}^{n}X_i$
- CLT for means: $x_n\sim N(\mu,\frac{\sigma^2}{n})$
- CLT for sums: $S_n\sim N(n\mu,n\sigma^2)$
- Standard deviation (mean): $\frac{\sigma}{\sqrt{n}}$
- Standard deviation (sum): $\sigma\sqrt{n}$
- Moment generating function (sum): $M_{S_n}(t)=\prod_{i=1}^{n}M_{X_i}(t)$

***
