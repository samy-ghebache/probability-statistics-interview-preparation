# Chebyshev's Inequality

## Statement of Chebyshev's Inequality
- For any random variable $X$ with mean $\mu$ and variance $\sigma^2$, and for any $a>0$:
  - $P(|X-\mu|\geq a)\leq\frac{\sigma^2}{a^2}$
- This inequality gives an upper bound on the probability that $X$ deviates from its mean by $a$ or more.

## Explanation and Illustration
- If you have a distribution for $X$ with mean $\mu$ and standard deviation $\sigma$, Chebyshev's inequality tells you that the probability of $X$ being far from $\mu$ (by at least $a$) cannot be large unless the distribution is very spread out (large variance).
- This result works for all distributions with a defined mean and variance, not just normal distributions.

## Proof Outline

1. **Introduce new variable:** Let $Y=(X-\mu)^2$, and let $B=a^2$.
2. Notice: $P(|X-\mu|\geq a)=P((X-\mu)^2\geq a^2)=P(Y\geq B)$.
3. **Apply Markov's inequality:** For any non-negative random variable $Y$ and constant $B>0$, $P(Y\geq B)\leq\frac{E[Y]}{B}$.
4. Here, $E[Y]=E[(X-\mu)^2]=\sigma^2$.
5. Substitute into Markov’s inequality: $P(Y\geq B)\leq\frac{\sigma^2}{a^2}$.

## Intuition
- Chebyshev's inequality says you can't have too much probability mass far from the mean unless the variance is large.
- If the variance is small, most values are close to the mean with high probability.

## Relation to Markov's Inequality
- Markov's inequality: For a non-negative random variable and $a>0$, $P(X\geq a)\leq\frac{E[X]}{a}$.
- Chebyshev’s uses the variance (the expected squared deviation from the mean), resulting in an inequality for deviations from the mean.

## Key Formulas
- Chebyshev: $P(|X-\mu|\geq a)\leq\frac{\sigma^2}{a^2}$
- Markov: $P(X\geq a)\leq\frac{E[X]}{a}$

## Application
- These inequalities are fundamental tools in probability and statistics.
- Chebyshev's inequality is essential for proving the law of large numbers and understanding the behavior of averages and deviations in random samples.

***