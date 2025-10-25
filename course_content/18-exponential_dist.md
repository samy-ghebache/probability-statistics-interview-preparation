# Exponential Distribution

## Definition
A random time $T$ is **exponentially distributed** with parameter $\lambda$ if the probability density function is:

$$f(t)=\lambda e^{-\lambda t}$$

for $t\geq 0$, and $f(t)=0$ for $t<0$.

## Applications
- Modeling the time until rare events occur
- Light bulb lifetimes and failure times
- Radioactive decay
- Waiting times (e.g., at the DMV)

## Parameter $\lambda$
- $\lambda$ is a positive number representing the rate parameter
- $\lambda=\frac{1}{\text{average lifetime}}$
- Expected value: $E[T]=\frac{1}{\lambda}$
- Standard deviation: $\sigma=\frac{1}{\lambda}$

## Probability in a Range
The probability that the event occurs between times $a$ and $b$ is:

$$P(a<T<b)=\int_a^b \lambda e^{-\lambda t}dt=e^{-\lambda a}-e^{-\lambda b}$$

## Cumulative Distribution Function (CDF)
The cumulative distribution function is:

$$F(t)=\int_{-\infty}^t P(T=t)dt=1-e^{-\lambda t}$$

This gives the probability that the event occurs before time $t$.

## Exercises
1. **Derive the CDF**: Show that $F(t)=1-e^{-\lambda t}$ by integrating the PDF.
2. **Verify normalization**: Show that $\int_{-\infty}^{\infty}P(T=t)dt=1$.

## Example 1: Light Bulb Lifetime
- Average lifetime of a light bulb: 100 hours
- Therefore: $\lambda=\frac{1}{100}$
- **Question**: What is the probability that a random light bulb lasts at least 50 hours?

**Solution**:
$$P(T\geq 50)=1-P(T<50)=1-F(50)=e^{-\lambda\times 50}=e^{-\frac{1}{100}\times 50}=e^{-0.5}$$

This equals approximately 0.61, or 61% chance.

## Example 2: Radioactive Decay (Polonium-210)
- Halflife of Polonium-210: 138 days
- Halflife means: $F(138)=\frac{1}{2}$
- Therefore: $1-e^{-138\lambda}=\frac{1}{2}$
- Solving for $\lambda$: $e^{-138\lambda}=\frac{1}{2}$
- Taking natural log: $-138\lambda=\ln(\frac{1}{2})=-\ln(2)$
- Result: $\lambda=\frac{\ln(2)}{138}$

**Useful questions**:
- What is the probability that one atom lasts 365 days?
- How long for 99% of a kilogram to decay?

## Memoryless Property
The exponential distribution has a unique **memoryless property**:

$$P(T>t+s|T>s)=P(T>t)$$

**Interpretation**: If time $s$ has already passed without the event occurring, the probability of lasting another $t$ time units is the same as the original probability starting from time zero. The "clock resets."

**Example**: If a light bulb has an expected lifetime of 1000 hours and has already lasted 1000 hours, the expected remaining lifetime is still 1000 hours.

## Key Formulas Summary
- **PDF**: $P(T=t)=\lambda e^{-\lambda t}$ for $t\geq 0$
- **CDF**: $F(t)=1-e^{-\lambda t}$
- **Probability in range**: $P(a<T<b)=e^{-\lambda a}-e^{-\lambda b}$
- **Expected value**: $E[T]=\frac{1}{\lambda}$
- **Standard deviation**: $\sigma=\frac{1}{\lambda}$
- **Memoryless property**: $P(T>t+s|T>s)=P(T>t)$

## Connection to Other Topics
- The exponential distribution is intimately related to the **Poisson process**
- The **hazard function** is another important concept related to exponential distributions