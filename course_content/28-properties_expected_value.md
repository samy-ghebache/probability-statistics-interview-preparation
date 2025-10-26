# Expected Value: Properties

## Three Important Properties of Expected Value

### Property 1: Linearity
The expected value of a sum equals the sum of expected values.

**Formula:**
- $E[X+Y]=E[X]+E[Y]$

**Key Points:**
- This works for any random variables X and Y (they don't need the same distribution or to be independent).
- Extends to larger sums: $E[X+Y+Z]=E[X]+E[Y]+E[Z]$
- This is called the linearity property.

### Property 2: Product of Independent Variables
If X and Y are independent, the expected value of their product equals the product of their expected values.

**Formula:**
- If X and Y are independent: $E[X\times Y]=E[X]\times E[Y]$

**Important:**
- Independence means: $P(X,Y)=P(X)\times P(Y)$
- This property is **only true** for independent variables.
- If X and Y are dependent, then $E[X\times Y]\neq E[X]\times E[Y]$

**Proof for discrete random variables:**

Starting with the definition:
$E[X\times Y]=\sum_{X,Y}x\times y\times P(X=x,Y=y)$

Since X and Y are independent:
$E[X\times Y]=\sum_{X,Y}x\times y\times P(X=x)\times P(Y=y)$

Rearranging the sums:
$E[X\times Y]=\sum_{X}x\times P(X=x)\times\sum_{Y}y\times P(Y=y)$

This simplifies to:
$E[X\times Y]=E[X]\times E[Y]$

### Property 3: Expected Value of a Function
If Y is a function of X, i.e., $Y=G(X)$, then the expected value of Y is computed by replacing x with $G(x)$ in the expectation formula.

**Formula:**
- For discrete X: $E[G(X)]=\sum_{x}G(x)\times P(X=x)$
- For continuous X: $E[G(X)]=\int_{-\infty}^{\infty}G(x)\times f(x)dx$

**Important:**
- This property is not obvious and requires proof (not shown here).
- You simply plug the function $G(x)$ where you would normally see x in the expectation formula.

**Example:**
The expected value of $X^2$ (the second moment):
$E[X^2]=\int_{-\infty}^{\infty}x^2\times f(x)dx$

This is useful for computing variance and standard deviation.

## Generalizations
You can combine these properties. For example, if X and Y are independent:
$E[G(X)\times H(Y)]=E[G(X)]\times E[H(Y)]$

## Summary
1. **Linearity:** $E[X+Y]=E[X]+E[Y]$ (always true)
2. **Product (independent only):** $E[X\times Y]=E[X]\times E[Y]$ (only if independent)
3. **Function of X:** $E[G(X)]=\sum G(x)\times P(x)$ or $\int G(x)\times f(x)dx$