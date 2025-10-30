# Central Limit Theorem

## Statement of the Theorem
The central limit theorem states: given a collection of independent, identically distributed random variables $x_1,x_2,\ldots,x_n$ with mean zero and variance $\sigma^2$, their sum $s_n=x_1+x_2+\ldots+x_n$ becomes normally distributed as $n$ becomes large. This result is true regardless of the original distribution, as long as the variables are sampled independently and have the same mean and variance.

## Mathematical Formulation
- **Normalizing the sum:** The normalized sum $z=\frac{s_n}{\sigma\sqrt{n}}$ will tend to the standard normal distribution as $n\to\infty$.
- **CDF convergence:** The cumulative distribution function of $z$ converges to that of the standard unit normal with mean $0$ and standard deviation $1$ as $n$ increases.
- **Equivalent forms:**
  - $s_n$ is normal with mean $0$ and variance $n\sigma^2$.
  - The average $\bar{x}=\frac{1}{n}(x_1+\ldots+x_n)$ is normal with mean $0$ and variance $\frac{\sigma^2}{n}$.

## Proof Outline Using Moment Generating Functions

### Step 1: Proof Approach
- Goal: Show the normalized variable $z=\frac{s_n}{\sigma\sqrt{n}}$ is standard normal with mean $0$ and standard deviation $1$.
- Method: Show $z$ has the same moment generating function as the standard unit normal.

### Step 2: Moment Generating Functions of Each Variable
- Each $x_i$ has moment generating function $m(t)$, because all are sampled from the same distribution.

### Step 3: Moment Generating Function of the Sum
- The moment generating function of $s_n$ is $m(t)^n$.

### Step 4: Taylor Series Expansion
- $m(t)=m(0)+tm'(0)+\frac{t^2}{2}m''(0)+\ldots$
- $m(0)=1$ (zeroth moment)
- $m'(0)=0$ (mean is zero)
- $\frac{t^2}{2}m''(0)=\frac{t^2\sigma^2}{2}$
- Higher order terms are denoted as $\epsilon$ and go to zero as $n\to\infty$.

### Step 5: Plug In the Normalization
- If $y=bx$, the moment generating function of $y$ is $m(bt)$.
- For $z=\frac{s_n}{\sigma\sqrt{n}}$, use $m\left(\frac{t}{\sigma\sqrt{n}}\right)^n$.

### Step 6: Taylor Expand the Normalized MGF
- $m\left(\frac{t}{\sigma\sqrt{n}}\right)\approx 1+\frac{1}{2}\sigma^2\left(\frac{t}{\sigma\sqrt{n}}\right)^2+\epsilon$
- Simplifies to $1+\frac{t^2}{2n}+\epsilon$

### Step 7: Take Limit as $n\rightarrow\infty$
- The moment generating function is $\left(1+\frac{t^2}{2n}+\epsilon\right)^n$
- Letting $n\to\infty$, $\epsilon$ vanishes and the limit is $e^{t^2/2}$
  - $\lim_{n\to\infty}\left(1+\frac{a}{n}\right)^n=e^a$

### Step 8: Conclusion
- $z$ and the standard unit normal share the same moment generating function $e^{t^2/2}$.
- Therefore, they have the same probability distribution, proving the central limit theorem.

## Summary of Key Formulas

- **Normalized sum:** $z=\frac{s_n}{\sigma\sqrt{n}}$
- **Moment generating function of $z$:** $m_z(t)=m_{s_n}\left(\frac{t}{\sigma\sqrt{n}}\right)$
- **MGF limit:** $\lim_{n\to\infty}\left(1+\frac{t^2}{2n}\right)^n=e^{t^2/2}$
- **Standard normal MGF:** $m_{N(0,1)}(t)=e^{t^2/2}$

***