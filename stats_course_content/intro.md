# Introduction to Statistics: Course Overview

## Probability vs. Statistics

- **Probability** focuses on modeling uncertainty in the real world using mathematical models, combinatorics, and distributions. You assume the probability model is known and use theory to say what is likely, even without seeing any data.
- **Statistics** is about data. With statistics, you have observed data and try to infer something about the underlying probability model or its parameters. This is essential for data science and modern machine learning.

## The Duality

- In probability: Model is fixed, data is unknown, infer likelihoods of outcomes.
- In statistics: Data is fixed, model is unknown, infer or estimate the underlying model from data.

## Relevance

- Foundational for modern data science, machine learning, decision making, and prediction.
- Real world systems often defy simple analytic probability models; statistics helps learn models directly from data, even with complex or unknown densities.

***

## Course Structure

- Two-part module (intermediate and advanced), targeted for practical use.
- Core topics in ~5 hours for foundation, advance to topics like stochastic differential equations, Markov chains, Monte Carlo optimization, Bayesian methods, and practical machine learning.

***

## Survey Sampling

- **Survey sampling** or polling: Draw a small sample from a large population.
- Main goal: Use small sample to say something meaningful about the larger population, with statistical confidence.
- **Key tool:** The sample mean ($\bar{x}$), computed as the average of your measured values.

### Central Limit Theorem

- For any distribution, if you take sufficiently large random samples, the sample mean $\bar{x}$ will be approximately normally distributed:
  - Mean: $\mu$ (true population mean)
  - Variance: $\frac{\sigma^2}{n}$ (population variance divided by sample size)
- This tells us how accurate our sample mean is as an estimate of the true mean, and how large a sample ($n$) we need for desired accuracy.

  $$
  \text{If sample size is }n,\ \ \bar{x}\sim N\left(\mu,\frac{\sigma^2}{n}\right)
  $$

- This is **distribution-free**: applies regardless of the underlying population shape.

***

## Hypothesis Testing

- Test hypotheses using data and probability distributions.
- Examples:
  - **Does a drug work?**: Use control and treatment groups, test if means differ.
  - **Did a marketing campaign increase web traffic?**: A/B testing.
  - **Are two distributions the same?**: Use tests like the chi-squared test.

- **Statistical significance (p-value):** Quantifies confidence in a result, e.g., $p<0.05$ means the result is "statistically significant."
- Pitfalls: Bad experiment design or fraudulent analysis can give misleading results. It is critical to design experiments and tests correctly.

***

## Experimental Design

- Planning experiments and data collection protocols to test hypotheses honestly, accurately, and with sufficient power and significance.
- The *significance level* is the risk threshold for rejecting a null hypothesis; commonly set as $p=0.05$.

***

## Parameter Estimation & Fitting Distributions

- **Fitting distributions:** Infer the best probability distribution and its parameters from data. This is the bridge to machine learning.
- *Probability*: $P(X|\theta)$: data given model parameters ($\theta$)
- *Statistics*: $P(\theta|X)$: best-fit parameters given observed data

### Methods

- **Method of Moments:** Estimate parameters by equating sample moments to population moments.
- **Maximum Likelihood Estimation (MLE):** Optimize parameters to maximize the probability of observed data.
- **Goodness-of-fit & Confidence Intervals:** Assess how well the model fits and quantify uncertainty in parameter estimates.
- **Bootstrapping & Monte Carlo Simulation:** Use repeated sampling and simulation to estimate uncertainty, especially when analytic solutions are impossible.

***

## Bayesian Statistics

- Bayesian statistics allows incorporating prior knowledge or beliefs into estimates.
- Probability models (e.g., coin toss) can be "updated" with observed data to refine parameter estimates.
- Bayesian techniques prevent overconfidence due to small sample sizes by incorporating logical priors.

***

## Toward Modern Statistics & Machine Learning

- The field advances toward fitting complex empirical distributions from massive data ("big data").
- Tools like calculus, linear algebra, and statistics are required to model the complexity and uncertainty in modern data-centric applications.

***

## Key Formulas

- **Sample mean:** $\bar{x}=\frac{1}{n}\sum_{i=1}^n x_i$
- **Central limit theorem:** If sample size is $n$, $\bar{x}\sim N(\mu,\frac{\sigma^2}{n})$
- **Variance of sample mean:** $\text{Var}(\bar{x})=\frac{\sigma^2}{n}$
- **p-value:** $p=P(\text{data}|\text{null hypothesis true})$
- **MLE example:** $\hat{\theta}_{MLE}=\arg\max_\theta P(X|\theta)$

***
